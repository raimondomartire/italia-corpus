# B.2.3 — Quadratura del bilancio di verifica

> Parte 2 — Verifiche periodiche sulla regolare tenuta della contabilità · 2.B — Regolarità formale delle scritture e dei libri

## Documenti da allegare

- bilancio di verifica alla data; bilancio di verifica alla data della verifica precedente; bilancio dell’esercizio precedente approvato; libro giornale.

## Carta di lavoro / output prodotto

A01 – Mapping del bilancio di verifica — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le verifiche periodiche sulla regolare tenuta della contabilità.
Documenti allegati a questa istanza: bilancio di verifica alla data; bilancio di verifica alla data della verifica precedente; bilancio dell’esercizio precedente approvato; libro giornale.

Verifica la coerenza del bilancio di verifica.
- Verifica la quadratura contabile complessiva: totale dare uguale a totale avere; totale attivo uguale a totale passivo più patrimonio netto più o meno risultato di periodo.
- Verifica la continuità: i saldi di apertura dei conti patrimoniali coincidono con i saldi di chiusura del bilancio approvato dell'esercizio precedente? elenca ogni differenza con l'importo.
- Per ogni differenza rilevata al punto 2, ricerca nel libro giornale la registrazione che l'ha generata e riportala.
- Verifica la coerenza con la verifica precedente: elenca i conti la cui movimentazione nel periodo appare incoerente con l'andamento atteso.
- Individua i conti con saldo di segno contrario a quello atteso per la loro natura ed elencali con l'importo.
- Individua i conti che non risultano movimentati da oltre [N] mesi pur presentando un saldo.
- Verifica che i conti d'ordine e le partite di giro risultino quadrati.
Esponi ogni verifica con i valori confrontati e la differenza, in modo che io possa ricalcolarla.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
