# Sezione V — Formazione e riconoscimento degli errori

## V.1 Percorso formativo obbligatorio

Nessun componente del team utilizza l'agente prima di aver completato il percorso e superato la verifica finale.

| Modulo | Contenuto | Destinatari |
| --- | --- | --- |
| 1. Fondamenti | Cosa è e cosa non è un sistema di AI generativa; perché produce output plausibili ma errati; cosa significa che l'output non è evidenza | Tutti |
| 2. Perimetro e regole | [`01-principi-generali-e-regole-di-utilizzo.md`](01-principi-generali-e-regole-di-utilizzo.md) e [`02-configurazione-agente-e-limiti.md`](02-configurazione-agente-e-limiti.md); la funzione di blocco e i suoi limiti; livelli di autorizzazione | Tutti |
| 3. Costruzione dei prompt | Struttura R-C-C-V-F; utilizzo della libreria; personalizzazione delle schede | Tutti |
| 4. Verifica dell'output | [`08-regole-di-verifica-per-tipologia-di-output.md`](08-regole-di-verifica-per-tipologia-di-output.md); esercizi di individuazione degli errori su casi predisposti | Tutti |
| 5. Documentazione | Come tracciare l'utilizzo in carta di lavoro; registro degli utilizzi | Tutti |
| 6. Aree critiche | Schede su frode, continuità, stime, indipendenza, gruppi | Livello intermedio e avanzato |
| 7. Governance | [`03-governance-qualita-e-monitoraggio.md`](03-governance-qualita-e-monitoraggio.md) e [`04-riservatezza-e-quadro-normativo.md`](04-riservatezza-e-quadro-normativo.md); gestione degli incidenti | Livello avanzato |

Aggiornamento annuale obbligatorio, con illustrazione degli incidenti dell'anno e delle modifiche alla configurazione.

## V.2 Errori tipici: come si presentano e come si riconoscono

Questa è la parte da leggere più di una volta. Gli errori di un sistema di AI non assomigliano agli errori umani: non sono distratti, sono coerenti e ben esposti.

### Il riferimento inventato

- **Come si presenta.** L'agente cita un numero di paragrafo, un articolo, una circolare o una massima con precisione apparentemente rigorosa. Il riferimento è plausibile per numerazione e collocazione, ma non esiste o riguarda altro.
- **Perché è insidioso.** La precisione è essa stessa il segnale d'allarme, ma opera in senso opposto: un riferimento puntuale genera fiducia. È l'errore che più frequentemente supera la verifica.
- **Come si riconosce.** Non si riconosce: si verifica. Ogni riferimento va riscontrato sul testo. In caso di dubbio, si elimina.

### La ricostruzione plausibile del dato mancante

- **Come si presenta.** Un documento non è stato caricato o è illeggibile. Anziché segnalarlo, l'agente colma la lacuna con un valore coerente con il resto: un saldo che quadra, una percentuale ragionevole, una data compatibile.
- **Perché è insidioso.** Il dato non stona. Quadra con gli altri, perché è stato costruito per quadrare.
- **Come si riconosce.** Verificando che ogni dato riportato abbia un documento di origine indicato. Un output che non traccia le fonti va rifiutato e richiesto nuovamente.

### La conferma compiacente

- **Come si presenta.** Si formula un'ipotesi e l'agente la conferma. Si esprime un dubbio su quella conferma e l'agente si corregge, confermando il dubbio.
- **Perché è insidioso.** Produce l'impressione di un confronto critico laddove vi è solo adattamento alla direzione impressa dall'interlocutore.
- **Come si riconosce.** Ponendo la stessa domanda in senso opposto in una sessione separata. Se l'agente conferma entrambe le versioni, nessuna delle due è informativa.

### La generalizzazione che sembra specifica

- **Come si presenta.** Un elenco di rischi, procedure o osservazioni che si legge come pertinente ma vale per qualunque società del settore.
- **Perché è insidioso.** Passa la verifica di plausibilità perché è plausibile. Non aggiunge nulla e occupa lo spazio dell'analisi che non è stata svolta.
- **Come si riconosce.** Chiedendosi: questo elemento cambierebbe se cambiasse la società? Se no, va scartato.

### Il calcolo corretto sul dato sbagliato

- **Come si presenta.** Un ricalcolo esposto con precisione, con passaggi verificabili e risultato aritmeticamente esatto, condotto su un dato di input errato — letto male, tratto dalla colonna sbagliata, riferito a un periodo diverso.
- **Perché è insidioso.** La verifica si concentra sul calcolo, che è corretto, e non sull'input.
- **Come si riconosce.** Verificando sempre l'input prima del procedimento.

### L'omissione silenziosa

- **Come si presenta.** L'output risponde alla domanda posta ma tralascia un elemento rilevante presente nella documentazione, senza segnalarlo.
- **Perché è insidioso.** Nulla nell'output indica la lacuna. È l'errore più difficile da individuare, perché richiede di conoscere già la risposta.
- **Come si riconosce.** È la ragione per cui l'agente non può sostituire la lettura dei documenti da parte del revisore. La lettura diretta resta l'unica difesa.

### La coerenza apparente sul testo lungo

- **Come si presenta.** Un documento articolato che, riletto integralmente, contiene affermazioni tra loro incompatibili in punti distanti.
- **Perché è insidioso.** Ciascun passaggio, letto isolatamente, è corretto.
- **Come si riconosce.** Rileggendo il documento per intero e non a sezioni.

## V.3 Esercizi di verifica finale

La verifica di superamento del percorso formativo si compone di:

- **Individuazione degli errori.** Al candidato sono sottoposti cinque output predisposti contenenti errori delle tipologie di cui al § V.2. È richiesto di individuarli e classificarli.
- **Costruzione di un prompt.** È assegnata una procedura di revisione e richiesta la costruzione del prompt corrispondente secondo la struttura R-C-C-V-F, con individuazione dei documenti da allegare.
- **Verifica di un output.** È sottoposto un output ed è richiesto di descrivere le verifiche necessarie prima del suo utilizzo in carta di lavoro, con indicazione delle fonti di riscontro.
- **Documentazione.** È richiesta la redazione della sezione di carta di lavoro che documenta l'utilizzo dell'agente per una procedura assegnata.

Il mancato superamento comporta la ripetizione del percorso e l'inibizione all'utilizzo nel frattempo.
