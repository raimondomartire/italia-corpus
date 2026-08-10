# D.1.2 — Dimensionamento del campione

> Parte 4 — Procedure trasversali e situazioni particolari · 4.A — Controlli e campionamento
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- popolazione completa in formato elaborabile; policy dello studio sul campionamento; significatività operativa; valutazione del rischio per l’asserzione interessata.

## Carta di lavoro / output prodotto

Modulo di campionamento della voce interessata (es. D09-04, D21-04, D08-05) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: popolazione completa in formato elaborabile; policy dello studio sul campionamento; significatività operativa; valutazione del rischio per l’asserzione interessata.

Supportami nel dimensionamento del campione per la seguente procedura: [DESCRIZIONE DELLA PROCEDURA E DELL'ASSERZIONE].
- Descrivi la popolazione: numerosità, valore complessivo, valore medio e mediano, distribuzione per fascia di importo, presenza di valori estremi, elementi di segno negativo, elementi con valore nullo.
- Verifica la completezza della popolazione: riconcilia il totale dell'estrazione con il saldo contabile ed esponi ogni differenza. Se la popolazione non risulta completa, segnalalo prima di procedere.
- Individua gli elementi che devono essere esaminati integralmente perché di importo superiore alla significatività operativa o per altre caratteristiche di rilievo, ed esponi il valore residuo della popolazione dopo la loro estrazione.
- Applica i criteri di dimensionamento previsti dalla policy dello studio ai parametri che ti indico: [LIVELLO DI RISCHIO], [AFFIDAMENTO SUI CONTROLLI], [ERRORE ATTESO]. Esponi il calcolo in modo verificabile.
- Proponi una stratificazione della popolazione residua e indica il dimensionamento per ciascuno strato.
- Genera la selezione applicando il metodo che ti indico [CASUALE / SISTEMATICO / PER UNITÀ MONETARIA] ed esponi il criterio, il punto di partenza e l'intervallo utilizzati, così che la selezione sia riproducibile.
La decisione sull'ampiezza del campione è mia. Tu fornisci il supporto di calcolo e la selezione.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)

riesecuzione del dimensionamento; verifica che la selezione sia riproducibile e non manipolabile; verifica della completezza della popolazione su fonte contabile.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
