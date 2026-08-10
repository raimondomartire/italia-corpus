# Nota al fascicolo su una questione aperta — Nota al fascicolo su una questione aperta

> Parte 5 — Redazione delle note e dei memo di lavoro · 5.H — Note trasversali
> **Fase AuditFlow:** Trasversale (tutte le fasi) — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- descrizione della questione; documentazione pertinente; posizione provvisoria del revisore ove formulata.

## Carta di lavoro / output prodotto

Nota al fascicolo (memo di questione aperta) — bozza da compilare; la nota va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale incaricato di redigere, in bozza, la nota o il memo a corredo di una carta di lavoro già predisposta e verificata dal revisore.
Documenti allegati a questa istanza: descrizione della questione; documentazione pertinente; posizione provvisoria del revisore ove formulata.

Redigi la bozza di una nota al fascicolo sulla seguente questione: [QUESTIONE].
- Descrivi il fatto e il contesto, richiamando i documenti pertinenti.
- Esponi gli elementi a favore e contro le possibili interpretazioni, senza sceglierne una.
- Elenca le informazioni ulteriori da acquisire e i passi successivi.
- Riporta la posizione provvisoria del revisore, se me l’hai indicata, qualificandola come tale.
Non risolvere tu la questione: organizza gli elementi per la decisione del revisore.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: bozza della nota al fascicolo con elementi a favore e contro e passi successivi.
```

## Output atteso

bozza della nota al fascicolo con elementi a favore e contro e passi successivi.

## Verifica del revisore (obbligatoria prima dell'uso)

la decisione sulla questione è del revisore; la nota organizza gli elementi, non li risolve.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
