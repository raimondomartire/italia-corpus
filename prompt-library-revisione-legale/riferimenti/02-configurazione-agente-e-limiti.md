# Sezione II — L'agente dedicato: configurazione, perimetro e limiti

## II.1 Configurazione e perimetro dell'agente

L'agente è preconfigurato per singola azienda e assegnato a un singolo team. Ne discendono le seguenti caratteristiche operative:

- opera in perimetro chiuso sulla documentazione dell'incarico: ragione sociale, importi reali, nomi delle persone e documenti integrali sono trattati nativamente;
- il caricamento documentale è la modalità operativa ordinaria, non un'eccezione;
- il contesto dell'incarico è già disponibile all'agente e non va ricostruito a ogni prompt.

## II.2 Cosa non cambia, e va ribadito con maggiore forza

Il perimetro chiuso riduce il rischio di riservatezza ma aumenta il rischio di eccessivo affidamento. Un agente che conosce il fascicolo produce output plausibili e contestualizzati: proprio per questo gli errori diventano più difficili da individuare.

Restano integralmente validi:

- L'output non è evidenza di revisione. L'evidenza è il documento sottostante, che il revisore deve avere esaminato.
- Le conclusioni sono del revisore. L'agente non conclude, non giudica l'adeguatezza, non valuta la ragionevolezza di una stima.
- La verifica documentata resta obbligatoria per ogni elemento che confluisce in carta di lavoro.
- Lo scetticismo professionale si applica all'agente, non solo alla direzione della società.

## II.3 Il blocco per documentazione non conforme: cosa significa e cosa non significa

La funzione di blocco è un controllo di completezza e conformità formale, non una procedura di revisione.

| Il blocco significa | Il blocco non significa |
| --- | --- |
| Manca un documento richiesto | Che la documentazione fornita sia corretta |
| Il documento non è nel formato atteso | Che i dati siano attendibili |
| Il documento non è firmato o datato | Che non vi siano errori significativi |
| Il periodo di riferimento non corrisponde | Che le asserzioni siano soddisfatte |

Corollario operativo, da trasmettere con chiarezza al team: l'assenza di blocco non è un'attestazione di conformità. Un fascicolo che passa il controllo automatico può contenere errori significativi, documentazione contraffatta o omissioni sostanziali. Il superamento del controllo va documentato come dato di fatto, mai come conclusione.

Quando l'agente blocca, il revisore deve:

1. verificare autonomamente che il documento sia effettivamente mancante o difforme, e non un falso positivo;
2. richiederlo formalmente alla società, tracciando data e destinatario della richiesta (vedi modulo in [`09-modulistica.md`](09-modulistica.md), § D.5);
3. se il documento non viene fornito, valutare se ricorre una limitazione alle procedure di revisione e trattarla come tale, comunicandola agli organi di governance;
4. non aggirare il blocco caricando documentazione sostitutiva non equivalente.

## II.4 Struttura di ciascuna scheda prompt

Ogni scheda della libreria operativa ([`../prompts/`](../prompts/)) è composta da:

- **Codice** — per il richiamo in carta di lavoro
- **Documenti da allegare** — la sola documentazione-fonte (societaria e di terzi) necessaria; le carte di lavoro non vanno mai allegate perché sono l'output. Se i documenti-fonte mancano, attendersi il blocco
- **Carta di lavoro prodotta (output)** — la carta di lavoro del modello adottato dallo Studio che la scheda compila in bozza; è il risultato della scheda, mai un input, ed è indicata in ciascuna scheda
- **Prompt** — testo da utilizzare, personalizzabile nelle parti tra parentesi quadre; nella versione espansa di questa libreria include già l'impalcatura di ruolo/contesto e il vincolo anti-allucinazione
- **Output atteso** — la carta di lavoro indicata, compilata in bozza, con i contenuti e i prospetti richiesti dal relativo modello
- **Verifica del revisore** — cosa il revisore deve fare prima di utilizzare l'output

> **Principio.** Le carte di lavoro CNDCEC non sono mai un input dell'agente: sono l'output che l'agente redige in bozza a partire dalla documentazione-fonte. L'agente compila la carta di lavoro; il revisore la verifica, la integra con il proprio giudizio e la sottoscrive.

## II.5 Vincolo permanente da mantenere attivo

Da configurare nelle istruzioni di sistema dell'agente e da richiamare nei prompt critici. La prima regola fissa il perimetro «una società, un team»; le altre governano il modo di rispondere:

```
Regole permanenti per ogni risposta:
- Operi esclusivamente sul fascicolo di una singola società e per un singolo team di revisione. Tratti solo i documenti caricati in questa istanza; non richiamare, confrontare o utilizzare informazioni relative ad altre società o ad altri incarichi.
- Basa ogni affermazione esclusivamente sui documenti che ti sono stati forniti. Quando affermi qualcosa, indica il documento e, ove possibile, la pagina o la voce.
- Se un'informazione necessaria non è presente nella documentazione, dichiaralo esplicitamente come informazione mancante. Non colmare le lacune con ipotesi né con conoscenze generali.
- Distingui sempre in modo visibile: (a) dati rilevati dai documenti, (b) elaborazioni che hai svolto tu, (c) osservazioni o ipotesi tue.
- Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza. Il tuo compito termina con la rilevazione e l'analisi.
- Non citare numeri di paragrafo di principi di revisione o contabili.
- Segnala le contraddizioni tra documenti anche quando non ti sono state chieste.
```

Questo blocco è già incorporato, in forma sintetica, nella sezione "Vincoli permanenti" di ogni prompt espanso della libreria: impostarlo anche a livello di istruzioni di sistema dell'agente lo rende ridondante ma più robusto (si applica anche a richieste estemporanee non tratte dalla libreria).
