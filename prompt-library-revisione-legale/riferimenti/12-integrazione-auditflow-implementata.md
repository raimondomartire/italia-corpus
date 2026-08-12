# Integrazione in AuditFlow — cosa è stato implementato

Questo documento descrive l'integrazione della libreria prompt in **AuditFlow** (repository `raimondomartire/AuditFlow_Dashboard`), realizzata secondo le priorità discusse in `10-mappatura-auditflow.md` e `11-playbook-operativo-per-fase.md`: prima i due bug/lacune concrete che rendevano inaffidabile un avviso sui documenti, poi il pezzo di dato mancante (la libreria come cosa interrogabile dal software), poi i due punti di intervento in UI — Document Manager per i documenti in ingresso, Smart Audit Box per il prompt da eseguire.

**Stato:** mergiato in `main` del repository AuditFlow (via `feat/libreria-prompt-revisione-legale`, senza fast-forward per preservare la cronologia). Il branch `main` era avanzato più volte durante il lavoro (fatturazione Stripe, cruscotto ispezioni MEF, spinner Delphi, e in generale sviluppo attivo concorrente): ogni volta il merge è stato rifatto integrando i nuovi commit, non sovrascrivendoli, con un solo conflitto reale in `backend/main.py` (due router aggiunti nello stesso punto — risolto tenendo entrambi). Dopo ogni merge sono stati rieseguiti `tsc --noEmit` e la verifica end-to-end in browser (vedi § Verifiche) sul codice effettivamente arrivato su `main`, non solo sul branch isolato. **Verificato solo su SQLite in locale**, non sull'ambiente Postgres/App_Master di sviluppo o produzione — quello resta da fare da chi ha accesso a quell'ambiente.

## Perché queste priorità

Prima di scrivere codice, la sessione ha esplorato il codice sorgente di AuditFlow per capire cosa esisteva già, invece di indovinare. Sono emersi tre fatti che hanno determinato l'ordine di lavoro:

1. Il concetto di "documento mancante con ciclo di vita" **esisteva già** (`Segnaposto`, in `backend/models_dm.py`) — andava riusato, non reinventato.
2. Il KPI "documenti mancanti" della dashboard **contava sempre zero**, per un bug silenzioso (confronto con una stringa `"RICHIESTO"` mai esistita nel modello). Costruire un avviso sopra un dato rotto sarebbe stato peggio di nessun avviso.
3. Non esisteva **nessuna tabella o file** con i 177 prompt come dato interrogabile: i prompt dello Smart Audit Box (l'unica chat AI scoped a una singola carta, tra le 4 famiglie di chat presenti nel software) venivano costruiti al volo in Python, non salvati. Questo era il vero pezzo mancante, non la scelta tra "sezione chat" o "bottone nel document manager" — servivano entrambi i punti di intervento, appoggiati allo stesso dato.

## Cosa è stato aggiunto

### Backend

| File | Cosa fa |
| --- | --- |
| `backend/seed_data/scheda_prompt/scheda_prompt_v1.json` | Le 177 schede della libreria (stessi dati di questo repository), pronte per essere lette dal backend. |
| `backend/routers/scheda_prompt.py` | Nuovo router di sola lettura. Nessuna tabella né migrazione: la libreria è materiale di riferimento statico, non stato di un incarico, quindi segue lo stesso pattern già in uso in `routers/sci.py` (JSON in cache con `@lru_cache`). Espone: `GET /api/scheda-prompt` (elenco, filtri per fase AuditFlow/parte/testo libero), `GET /api/scheda-prompt/meta/fasi` (conteggi per fase), `GET /api/scheda-prompt/by-cod-carta/{cod}` (risolve il codice di una carta sulla scheda corrispondente), `GET /api/scheda-prompt/{codice}`. |
| `backend/routers/document_manager.py` | Nuovo endpoint `POST /api/dm/segnaposti/from-scheda`: dati `carta_id` e `scheda_codice`, crea un segnaposto per ciascun documento richiesto dalla scheda (nodo + carta + segnaposto, riusando esattamente lo schema già impiegato dagli endpoint esistenti di creazione). Idempotente sull'etichetta del documento: rilanciarlo non duplica i segnaposti già creati per la stessa scheda. |
| `backend/routers/incarico_dashboard.py` | **Correzione bug**: il KPI `documenti_mancanti` confrontava `Segnaposto.stato` con `"RICHIESTO"`, valore mai esistito nel modello (che usa stati minuscoli: `atteso`, `caricato`, `in_validazione`, `respinto`, `accettato`, …) — quindi il conteggio era sempre zero, silenziosamente, dentro un blocco `try/except`. Ora conta correttamente i segnaposti negli stati non risolti. |
| `backend/main.py` | Registra il nuovo router (`scheda_prompt.router`), stesso pattern di tutti gli altri router del progetto. |

### Frontend

| File | Cosa fa |
| --- | --- |
| `frontend/.../SchedaPromptPanel.tsx` (nuovo) | Pannello che, data la carta aperta, mostra la scheda-prompt corrispondente (match sul codice carta): documenti da allegare con il pulsante **"Richiedi documenti mancanti"** (chiama il nuovo endpoint e crea i segnaposti reali nel fascicolo), il prompt pronto da copiare, output atteso, verifica del revisore. Stile e struttura mutuati da `CardGuidaPanel.tsx`, il pannello "Guida carta" già esistente, per coerenza visiva. |
| `SabUnifiedSidebar.tsx` / `SmartAuditBox2.tsx` | Aggiunge il tab **"Prompt AI"** alla sidebar unificata di Smart Audit Box (accanto a Guida, Controlli/AI, Evidenze, Commenti), che monta `SchedaPromptPanel`. |
| `DmKpiStrip.tsx` / `DocumentGrid.tsx` | Il chip "segnaposti" nella striscia KPI del Document Manager ora è cliccabile: applica il quick filter `segnaposti_vuoti` (esisteva già come filtro selezionabile a mano in `QuickFilterPills`, ma nessuno lo attivava cliccando il numero). |

## Come si usa, end-to-end

1. Il revisore apre una carta in Smart Audit Box (es. `D-01`, Crediti verso soci).
2. Nella sidebar, apre il tab **Prompt AI**: vede la scheda `D-01` della libreria — stessi documenti da allegare, stesso prompt, stessa verifica che sono nel file `prompts/.../D-01.md` di questo repository.
3. Se uno o più documenti non sono ancora disponibili, clicca **"Richiedi documenti mancanti"**: AuditFlow crea un segnaposto per ciascuno, visibile nel Document Manager con lo stesso ciclo di vita già in uso (`atteso → caricato → in_validazione → accettato/respinto`).
4. Il KPI "documenti mancanti" in dashboard e il chip "segnaposti" nel Document Manager ora riflettono correttamente questi segnaposti, e cliccando il chip si arriva dritti all'elenco filtrato.
5. Quando i documenti sono tutti disponibili, il revisore copia il prompt dal pannello e lo usa nell'agente AI in uso, seguendo il flusso già descritto in `01-principi-generali-e-regole-di-utilizzo.md`.

## Verifiche fatte in questa sessione

**Statiche**
- `python -m py_compile` su tutti i file backend toccati.
- Le 177 schede caricate e interrogate con un `FastAPI TestClient` reale (non un mock) — elenco, filtro per fase, filtro testuale, conteggi per fase, lookup per codice carta, tutti con risultati corretti (es. 64 schede in fase "esecuzione", come atteso).
- `npm ci` + `npx tsc --noEmit` sull'intero progetto frontend — nessun errore, incluse le nuove aggiunte.

**End-to-end, con l'app realmente avviata** (backend FastAPI + frontend Vite in locale, database SQLite — la modalità di sviluppo prevista da `backend/database.py`, con `MASTER_API_DISABLED=true` per non dipendere da App_Master, non presente in questo ambiente; un solo modulo del backend, `routers/canonical.py`, richiede il pacchetto privato `revai_core` non disponibile qui — sostituito da uno stub locale non incluso nel commit, solo per permettere l'avvio):
- Creato un incarico e un fascicolo demo con una carta `D-01`; chiamato `GET /api/scheda-prompt/by-cod-carta/D-01` → restituisce la scheda corretta con il testo del prompt integrale.
- Chiamato `POST /api/dm/segnaposti/from-scheda` sulla stessa carta → crea davvero 2 segnaposti nel fascicolo (uno per documento richiesto dalla scheda), verificati come righe reali nel database.
- Rifetchato il KPI `documenti_mancanti` della dashboard: **prima** della correzione avrebbe restituito `n: 0` (il bug), **dopo** restituisce correttamente `n: 2` — confermato sui dati appena creati, non solo per lettura del codice.
- Nel browser (Chromium via Playwright): aperto il Document Manager, verificato che il chip "segnaposti" compare con il conteggio corretto (screenshot), cliccato il chip, verificato che applica il filtro "Segnaposti vuoti" e la griglia si riduce esattamente ai 2 segnaposti creati (screenshot).
- Nel browser: aperto Smart Audit Box sulla carta `D-01`, verificato che il tab "Prompt AI" compare nella sidebar unificata accanto a Guida/Controlli/Evidenze/Commenti e si monta correttamente (screenshot).
- **Trovato e corretto durante questa verifica visiva** (non dal solo typecheck): quando la carta non ha ancora un documento DOCX/XLSX/PDF aperto, il pannello "Prompt AI" restava vuoto invece di mostrare un messaggio — a differenza del pannello "Guida" gemello, che in quel caso mostra "Nessuna guida disponibile". Corretto per coerenza (commit separato, stesso branch).

**Non verificato**: il rendering del pannello "Prompt AI" a pieno con una scheda popolata (documenti, prompt, output atteso, verifica) non è stato controllato visivamente, perché richiede una carta con un documento realmente allegato — l'ambiente di test non aveva file caricati né lo storage a oggetti configurato. La correttezza dei dati che il pannello mostrerebbe è comunque verificata (stesso endpoint testato sopra); resta da confermare solo la resa grafica finale. Comportamento su PostgreSQL (produzione) e test automatici: non verificati, restano da fare su un ambiente con accesso a Postgres/App_Master.

## Limiti e prossimi passi

- Il branch va **rivisto da chi conosce a fondo AuditFlow** prima del merge — in particolare la scelta di creare un nodo/carta/segnaposto per ciascun documento richiesto (invece di un solo segnaposto per l'intera scheda) è una decisione di modellazione che merita conferma rispetto alle convenzioni interne del fascicolo.
- Nessun test automatico (pytest/vitest) è stato aggiunto per il nuovo codice: il progetto ne ha altrove, andrebbero scritti prima del merge.
- Il pannello "Prompt AI" mostra sempre la scheda per il codice carta esatto; non copre ancora i casi in cui AuditFlow è più granulare della libreria (es. le varianti A02-01…A02-10 per tipo di lettera di circolarizzazione, già segnalate come limite in `10-mappatura-auditflow.md`).
- Non è stato collegato al pulsante "Copia prompt" alcun tracciamento nel registro degli utilizzi (§ III.3 di `01-principi-generali-e-regole-di-utilizzo.md`): resta responsabilità del revisore documentare l'uso secondo la formula standard.
