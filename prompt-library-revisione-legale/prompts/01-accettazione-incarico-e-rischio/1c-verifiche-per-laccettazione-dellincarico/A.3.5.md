# A.3.5 — Predisposizione della lettera di incarico

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.C — Verifiche per l’accettazione dell’incarico
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- delibera di conferimento; profilo dell’entità; modello di lettera di incarico dello studio; eventuale lettera dell’esercizio precedente.

## Carta di lavoro / output prodotto

B10 – Lettera di incarico — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: delibera di conferimento; profilo dell’entità; modello di lettera di incarico dello studio; eventuale lettera dell’esercizio precedente.

Predisponi la bozza di lettera di incarico sulla base del modello fornito, adattandola alla specifica società. Verifica e adatta in particolare:
- La corretta identificazione delle parti e degli organi.
- L'individuazione del quadro normativo sull'informazione finanziaria applicabile alla società.
- L'oggetto dell'incarico, includendo tutte le attività dovute: revisione del bilancio d'esercizio, eventuale bilancio consolidato, verifiche periodiche sulla regolare tenuta della contabilità, ogni ulteriore attestazione richiesta.
- La descrizione delle responsabilità della direzione, con specifico riferimento alla predisposizione del bilancio, al sistema di controllo interno, alla messa a disposizione della documentazione e alla rilascio dell'attestazione finale.
- La descrizione dei limiti intrinseci della revisione.
- Durata, corrispettivo e criteri di adeguamento.
- Modalità di comunicazione e riservatezza.
Evidenzia con una marcatura ogni punto in cui hai dovuto adattare il modello e ogni punto in cui il modello richiede un dato che non ho fornito. Non inserire clausole non presenti nel modello senza segnalarmelo.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)

revisione integrale del testo. La lettera è un documento contrattuale: nessun automatismo è accettabile.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
