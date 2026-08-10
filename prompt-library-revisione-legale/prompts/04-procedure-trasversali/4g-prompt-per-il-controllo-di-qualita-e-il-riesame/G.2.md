# G.2 — Completezza del fascicolo in vista del riesame

> Parte 4 — Procedure trasversali e situazioni particolari · 4.G — Prompt per il controllo di qualità e il riesame
> **Fase AuditFlow:** Completamento — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- indice del fascicolo; carte di lavoro compilate; documentazione dell'utilizzo dell'agente.

## Carta di lavoro / output prodotto

E08 – Completamento dell'audit (checklist di completezza del fascicolo) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: indice del fascicolo; carte di lavoro compilate; documentazione dell'utilizzo dell'agente.

Verifica la completezza formale del fascicolo in vista del riesame.
- Confronta le carte di lavoro presenti con l'elenco atteso per l'incarico ed elenca cosa manca.
- Verifica che, dove l'agente è stato utilizzato, la carta di lavoro riporti la natura dell'utilizzo, le verifiche svolte e la fonte primaria.
- Segnala le carte di lavoro prive di firma di predisposizione o di riesame.
Questo è un controllo di completezza formale, non un riesame di merito. Non attestare la conformità del fascicolo.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: elenco delle mancanze formali e delle tracciature dell'utilizzo dell'agente.
```

## Output atteso

elenco delle mancanze formali e delle tracciature dell'utilizzo dell'agente.

## Verifica del revisore (obbligatoria prima dell'uso)

il superamento del controllo di completezza non attesta la conformità sostanziale del fascicolo.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
