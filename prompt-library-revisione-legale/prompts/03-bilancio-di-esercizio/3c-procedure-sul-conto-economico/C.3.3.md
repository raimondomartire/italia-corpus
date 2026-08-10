# C.3.3 — Imposte

> Parte 3 — Verifica del bilancio d’esercizio · 3.C — Procedure sul conto economico
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- calcolo delle imposte correnti con riconciliazione tra risultato civilistico e imponibile; dettaglio delle variazioni in aumento e in diminuzione; calcolo della fiscalità differita; dichiarazioni dell’esercizio precedente; documentazione sulle perdite fiscali riportabili; documentazione su agevolazioni e crediti d’imposta.

## Carta di lavoro / output prodotto

D-10 – Imposte — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le procedure sul bilancio d'esercizio.
Documenti allegati a questa istanza: calcolo delle imposte correnti con riconciliazione tra risultato civilistico e imponibile; dettaglio delle variazioni in aumento e in diminuzione; calcolo della fiscalità differita; dichiarazioni dell’esercizio precedente; documentazione sulle perdite fiscali riportabili; documentazione su agevolazioni e crediti d’imposta.

Analizza le imposte.
- Verifica la riconciliazione tra risultato ante imposte e imponibile fiscale: ricalcola il totale delle variazioni e verifica la quadratura.
- Per ciascuna variazione, riporta descrizione, importo, natura (permanente o temporanea), documentazione di supporto presente. Segnala le variazioni prive di supporto documentale.
- Ricalcola le imposte correnti applicando le aliquote all'imponibile determinato e confronta con il contabilizzato. Mostra il calcolo.
- Verifica la fiscalità differita: per ciascuna differenza temporanea, importo, aliquota applicata, esercizio atteso di riassorbimento, imposta calcolata. Ricalcola e confronta.
- Per le imposte anticipate, elenca gli elementi documentali a supporto della ragionevole certezza di recupero: piani, budget, redditi imponibili attesi, con data e orizzonte temporale.
- Verifica il riporto delle perdite fiscali: importo residuo, esercizio di formazione, limiti di utilizzo, coerenza con la dichiarazione dell'esercizio precedente.
- Verifica la riconciliazione tra i debiti tributari, gli acconti versati risultanti dagli F24 e le imposte di competenza.
- Calcola l'aliquota effettiva e confrontala con quella nominale e con l'esercizio precedente, esponendo le componenti dello scostamento.
Non esprimere valutazioni sulla correttezza del trattamento fiscale adottato né sulla spettanza delle agevolazioni.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
