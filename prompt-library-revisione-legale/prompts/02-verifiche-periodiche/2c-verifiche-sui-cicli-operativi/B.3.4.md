# B.3.4 — Rimanenze di magazzino

> Parte 2 — Verifiche periodiche sulla regolare tenuta della contabilità · 2.C — Verifiche sui cicli operativi
> **Fase AuditFlow:** Verifiche periodiche — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- situazione di magazzino a quantità e valore; movimentazione del periodo; criteri di valorizzazione formalizzati; distinte base; documentazione sulle conte fisiche svolte; elenco degli scarti e delle rettifiche inventariali; documentazione su merci presso terzi e di terzi.

## Carta di lavoro / output prodotto

F03 – Check list della verifica periodica (rimanenze) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le verifiche periodiche sulla regolare tenuta della contabilità.
Documenti allegati a questa istanza: situazione di magazzino a quantità e valore; movimentazione del periodo; criteri di valorizzazione formalizzati; distinte base; documentazione sulle conte fisiche svolte; elenco degli scarti e delle rettifiche inventariali; documentazione su merci presso terzi e di terzi.

Verifica le rimanenze alla data [DATA].
- Riconcilia il valore complessivo del magazzino con il saldo contabile.
- Verifica la coerenza interna della movimentazione: esistenza iniziale più entrate meno uscite uguale esistenza finale, per ciascuna categoria e in totale. Elenca le differenze.
- Verifica che nessun articolo presenti giacenza negativa in quantità o in valore, in nessun momento del periodo.
- Analizza l'indice di rotazione per categoria e la sua evoluzione.
- Individua gli articoli con le seguenti caratteristiche: a) nessuna movimentazione da oltre [N] mesi; b) giacenza superiore al consumo di [N] mesi; c) valore unitario significativamente difforme rispetto ad articoli della medesima categoria; d) valore unitario in aumento o in diminuzione rilevante rispetto al periodo precedente; e) quantità in giacenza superiore a [SOGLIA] e valore rilevante.
- Analizza le rettifiche inventariali del periodo: numero, importo, segno, concentrazione temporale, concentrazione per articolo o categoria, autorizzazione. Segnala le rettifiche di importo rilevante e quelle ricorrenti sui medesimi articoli.
- Verifica la coerenza del criterio di valorizzazione applicato con quello formalizzato, ricalcolando il valore di un campione di articoli che ti indico e mostrando il calcolo.
- Riconcilia le merci presso terzi e di terzi con la documentazione di supporto e verifica la loro corretta esclusione o inclusione nella valorizzazione.
Esponi i calcoli in modo verificabile.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
