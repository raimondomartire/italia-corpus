# D.4.2 — Valutazione del rischio con approccio semplificato

> Parte 4 — Procedure trasversali e situazioni particolari · 4.D — Specificità delle nano-imprese e delle imprese di minori dimensioni
> **Fase AuditFlow:** Pianificazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- bilancio dell'esercizio e dei due precedenti; risultanze delle procedure di analisi comparativa preliminari; documentazione della comprensione dell'entità e del contesto; note sul sistema di controllo interno.

## Carta di lavoro / output prodotto

C13 – Valutazione dei rischi per singola voce e asserzione (approccio semplificato) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: bilancio dell'esercizio e dei due precedenti; risultanze delle procedure di analisi comparativa preliminari; documentazione della comprensione dell'entità e del contesto; note sul sistema di controllo interno.

Supportami nell'identificazione e valutazione dei rischi di errori significativi con l'approccio semplificato ammesso per le nano-imprese, che assume un rischio di controllo elevato e stima direttamente il rischio di errori significativi senza scomporlo tra rischio intrinseco e rischio di controllo.
- Per ciascuna significativa classe di operazioni, saldo contabile e informativa, descrivi gli elementi documentali che incidono sul rischio intrinseco: natura della voce, grado di soggettività, volumi, presenza di stime, operazioni con il proprietario-amministratore o con parti correlate.
- Attribuisci a probabilità e impatto un valore qualitativo — alto, moderato o basso — motivando l'attribuzione sui soli elementi documentali.
- Combina probabilità e impatto in una matrice e classifica il rischio residuo risultante, tenendo il rischio di controllo sistematicamente alto.
- Evidenzia le voci che risultano rischi significativi (probabilità e impatto entrambi alti), che richiedono speciale considerazione.
- Distingui le voci da affrontare con test di dettaglio da quelle che, per importo e rischio contenuto, possono essere coperte dalla procedura di analisi comparativa finale.
Non concludere la valutazione del rischio: la determinazione finale del livello di rischio e delle risposte è mia. Segnala le voci per le quali i documenti non bastano ad attribuire un valore.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: matrice probabilità/impatto per voce con proposta di classificazione.
```

## Output atteso

matrice probabilità/impatto per voce con proposta di classificazione.

## Verifica del revisore (obbligatoria prima dell'uso)

la valutazione del rischio è un giudizio professionale non delegabile; l'agente ordina gli elementi, non decide il livello.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
