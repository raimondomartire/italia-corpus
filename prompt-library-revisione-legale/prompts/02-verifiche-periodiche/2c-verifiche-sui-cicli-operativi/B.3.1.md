# B.3.1 — Disponibilità liquide

> Parte 2 — Verifiche periodiche sulla regolare tenuta della contabilità · 2.C — Verifiche sui cicli operativi

## Documenti da allegare

- estratti conto bancari di tutti i rapporti; contabili; riconciliazioni bancarie predisposte dalla società; partitari dei conti banca e cassa; prima nota di cassa; elenco completo dei rapporti bancari e delle firme autorizzate; documentazione sugli affidamenti; centrale rischi.

## Carta di lavoro / output prodotto

F03 – Check list della verifica periodica (disponibilità liquide) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le verifiche periodiche sulla regolare tenuta della contabilità.
Documenti allegati a questa istanza: estratti conto bancari di tutti i rapporti; contabili; riconciliazioni bancarie predisposte dalla società; partitari dei conti banca e cassa; prima nota di cassa; elenco completo dei rapporti bancari e delle firme autorizzate; documentazione sugli affidamenti; centrale rischi.

Verifica le disponibilità liquide alla data [DATA].
- Per ciascun rapporto bancario, confronta il saldo dell'estratto conto con il saldo contabile ed esponi la differenza.
- Analizza le riconciliazioni predisposte dalla società: per ciascuna partita riconciliativa indica descrizione, importo, data di origine, anzianità. Segnala le partite di anzianità superiore a [N] giorni, quelle di importo rilevante, quelle prive di descrizione comprensibile e quelle che risultano reiterate rispetto alla riconciliazione precedente.
- Verifica che tutti i rapporti bancari risultanti dagli estratti conto e dalla centrale rischi siano rilevati in contabilità, e viceversa. Segnala i rapporti presenti in un elenco e non nell'altro.
- Analizza i movimenti di cassa: verifica che il saldo non risulti mai negativo nel periodo; elenca i giorni in cui il saldo supera [SOGLIA]; elenca i movimenti di importo superiore a [SOGLIA]; verifica il rispetto dei limiti all'uso del contante per i movimenti rilevati.
- Nei movimenti bancari, individua: bonifici verso controparti non presenti nell'anagrafica fornitori; movimenti verso l'estero; giroconti tra rapporti della società in prossimità della data di chiusura del periodo; movimenti con descrizione generica; accrediti e addebiti storno.
- Verifica gli affidamenti: confronta gli utilizzi con i limiti accordati e segnala gli sconfinamenti.
Esponi ogni confronto con i due valori messi a raffronto.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
