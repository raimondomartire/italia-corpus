# C.2.4 — Rimanenze

> Parte 3 — Verifica del bilancio d’esercizio · 3.B — Procedure sulle voci dello stato patrimoniale
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- inventario finale a quantità e valore; liste di conta fisica con evidenza della data e dei rilevatori; documentazione sulle rettifiche post-conta; criteri di valorizzazione; distinte base; documentazione sui costi di produzione; analisi di obsolescenza; prezzi di vendita successivi alla chiusura; documentazione su merci presso terzi e di terzi; documentazione su lavori in corso e commesse.

## Carta di lavoro / output prodotto

D-08 – Rimanenze (carte di sezione, campionamenti e cut-off) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le procedure sul bilancio d'esercizio.
Documenti allegati a questa istanza: inventario finale a quantità e valore; liste di conta fisica con evidenza della data e dei rilevatori; documentazione sulle rettifiche post-conta; criteri di valorizzazione; distinte base; documentazione sui costi di produzione; analisi di obsolescenza; prezzi di vendita successivi alla chiusura; documentazione su merci presso terzi e di terzi; documentazione su lavori in corso e commesse.

Analizza le rimanenze finali.
- Riconcilia l'inventario con il bilancio e con la nota integrativa, per categoria.
- Riconcilia le liste di conta fisica con l'inventario finale, esponendo tutte le rettifiche intervenute tra la data della conta e la data di chiusura, con la relativa documentazione di supporto.
- Verifica la coerenza tra esistenze iniziali, movimentazione dell'esercizio ed esistenze finali, per categoria e in totale.
- Ricalcola la valorizzazione di un campione di articoli secondo il criterio dichiarato, esponendo tutti i passaggi del calcolo.
- Per i prodotti finiti e semilavorati, verifica la composizione del costo di produzione: elementi inclusi, criterio di imputazione dei costi indiretti, base di ripartizione, capacità produttiva utilizzata come riferimento. Ricalcola su un campione.
- Analisi di obsolescenza: elenca gli articoli senza movimentazione da oltre [N] mesi, con giacenza eccedente il consumo di [N] mesi, con valore unitario in diminuzione. Esponi il valore complessivo per fascia di anzianità.
- Confronta il valore unitario di carico con i prezzi di vendita successivi alla chiusura, al netto dei costi di vendita, ed elenca gli articoli per i quali il valore di realizzo risulta inferiore al valore di carico, con l'importo della differenza.
- Riconcilia merci presso terzi e di terzi con la documentazione.
- Per i lavori in corso e le commesse: stato di avanzamento, criterio applicato, ricalcolo su un campione, verifica della coerenza tra ricavi maturati, costi sostenuti e margine atteso, elenco delle commesse con margine negativo o in riduzione.
Esponi tutti i calcoli. Non concludere sulla congruità del fondo svalutazione magazzino.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
