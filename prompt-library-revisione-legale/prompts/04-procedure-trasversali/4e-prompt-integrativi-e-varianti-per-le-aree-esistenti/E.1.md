# E.1 — Analisi del settore senza benchmark inventati (variante di A.2.2)

> Parte 4 — Procedure trasversali e situazioni particolari · 4.E — Prompt integrativi e varianti per le aree esistenti
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- profilo dell'entità; descrizione del modello di business; eventuale documentazione di settore già raccolta dal revisore.

## Carta di lavoro / output prodotto

B05 – Memorandum delle altre informazioni acquisite / C14 – Planning memo (analisi di settore) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: profilo dell'entità; descrizione del modello di business; eventuale documentazione di settore già raccolta dal revisore.

Sto svolgendo l'analisi del settore per la comprensione dell'entità. Il settore è [SETTORE], il modello di business è [DESCRIZIONE].
- Descrivi i driver economici del settore e le aree di bilancio che vi presentano tipicamente maggiore complessità o soggettività.
- Formula le domande che dovrei porre alla direzione per far emergere aspetti che un revisore esterno rischia di non cogliere.
- Dove sarebbe utile un benchmark o un dato di settore, non fornire un valore: indica quale dato dovrei cercare e presso quale fonte indipendente reperirlo.
Non riportare statistiche, quote di mercato o valori di settore: sono la principale fonte di allucinazione in questo compito. Se non conosci bene il settore, dichiaralo.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)

i dati di settore vanno reperiti su fonti indipendenti; l'output orienta la ricerca, non la chiude.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
