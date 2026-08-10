# Mappatura con le fasi AuditFlow

AuditFlow è il gestionale di incarico usato dallo Studio. Ogni incarico vi attraversa **6 fasi ISA**, in quest'ordine:

1. **Accettazione** (o "Mantenimento dell'incarico" dal secondo anno)
2. **Pianificazione**
3. **Esecuzione**
4. **Completamento**
5. **Verifiche periodiche**
6. **Chiusura e stampa fascicolo**

Ogni fase si articola in sotto-fasi (es. Accettazione → *configurazione preliminare, indipendenza e incompatibilità, valutazione del rischio cliente, formalizzazione dell'incarico*; Esecuzione → una sotto-fase per ciascuna area di bilancio: crediti, immobilizzazioni, debiti, fondi rischi, ecc.). Questo documento mappa **ogni scheda di [`../prompts/`](../prompts/) sulla fase AuditFlow in cui va usata**, così puoi aprire l'app master, filtrare per fase, e trovare subito i prompt pertinenti a dove sei nel fascicolo.

Questa mappatura è marcata anche nei dati dell'app (badge "Fase AuditFlow" su ogni scheda) e in cima a ciascun file `.md` della libreria.

## Come si usa in pratica

1. In AuditFlow, apri l'incarico e guarda in quale fase/sotto-fase ti trovi (breadcrumb delle 6 fasi nella Dashboard Incarico).
2. Nell'app master della libreria ([`../app/index.html`](../app/index.html)), filtra per la fase corrispondente (chip in alto).
3. Scegli la scheda pertinente all'area/sotto-fase specifica su cui stai lavorando (es. in Esecuzione, sotto-fase "Crediti verso soci" → scheda `D-01`).
4. Segui il flusso normale della scheda (documenti da allegare → prompt → verifica del revisore) descritto in [`01-principi-generali-e-regole-di-utilizzo.md`](01-principi-generali-e-regole-di-utilizzo.md).

## Fase per fase

### 1. Accettazione — 20 schede

Sotto-fasi AuditFlow: *configurazione preliminare, rischi reputazionali, rischi finanziari, valutazione rischio cliente, autovalutazione del revisore, formalizzazione dell'incarico.*

| Sotto-fase AuditFlow | Schede della libreria |
| --- | --- |
| Configurazione preliminare | `1.A` — A.1.1 (Inventario e conformità del fascicolo) |
| Valutazione rischio cliente | `1.B` — A.2.1, A.2.2 (profilo dell'entità, analisi di settore) |
| Rischi reputazionali / indipendenza / autovalutazione / formalizzazione | `1.C` — A.3.1 … A.3.5 (integrità direzione, indipendenza, incompatibilità, competenze e risorse, lettera di incarico) |
| PBC (documenti richiesti) | `5.A` — A05 |
| Memo di accettazione | `5.B` — B01 … B10 (incontro preliminare, attestazione/verifica indipendenza, memorandum, valutazione organizzativa, stima ore, questionari accettazione/continuazione, lettera di incarico) |
| Variante | `4.E` — E.1 (analisi di settore senza benchmark inventati) |

`5.B` corrisponde **esattamente**, codice per codice, alle carte di lavoro B01–B10 di AuditFlow (stessa numerazione, stesso contenuto).

### 2. Pianificazione — 35 schede

Sotto-fasi AuditFlow: *strategia, significatività, aree di rischio, piano di revisione/vigilanza* (+ *sistema di controllo interno*, gestito come approfondimento della pianificazione).

| Sotto-fase AuditFlow | Schede della libreria |
| --- | --- |
| Sistema di controllo interno | `1.D` — A.4.1, A.4.2, A.4.3 (ambiente di controllo, mappatura processi, controlli IT) |
| Aree di rischio / significatività / strategia | `1.E` — A.5.1 … A.5.8 (analisi comparativa preliminare, rischi di errore, rischi di frode, parti correlate, continuità aziendale preliminare, significatività, strategia e piano, comunicazioni iniziali) |
| Nano-imprese/PMI (approccio proporzionato) | `4.D` — D.4.1 … D.4.8 |
| Memo di pianificazione | `5.C` — C01-C02 … C15 |
| Varianti | `4.E` — E.2, E.3 (rischi di frode e significatività per imprese minori) |

`5.C` corrisponde **quasi esattamente** alle carte C01–C15 di AuditFlow: stesso contenuto per C04 (rischio frode), C05 (controlli antifrode libro giornale), C06 (analisi comparativa preliminare), C07 (incontro precedente revisore), C08/C09 (manleva), C10 (questionario SCI), C11 (sistemi IT), C12 (servizi da fornitore esterno), C13 (valutazione rischi), C14 (planning memo), C15 (parti correlate). Unica differenza: AuditFlow scompone la significatività preliminare in tre varianti di formato (C01 Excel, C01.2 Word, C02 narrativo); la libreria la tratta come un'unica scheda `C01-C02`.

### 3. Esecuzione — 64 schede

Sotto-fasi AuditFlow: *procedure analitiche, test sui crediti, circolarizzazione, verifica delle rimanenze*, più **una sotto-fase per ciascuna area di bilancio** generata dinamicamente nel fascicolo (crediti verso soci, immobilizzazioni immateriali/materiali/finanziarie, rimanenze, cassa e banche, patrimonio netto, fondi rischi, TFR, debiti, ratei e risconti, ecc.).

| Sotto-fase AuditFlow | Schede della libreria |
| --- | --- |
| Apertura fase di bilancio / procedure analitiche | `3.A` — C.1.1, C.1.2 |
| Una sotto-fase per voce di stato patrimoniale | `3.B` — C.2.1 … C.2.10 |
| Voci di conto economico | `3.C` — C.3.1 … C.3.6 |
| Campionamento / test dei controlli / circolarizzazione | `4.A` — D.1.1 … D.1.4 |
| Situazioni particolari (gruppi, esperti, fornitori esterni) | `4.B` — D.2.1 … D.2.8 |
| Supporto contabile per voce (OIC) | `4.F` — F.1 … F.5 |
| Memo per singola voce di bilancio | `5.D` — D-01 … D-24 |
| Mapping bilancio di verifica / circolarizzazioni | `5.A` — A01, A02, A06 |
| Varianti | `4.E` — E.4, E.5, E.6, E.9 |

`5.D` (D-01…D-24) è la sezione con la corrispondenza più diretta e più utile: **ogni codice coincide con la sotto-fase "area di bilancio" che AuditFlow crea automaticamente in Esecuzione** (es. D-01 Crediti verso soci ↔ sotto-fase "Crediti verso soci"; D-17 Fondi rischi e oneri ↔ sotto-fase "Fondi rischi e oneri"; D-21 Debiti verso fornitori ↔ sotto-fase "Debiti verso fornitori"). Quando apri in AuditFlow una di quelle sotto-fasi, la scheda `5.D` con lo stesso nome è il memo da compilare a valle del lavoro fatto con `3.B`/`3.C`/`4.F`.

### 4. Completamento — 29 schede

Sotto-fasi AuditFlow: *eventi successivi, attestazione della direzione, riesame finale, riesame della qualità (solo società di revisione).*

| Sotto-fase AuditFlow | Schede della libreria |
| --- | --- |
| Aree di giudizio (stime, continuità, eventi successivi, nota integrativa, rendiconto, errori, autovalutazione) | `3.D` — C.4.1 … C.4.9, C.4.12 |
| Conformità normativa e obblighi del revisore | `4.C` — D.3.1 … D.3.5 |
| Controllo di qualità e riesame | `4.G` — G.1, G.2 |
| Memo di completamento | `5.E` — E01 … E09 |
| Varianti | `4.E` — E.7, E.8, E.10 |

`5.E` corrisponde da vicino alle carte E01–E08 di AuditFlow (significatività definitiva, analisi comparativa finale, conferma del risk assessment, riepilogo errori, continuità aziendale, checklist nota integrativa, eventi successivi, lettera di attestazione), con uno scarto di numerazione dopo E06: dove AuditFlow ha E07 "Eventi successivi" ed E08 "Lettera di attestazione", la libreria intercala E07 "Checklist della relazione sulla gestione" ed E08 "Completamento dell'audit" prima di E09 "Lettera di attestazione". Il contenuto è comunque tutto presente; verifica solo il codice esatto sulla carta AuditFlow che stai compilando prima di citare il codice nel memo.

### 5. Verifiche periodiche — 22 schede

Corrisponde integralmente alla fase AuditFlow "Verifiche periodiche".

| Schede della libreria |
| --- |
| `2.A` … `2.D` — B.1.1 … B.4.3 (apertura verifica, regolarità formale, cicli operativi, analisi trasversali e chiusura) |
| `5.F` — F01, F02, F03 (programma, adempimenti fiscali, checklist) — **corrispondenza esatta**, stessi codici di AuditFlow |
| Varianti | `4.E` — E.4, E.5 (già citate anche in Esecuzione: riguardano ciclo attivo e adempimenti tributari verificati in sede periodica) |

### 6. Chiusura e stampa fascicolo — 3 schede

| Schede della libreria |
| --- |
| `3.D` — C.4.10 (predisposizione della relazione di revisione), C.4.11 (comunicazione finale agli organi di governance) |
| `5.A` — A03 (modelli di relazione di revisione — in AuditFlow scomposti nelle 6 varianti di giudizio A03-01…A03-06: senza modifica, con rilievi, con rilievi e limitazioni, impossibilità di giudizio per incertezze o per limitazioni, giudizio negativo) |

### Trasversale — 4 schede

Non legate a una fase specifica dell'incarico in corso, ma a materiale che accompagna il fascicolo nel tempo o note generiche:

- `5.G` — G01, G02 (indice e scheda del permanent file)
- `5.H` — Nota al fascicolo su una questione aperta, Nota di sintesi per il responsabile dell'incarico

## Limiti di questa mappatura

- È una mappatura **di raccordo**, costruita confrontando la struttura Parte/Fase della libreria con `backend/seed_catalog.py`, `backend/services/fascicolo_phase_structure.py` e l'indice delle carte di lavoro in `docs/corpus_rag/manuale_cndcec_2025/WP/` del codice sorgente di AuditFlow: non è generata automaticamente dal software e va aggiornata se la struttura delle fasi in AuditFlow cambia.
- Alcune schede sono utili in più di una fase (es. le varianti "situazioni particolari" del 4.B); la fase indicata è quella prevalente.
- Dove AuditFlow scompone una scheda della libreria in più varianti (es. A02 → 10 lettere per tipo destinatario A02-01…A02-10; A03 → 6 varianti di giudizio A03-01…A03-06; C01/C02 → tre formati), la libreria mantiene una scheda unica più generale: personalizza il prompt indicando la variante specifica che ti serve.
