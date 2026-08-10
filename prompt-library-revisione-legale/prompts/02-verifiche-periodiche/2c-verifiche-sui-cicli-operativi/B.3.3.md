# B.3.3 — Ciclo passivo e debiti

> Parte 2 — Verifiche periodiche sulla regolare tenuta della contabilità · 2.C — Verifiche sui cicli operativi
> **Fase AuditFlow:** Verifiche periodiche — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- partitario fornitori con partite aperte; ageing dei debiti; registro IVA acquisti; anagrafica fornitori; contratti con i principali fornitori; documentazione su ordini e autorizzazioni; elenco delle fatture da ricevere.

## Carta di lavoro / output prodotto

F03 – Check list della verifica periodica (ciclo passivo e debiti) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le verifiche periodiche sulla regolare tenuta della contabilità.
Documenti allegati a questa istanza: partitario fornitori con partite aperte; ageing dei debiti; registro IVA acquisti; anagrafica fornitori; contratti con i principali fornitori; documentazione su ordini e autorizzazioni; elenco delle fatture da ricevere.

Verifica il ciclo passivo alla data [DATA].
- Riconcilia il totale del partitario fornitori con il saldo contabile.
- Riconcilia i costi contabilizzati con i totali del registro IVA acquisti, esponendo le partite di raccordo.
- Analizza l'ageing dei debiti e la sua evoluzione, calcolando i giorni medi di pagamento e confrontandoli con i termini contrattuali.
- Elenca le posizioni con le seguenti caratteristiche: a) saldo a debito di segno contrario; b) partite scadute e non pagate da oltre [N] giorni; c) partite non movimentate da oltre [N] mesi; d) fornitori con saldo superiore a [SOGLIA].
- Analizza l'anagrafica fornitori: fornitori inseriti nel periodo; fornitori con una sola operazione; fornitori privi di partita IVA o con dati anagrafici incompleti; fornitori con coordinate bancarie modificate nel periodo; fornitori con sede coincidente con quella di altri fornitori, di dipendenti o di parti correlate; fornitori con denominazione simile ad altri.
- Verifica la corrispondenza tra fornitori presenti in anagrafica e fornitori effettivamente movimentati.
- Analizza le prestazioni di servizi generiche: consulenze, prestazioni professionali, servizi non specificati. Elenca gli importi, i fornitori, la presenza di un contratto e la descrizione riportata in fattura. Segnala le fatture con descrizione generica e importo rilevante.
- Verifica la progressività della numerazione di protocollo degli acquisti e la coerenza tra data della fattura e data di registrazione.
- Analizza le fatture da ricevere: composizione, anzianità, criterio di determinazione, confronto con il periodo precedente.
Presenta ciascun punto in tabella separata.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
