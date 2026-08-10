# C.2.10 — Debiti e ratei e risconti

> Parte 3 — Verifica del bilancio d’esercizio · 3.B — Procedure sulle voci dello stato patrimoniale
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- partitario fornitori; ageing; risposte alla circolarizzazione fornitori; estratti conto dei finanziamenti; documentazione fiscale e contributiva; dettaglio dei ratei e risconti con calcolo; contratti sottostanti.

## Carta di lavoro / output prodotto

D-21 – Debiti verso fornitori, D-22 – Altri debiti e D-14 – Ratei e risconti — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le procedure sul bilancio d'esercizio.
Documenti allegati a questa istanza: partitario fornitori; ageing; risposte alla circolarizzazione fornitori; estratti conto dei finanziamenti; documentazione fiscale e contributiva; dettaglio dei ratei e risconti con calcolo; contratti sottostanti.

Analizza i debiti e i ratei e risconti.
- Riconcilia i partitari con il bilancio e con la nota integrativa, per categoria di debito.
- Analizza l'esito della circolarizzazione fornitori: copertura, risposte, discordanze con riconciliazione, mancate risposte. Per le mancate risposte, verifica i pagamenti successivi documentati.
- Verifica la corretta separazione tra debiti entro e oltre l'esercizio successivo, e l'informativa sui debiti oltre cinque anni.
- Riconcilia i debiti tributari e previdenziali con le dichiarazioni, con il cassetto fiscale e con l'estratto conto contributivo. Elenca ogni differenza.
- Verifica la ricerca delle passività non registrate: analizza i pagamenti e le fatture ricevute nei [N] giorni successivi alla chiusura e verifica la corretta competenza. Elenca le posizioni per le quali la competenza appare riferibile all'esercizio chiuso e non risulta rilevata.
- Analizza le fatture da ricevere: composizione, criterio di determinazione, riscontro con i documenti pervenuti successivamente, confronto con l'esercizio precedente.
- Per ciascun rateo e risconto, verifica il calcolo ricalcolandolo sulla base del contratto sottostante e della competenza temporale. Mostra i calcoli. Elenca le poste prive di contratto a supporto.
- Verifica che non siano classificati tra i ratei e risconti elementi di natura diversa.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
