# C.1.1 — Conformità del fascicolo di bilancio

> Parte 3 — Verifica del bilancio d’esercizio · 3.A — Apertura della fase di bilancio
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- progetto di bilancio completo con stato patrimoniale, conto economico, rendiconto finanziario e nota integrativa; relazione sulla gestione; bilancio di verifica finale; verbale dell’organo amministrativo di approvazione del progetto; relazione dell’organo di controllo; bilancio dell’esercizio precedente approvato; prospetti di dettaglio di tutte le voci.

## Carta di lavoro / output prodotto

A05 – PBC (fascicolo di bilancio) ed E08 – Completamento dell’audit — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le procedure sul bilancio d'esercizio.
Documenti allegati a questa istanza: progetto di bilancio completo con stato patrimoniale, conto economico, rendiconto finanziario e nota integrativa; relazione sulla gestione; bilancio di verifica finale; verbale dell’organo amministrativo di approvazione del progetto; relazione dell’organo di controllo; bilancio dell’esercizio precedente approvato; prospetti di dettaglio di tutte le voci.

Svolgi il controllo di conformità del fascicolo di bilancio.
- Verifica la completezza del fascicolo rispetto ai documenti attesi ed elenca ciò che manca.
- Verifica la conformità formale: presenza delle firme, data del progetto, coerenza tra le date dei documenti, versione definitiva o bozza.
- Verifica la quadratura interna del bilancio: totale attivo uguale a totale passivo; risultato di conto economico uguale al risultato riportato nello stato patrimoniale; totali dei raggruppamenti uguali alla somma delle voci componenti.
- Verifica la corrispondenza tra bilancio e bilancio di verifica finale, voce per voce, esponendo ogni differenza.
- Verifica la corrispondenza tra i valori dell'esercizio precedente riportati a confronto e il bilancio approvato dell'esercizio precedente. Elenca ogni differenza e verifica se sia data informativa della riclassificazione o della rettifica.
- Verifica la coerenza tra i valori esposti nei prospetti e i medesimi valori richiamati in nota integrativa e nella relazione sulla gestione. Elenca ogni incoerenza con l'indicazione dei due valori.
- Verifica la coerenza tra rendiconto finanziario e variazioni patrimoniali: il flusso di cassa complessivo corrisponde alla variazione delle disponibilità liquide?
Elenca ogni difformità con i valori a raffronto. Se il fascicolo non consente di procedere, indicalo espressamente.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
