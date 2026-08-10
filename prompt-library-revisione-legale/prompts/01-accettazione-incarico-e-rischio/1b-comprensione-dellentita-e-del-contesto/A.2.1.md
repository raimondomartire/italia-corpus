# A.2.1 — Profilo dell’entità

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.B — Comprensione dell’entità e del contesto
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- visura camerale; statuto; bilanci ultimi tre esercizi; relazione sulla gestione; organigramma; sito istituzionale o materiale descrittivo del business; elenco delle sedi e delle unità locali.

## Carta di lavoro / output prodotto

B05 – Memorandum delle altre informazioni acquisite (profilo dell’entità), con alimentazione del G01 – Permanent file — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: visura camerale; statuto; bilanci ultimi tre esercizi; relazione sulla gestione; organigramma; sito istituzionale o materiale descrittivo del business; elenco delle sedi e delle unità locali.

Costruisci il profilo dell'entità sulla base della documentazione fornita.
Struttura la risposta nelle seguenti sezioni:
- Forma giuridica, assetto proprietario, struttura del gruppo se esistente, organi sociali e loro composizione, con date di nomina e scadenza.
- Attività svolta: prodotti o servizi, mercati serviti, canali di vendita, modello di ricavo, ciclo produttivo, principali fattori produttivi.
- Dimensione economica: andamento su tre esercizi di ricavi, marginalità, patrimonio netto, posizione finanziaria netta, dipendenti.
- Elementi strutturali rilevanti: presenza di magazzino, di lavorazioni in corso, di commesse pluriennali, di partecipazioni, di immobilizzazioni immateriali significative, di indebitamento finanziario, di garanzie prestate.
- Operazioni straordinarie o eventi non ricorrenti emergenti dai documenti.
Per ciascuna informazione indica il documento da cui la ricavi.
Elenca separatamente le informazioni che non sei riuscito a ricavare e che dovrò acquisire.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: profilo strutturato con tracciamento delle fonti ed elenco delle lacune informative.
```

## Output atteso

profilo strutturato con tracciamento delle fonti ed elenco delle lacune informative.

## Verifica del revisore (obbligatoria prima dell'uso)

riscontro dei dati dimensionali sui bilanci; integrazione delle lacune tramite colloquio con la direzione, da documentare separatamente.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
