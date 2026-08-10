# Sezione I — Principi generali e regole di utilizzo

> Ambito. Lo strumento di intelligenza artificiale in uso nello Studio è un agente dedicato, preconfigurato per singola azienda e assegnato a un singolo team di revisione. Non è ammesso l'uso di strumenti di AI generalisti sull'incarico: l'agente dedicato è l'unico strumento consentito. Le regole che seguono ne governano l'utilizzo in ogni fase della revisione; la configurazione, il perimetro e la funzione di blocco sono trattati in [`02-configurazione-agente-e-limiti.md`](02-configurazione-agente-e-limiti.md), la riservatezza e la protezione dei dati in [`04-riservatezza-e-quadro-normativo.md`](04-riservatezza-e-quadro-normativo.md).

## I.1 Principio fondamentale

L'agente **non è una fonte di evidenza di revisione** e **non esegue procedure di revisione**.

È uno strumento di supporto alla redazione, all'analisi e al ragionamento del revisore. Ogni output prodotto dall'agente è, a tutti gli effetti, una bozza non verificata. L'evidenza di revisione resta quella ottenuta dalle procedure svolte dal revisore su documentazione della società e da fonti indipendenti.

Tre conseguenze non negoziabili:

- La responsabilità professionale non è delegabile. Il revisore che firma la carta di lavoro risponde del contenuto, indipendentemente da come è stato prodotto.
- Nessun output entra in una carta di lavoro senza verifica documentata (§ I.7).
- Lo scetticismo professionale si applica anche all'AI. Un testo ben scritto e sicuro di sé non è per questo corretto.

## I.2 Riservatezza, perimetro e segregazione per azienda e per team

L'agente opera in perimetro chiuso: i dati dell'incarico non sono utilizzati per addestrare modelli né conservati oltre quanto necessario all'incarico (vedi [`04-riservatezza-e-quadro-normativo.md`](04-riservatezza-e-quadro-normativo.md)). Poiché l'agente tratta i dati reali della società, la riservatezza si presidia con regole di assegnazione e di segregazione, non con l'anonimizzazione dei contenuti.

Regole di assegnazione e di segregazione:

- **Un'istanza per azienda.** Ogni agente è preconfigurato su una singola società: non utilizzarlo per un'altra azienda e non caricarvi documenti che non appartengono a quella società.
- **Un'istanza per team.** L'accesso è riservato al team di revisione assegnato all'incarico; le credenziali sono personali e non si condividono.
- **Nessun travaso tra istanze.** Non spostare documenti, prompt o output da un'istanza all'altra: ogni fascicolo resta nel proprio perimetro.
- **Nessun uso fuori perimetro.** Non trasferire in strumenti esterni — posta, chat, altri servizi di AI — contenuti tratti dall'agente.
- **Restrizioni del cliente.** Se il cliente ha posto limiti contrattuali all'uso di AI sull'incarico, questi prevalgono: verificarli prima dell'utilizzo.

> Il perimetro chiuso riduce il rischio di riservatezza ma sposta il rischio sull'eccessivo affidamento: un output costruito sui dati reali dell'incarico appare convincente proprio perché contestualizzato.

## I.3 Usi ammessi e usi vietati

### Ammessi

- Redazione di bozze di memo, verbali interni, comunicazioni
- Riformulazione e sintesi di testi già prodotti dal revisore
- Brainstorming di rischi, ipotesi di frode, procedure alternative
- Spiegazione di principi contabili e di revisione a fini formativi
- Generazione di formule Excel, script di analisi dati, query
- Traduzione e revisione linguistica di documentazione
- Predisposizione di checklist e strutture di carte di lavoro
- Confronto logico tra testi (es. due versioni di un contratto)
- Supporto alla verbalizzazione di ragionamenti tecnici già maturati

### Vietati

- Determinare conclusioni di revisione o giudizi
- Calcolare la materialità o dimensionare campioni come output finale
- Produrre riferimenti normativi da inserire senza verifica sulla fonte
- Valutare la ragionevolezza di stime contabili in luogo del revisore
- Redigere la relazione di revisione o parti che ne modificano il giudizio
- Sostituire l'interrogazione della direzione o le procedure di conferma esterna
- Generare dati, tabelle o riconciliazioni che appaiano come evidenza
- Qualunque utilizzo su incarichi ove il cliente lo abbia contrattualmente escluso

## I.4 Come si costruisce un prompt efficace

L'agente dispone del fascicolo dell'incarico, ma la qualità dell'output dipende comunque da come è formulata la richiesta. Anche con il contesto già caricato, un prompt efficace esplicita ruolo, compito, vincoli e formato attesi.

Struttura **R-C-C-V-F**:

| Elemento | Cosa scrivere |
| --- | --- |
| Ruolo | Chi deve simulare di essere il modello e con quale livello di seniority |
| Contesto | Settore, dimensione (in ordini di grandezza), fase dell'incarico, framework contabile |
| Compito | Un solo obiettivo, espresso con un verbo operativo |
| Vincoli | Cosa non fare, limiti di lunghezza, cosa non inventare |
| Formato | Tabella, elenco, memo, numero di elementi attesi |

**Vincolo anti-allucinazione da inserire sempre**, in coda a ogni prompt che tocchi materia tecnica (nella libreria operativa è già incorporato in ogni scheda, vedi la sezione "Prompt" di ciascuna):

> "Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu."

**Esempio — debole vs. efficace:**

- *Debole:* "Aiutami con l'analisi dei ricavi."
- *Efficace:* "Sei un manager di revisione con esperienza nel settore manifatturiero. Contesto: sto pianificando le procedure sui ricavi di una società industriale che vende a distributori con resi contrattualmente ammessi e premi di fine anno legati a volumi. Framework contabile italiano. Ricavi nell'ordine dei 50 milioni. Compito: elencami i rischi di errore significativo sui ricavi specifici di questo modello di business, distinguendo per asserzione. Vincoli: non citare numeri di paragrafo. Concentrati sui rischi che derivano dal modello contrattuale descritto, non su rischi generici validi per qualunque azienda. Formato: tabella con colonne Rischio | Asserzione interessata | Perché è specifico di questo contesto."

## I.5 Libreria dei prompt operativi

La libreria operativa (cartella [`../prompts/`](../prompts/)) non è generica: ogni scheda è agganciata alla specifica carta di lavoro del modello adottato dallo Studio che l'agente compila in bozza. Si utilizza quella, sui documenti reali dell'incarico caricati nell'agente, e non prompt generici su dati anonimizzati.

## I.6 Tecniche avanzate

- **Iterare invece di ripartire.** Se l'output non convince, non riformulare da zero: spiegare cosa non va. *"Questa risposta è troppo generica, vale per qualunque azienda. Concentrati solo su ciò che deriva dal fatto che i clienti hanno diritto di reso."*
- **Forzare il disaccordo.** I modelli tendono ad assecondare. Contromisura: *"Argomenta contro la mia conclusione. Qual è l'obiezione più forte che un revisore della qualità potrebbe sollevare?"*
- **Chiedere il livello di confidenza.** *"Per ciascun punto indica se è un dato consolidato, una tua inferenza o un'ipotesi."*
- **Non fidarsi della conferma.** Chiedere "sei sicuro?" produce spesso una correzione compiacente, non più accurata. La verifica si fa sulla fonte, non sul modello.
- **Un'istanza per azienda e per team.** Non riutilizzare l'istanza di una società per un'altra: la separazione dei contesti è garantita dalla configurazione dedicata dello strumento.

## I.7 Procedura di verifica obbligatoria

Nessun contenuto generato da AI entra in una carta di lavoro senza il passaggio seguente.

| # | Controllo | Come |
| --- | --- | --- |
| 1 | Fonti | Ogni riferimento normativo, principio, paragrafo o dato citato è verificato sul documento originale. I riferimenti non verificabili si eliminano. |
| 2 | Calcoli | Ogni operazione aritmetica è ricalcolata autonomamente. |
| 3 | Coerenza con l'incarico | Il contenuto riflette i fatti effettivi del cliente, non una ricostruzione plausibile ma generica. |
| 4 | Completezza | Sono stati omessi aspetti rilevanti che il revisore conosce e il modello no? |
| 5 | Conclusioni | Le conclusioni sono state formulate dal revisore, non recepite dall'output. |
| 6 | Riservatezza a ritroso | Nulla di riservato è stato inserito nel prompt oltre quanto necessario. |

Il revisore che appone la propria firma sulla carta di lavoro attesta implicitamente di aver eseguito questa verifica.

## I.8 Documentazione nelle carte di lavoro

La documentazione deve consentire a un revisore esperto e indipendente di comprendere il lavoro svolto. Ciò richiede che l'utilizzo dell'AI sia tracciato.

**Da documentare:** l'indicazione che lo strumento è stato utilizzato e per quale attività; la natura dell'utilizzo (bozza redazionale, brainstorming, supporto analitico); le verifiche svolte sull'output e i loro esiti; la fonte primaria su cui ogni elemento tecnico è stato riscontrato.

**Da non documentare:** trascrizioni integrali delle conversazioni, che appesantiscono il fascicolo senza aggiungere evidenza.

**Formula standard** (vedi anche [`09-modulistica.md`](09-modulistica.md)):

> "La presente analisi è stata redatta con il supporto dell'agente AI di revisione in fase di [strutturazione della bozza / generazione di ipotesi]. I contenuti tecnici sono stati verificati su [fonte primaria]; i calcoli sono stati rieseguiti autonomamente. Le valutazioni e le conclusioni sono del sottoscritto revisore."

## I.9 Segnali di allarme

Interrompere e verificare quando l'output presenta:

- riferimenti troppo precisi: numeri di paragrafo, articoli, sentenze citati con sicurezza — è il pattern di allucinazione più comune e più insidioso;
- statistiche o benchmark di settore senza fonte verificabile;
- assenza totale di dubbio su una questione che il revisore sa essere controversa;
- conferma immediata di un'ipotesi appena avanzata dal revisore;
- testo che "suona" perfettamente professionale ma non contiene alcun elemento specifico dell'incarico;
- coerenza apparente tra parti di un documento lungo che, riletto, presenta contraddizioni interne.

## I.10 Checklist rapida da tenere alla scrivania

**Prima**
- [ ] Sto usando l'istanza dell'agente assegnata a questa società e al mio team?
- [ ] Il cliente ha posto restrizioni contrattuali all'uso di AI?
- [ ] Il compito rientra tra gli usi ammessi?
- [ ] Ho allegato i documenti-fonte richiesti dalla scheda?

**Durante**
- [ ] Ho fornito ruolo, contesto, compito, vincoli e formato?
- [ ] Ho inserito il vincolo anti-allucinazione?
- [ ] Sto verificando l'output mentre lo leggo, non dopo?

**Dopo**
- [ ] Ho verificato ogni fonte su documento originale?
- [ ] Ho ricalcolato ogni operazione aritmetica?
- [ ] Ho documentato l'utilizzo secondo la formula standard?
- [ ] Le conclusioni riportate sono le mie, non quelle dell'agente?

## I.11 Escalation

In caso di dubbio sull'affidabilità di un output, sul rispetto del perimetro o su un possibile incidente, il caso va segnalato secondo la procedura di [`03-governance-qualita-e-monitoraggio.md`](03-governance-qualita-e-monitoraggio.md) (§ Gestione degli incidenti) prima di proseguire l'utilizzo sull'area interessata.
