# Playbook operativo — come si usano i prompt in ciascuna fase

Questo file completa [`10-mappatura-auditflow.md`](10-mappatura-auditflow.md): quel documento risponde a "**quale** scheda uso in **quale** fase/sotto-fase", questo risponde a "**in che sequenza** le uso, **cosa** aspettarmi di buono e **a cosa** stare attento" — fase per fase, con lo stesso pattern a due strati che regge tutta la libreria:

> **prompt operativo** (bozza di analisi, Parti 1-4) → verifica del revisore → **prompt memo** (Parte 5, formalizza in carta di lavoro).

Il pattern non cambia mai; cambia solo cosa c'è dentro. Per questo, una volta capito bene su una fase, le altre si leggono in fretta.

---

## 1. Accettazione — 20 schede

**Sotto-fasi AuditFlow:** configurazione preliminare · rischi reputazionali · rischi finanziari · valutazione rischio cliente · autovalutazione del revisore · formalizzazione dell'incarico.

**Sequenza consigliata:**
1. Configurazione preliminare → `A.1.1` (inventario e conformità del fascicolo) + `A05` (PBC, elenco documenti richiesti alla società): si apre l'incarico verificando cosa c'è e cosa manca, prima di qualunque analisi di merito.
2. Valutazione rischio cliente → `A.2.1` profilo dell'entità, `A.2.2` analisi di settore (o `E.1` se il settore non ha benchmark verificabili — vedi § Rischi tipici) → memo `B04`, `B05`.
3. Rischi reputazionali/finanziari e indipendenza → `A.3.1` integrità della direzione, `A.3.2` verifica indipendenza, `A.3.3` incompatibilità e limiti di durata → memo `B02`, `B03`, `B08`/`B09` (questionari accettazione/continuazione).
4. Autovalutazione del revisore → `A.3.4` adeguatezza di competenze e risorse → memo `B06`, `B07`.
5. Formalizzazione → `A.3.5` predisposizione lettera di incarico → memo `B10`, con `B01` (incontro preliminare) a corredo dell'intero processo.

**Dove il prompt aiuta di più:** è la fase con il più alto rapporto tra "checklist da non dimenticare" e "giudizio da esprimere" — l'agente è forte nel garantire che nessun controllo formale (documento mancante, verbale non firmato, capitale sociale disallineato tra visura e statuto) sfugga.

**Rischio tipico da presidiare:** *l'omissione silenziosa* (§ V.2) — un conflitto di interesse o una relazione con parti correlate può essere citata di sfuggita in un verbale tra decine di pagine; il prompt risponde a quello che gli chiedi, non necessariamente segnala quello che non gli hai chiesto di cercare. Su `A.3.1`/`A.3.2` in particolare, la lettura diretta dei verbali resta insostituibile.

---

## 2. Pianificazione — 35 schede

**Sotto-fasi AuditFlow:** strategia · significatività · aree di rischio · piano di revisione/vigilanza (+ sistema di controllo interno).

*(Trattata in dettaglio nella conversazione che ha originato questo file; sintesi qui sotto.)*

**Sequenza consigliata:**
1. Sistema di controllo interno → `A.4.1` ambiente di controllo, `A.4.2` mappatura processi, `A.4.3` controlli IT → memo `C10`, `C11`.
2. Aree di rischio → `A.5.1` analisi comparativa preliminare, `A.5.2` rischi di errore significativo, `A.5.3` rischi di frode (o `E.2` per società a controllo proprietario-amministratore), `A.5.4` parti correlate, `A.5.5` continuità aziendale preliminare → memo `C04`, `C05`, `C06`, `C13`, `C15` (+ `C07`/`C08`/`C09` se c'è un precedente revisore).
3. Significatività → `A.5.6` (o `E.3` per PMI) → memo `C01-C02`.
4. Strategia e piano → `A.5.7`, `A.5.8` → memo `C14` (Planning memo, la sintesi dell'intera fase); `C03` fa da ponte con l'Accettazione se il rischio d'incarico va rivisto.

**Dove il prompt aiuta di più:** struttura la valutazione dei rischi in modo sistematico e ripetibile — stessa griglia di analisi ogni incarico, meno probabilità di dimenticare un'asserzione o un ciclo.

**Rischio tipico da presidiare:** *la generalizzazione che sembra specifica* — con i dati reali del cliente già caricati, è facile ottenere una lista di rischi "plausibile" che in realtà andrebbe bene per qualunque azienda del settore. Su `A.5.2`/`A.5.3` in particolare, usa la tecnica del disaccordo forzato (§ I.6): *"questo rischio cambierebbe se cambiasse la società? Se no, scartalo."*

---

## 3. Esecuzione — 64 schede (la più grande)

**Sotto-fasi AuditFlow:** procedure analitiche · test sui crediti · circolarizzazione · verifica delle rimanenze, più **una sotto-fase per ciascuna area di bilancio** (crediti, immobilizzazioni, debiti, fondi rischi, ecc. — vedi la tabella completa in `10-mappatura-auditflow.md`, sezione 3).

**Sequenza consigliata (per ogni area di bilancio):**
1. Apertura → `3.A` (`C.1.1` conformità fascicolo bilancio, `C.1.2` aggiornamento significatività e rischi) — si fa **una volta sola** all'inizio della fase, non per ogni voce.
2. Per ciascuna voce di stato patrimoniale o conto economico → il prompt operativo corrispondente in `3.B` (`C.2.1`…`C.2.10`) o `3.C` (`C.3.1`…`C.3.6`), eventualmente affiancato dal prompt OIC in `4.F` se la voce richiede un test tecnico specifico (riduzione di valore, rilevazione ricavi, derivati, ammortamenti, fondi/TFR).
3. Se la voce richiede campionamento, test dei controlli o conferme esterne → `4.A` (`D.1.1`…`D.1.4`) si applica trasversalmente, non è legato a una singola voce.
4. Situazioni particolari (saldi di apertura, gruppi, lavoro di esperti/internal audit/fornitori esterni) → `4.B` (`D.2.1`…`D.2.8`), quando ricorrono.
5. Una volta verificata l'analisi → il memo `5.D` con lo **stesso nome dell'area di bilancio** (es. voce "Crediti verso soci" → `D-01`) formalizza il lavoro; `A01` (mapping bilancio di verifica) tiene la riconciliazione trasversale, `A02`/`A06` gestiscono le lettere di circolarizzazione e il relativo registro.

**Dove il prompt aiuta di più:** è la fase a più alto volume e più ripetitiva — stessa struttura di analisi su decine di voci per decine di incarichi l'anno. È qui che il risparmio di tempo aggregato è maggiore, ed è anche il motivo per cui ogni scheda porta il blocco "Documenti disponibili/non disponibili" nell'app: su 64 schede, sapere subito su quali puoi procedere e su quali no evita di scoprirlo a metà lavoro.

**Rischio tipico da presidiare:** *il calcolo corretto sul dato sbagliato* — su ricalcoli (ammortamenti, interessi, TFR) il prompt esegue i passaggi in modo impeccabile ma su un input che può essere stato letto dalla colonna sbagliata o dal periodo sbagliato; l'Allegato B (`08-regole-di-verifica-per-tipologia-di-output.md`) impone di verificare sempre l'input prima del procedimento, non solo il risultato.

---

## 4. Completamento — 29 schede

**Sotto-fasi AuditFlow:** eventi successivi · attestazione della direzione · riesame finale · riesame della qualità (solo società di revisione).

**Sequenza consigliata:**
1. Aree di giudizio → `3.D`: `C.4.1` stime contabili, `C.4.2` continuità aziendale finale (o `E.7` con scadenzario e stress delle assunzioni), `C.4.3` eventi successivi, `C.4.4` nota integrativa, `C.4.5` relazione sulla gestione, `C.4.6` rendiconto finanziario, `C.4.7` attestazione della direzione, `C.4.8` riepilogo errori (o `E.10` per il prospetto), `C.4.9` procedure analitiche finali.
2. Conformità e obblighi del revisore → `4.C` (`D.3.1`…`D.3.5`): leggi/regolamenti, antiriciclaggio, aspetti chiave della revisione, coerenza delle altre informazioni, eventi successivi all'emissione.
3. Autovalutazione e riesame → `C.4.12` (o `E.8`, che simula il riesame della qualità) e, se lo Studio è una società di revisione, `4.G` (`G.1` supporto al responsabile del riesame, `G.2` completezza del fascicolo).
4. Formalizza con i memo `5.E` (`E01`…`E09`).

**Dove il prompt aiuta di più:** tiene insieme in un'unica sequenza coerente aree molto eterogenee (stime, continuità, eventi successivi, nota integrativa) che altrimenti si affrontano in ordine sparso; utile anche come checklist di completezza prima della chiusura.

**Rischio tipico da presidiare:** *la conferma compiacente* (§ V.2) — è il rischio più alto di tutta la libreria su `C.4.2` (continuità aziendale) e `C.4.1` (stime): il modello tende ad assecondare l'ipotesi già formulata dal revisore invece di metterla sotto stress. Qui la tecnica del disaccordo forzato non è opzionale: *"argomenta contro la mia conclusione di continuità aziendale, qual è l'obiezione più forte che un riesaminatore della qualità potrebbe sollevare?"* — e la verifica va sempre fatta ponendo la stessa domanda anche in senso opposto, in una sessione separata.

---

## 5. Verifiche periodiche — 22 schede

**Sotto-fase AuditFlow:** verifiche periodiche (unica, ma ricorrente più volte l'anno).

**Sequenza consigliata:**
1. Apertura della singola verifica → `2.A` (`B.1.1` controllo di conformità periodica, `B.1.2` riscontro risultanze verifica precedente).
2. Regolarità formale → `2.B` (`B.2.1`…`B.2.3`: libri obbligatori, registrazioni contabili, quadratura bilancio di verifica).
3. Cicli operativi → `2.C` (`B.3.1`…`B.3.9`, uno per ciclo: liquidità, attivo/crediti, passivo/debiti, magazzino, personale, tributario, immobilizzazioni, finanziamenti, cassa) — eventualmente con le varianti `E.4` (test esteso su fatture elettroniche) ed `E.5` (scadenzario versamenti).
4. Analisi trasversali e chiusura → `2.D` (`B.4.1`…`B.4.3`: analisi comparativa di periodo, indicatori di crisi, verbale di verifica).
5. Formalizza con `5.F` (`F01` programma, `F02` adempimenti fiscali, `F03` checklist).

**Dove il prompt aiuta di più:** è la fase più ricorrente nel tempo (trimestrale o comunque infra-annuale) — la standardizzazione del programma (`F01`) e della checklist (`F03`) rende ogni verifica confrontabile con la precedente, un valore che cresce nel tempo più che nel singolo utilizzo.

**Rischio tipico da presidiare:** proprio perché è ripetitiva, è la fase dove ci si abitua di più e si allenta la verifica — la checklist rapida (§ I.10 in `01-principi-generali-e-regole-di-utilizzo.md`) va tenuta stretta qui più che altrove, non meno.

---

## 6. Chiusura e stampa fascicolo — 3 schede

**Sotto-fasi AuditFlow:** bozza della relazione · approvazione e firma.

**Sequenza consigliata:**
1. `C.4.10` predisposizione della relazione di revisione (in AuditFlow scomposta nelle varianti di giudizio: senza modifica, con rilievi, con rilievi e limitazioni, impossibilità per incertezze o per limitazioni, giudizio negativo — la scheda `A03`/`C.4.10` copre il caso generale, personalizza per la variante specifica).
2. `C.4.11` comunicazione finale agli organi di governance.
3. Approvazione e firma — fuori dal perimetro dei prompt: nessuna scheda genera o modifica il giudizio, per policy (§ I.3, "usi vietati": *redigere la relazione di revisione o parti che ne modificano il giudizio*).

**Dove il prompt aiuta di più:** solo sulla forma — mette in formato professionale un giudizio che il revisore ha già deciso, non lo determina.

**Rischio tipico da presidiare:** *il riferimento inventato*, il più insidioso di tutti (§ V.2) — sulle formule standard di giudizio un riferimento normativo enunciato con sicurezza ma leggermente impreciso è il tipo di errore che più facilmente supera una lettura superficiale proprio perché il testo "suona" professionale.

---

## Trasversale — 4 schede

`G01`/`G02` (indice e scheda del permanent file) non sono legate a un momento preciso dell'incarico ma vanno aggiornate ogni volta che qualcosa di rilevanza pluriennale cambia (organi sociali, contratti quadro, policy). Le due note (`5.H`: nota al fascicolo su una questione aperta, nota di sintesi per il responsabile) si usano in qualunque fase quando serve mettere per iscritto un punto aperto o una sintesi per chi supervisiona, senza aspettare la formalizzazione della fase in corso.

---

## Nota di metodo

Questo playbook riflette la sequenza **tipica**; non è un vincolo procedurale. Il revisore resta libero di saltare, anticipare o ripetere una scheda in base alle specificità dell'incarico — la sequenza serve a non perdere passaggi la prima volta che si usa la libreria su una fase, non a sostituire il giudizio professionale su cosa serve davvero in quel caso concreto.
