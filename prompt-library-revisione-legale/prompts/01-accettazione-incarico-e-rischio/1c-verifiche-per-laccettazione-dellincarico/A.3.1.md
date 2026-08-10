# A.3.1 — Integrità della direzione e fattori di rischio dell’incarico

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.C — Verifiche per l’accettazione dell’incarico
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- visura camerale storica; libro soci; verbali di assemblea e dell’organo amministrativo; bilanci ultimi tre esercizi; relazioni del precedente revisore; relazioni del collegio sindacale; eventuale documentazione su contenziosi; situazione debitoria fiscale e contributiva.

## Carta di lavoro / output prodotto

B08 – Questionario di accettazione dell’incarico (o B09 – Questionario di continuazione) e C03 – Rideterminazione del rischio dell’incarico — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: visura camerale storica; libro soci; verbali di assemblea e dell’organo amministrativo; bilanci ultimi tre esercizi; relazioni del precedente revisore; relazioni del collegio sindacale; eventuale documentazione su contenziosi; situazione debitoria fiscale e contributiva.

Analizza la documentazione per individuare elementi rilevanti ai fini della valutazione di accettazione dell'incarico.
- Ricostruisci la storia degli organi sociali e dei revisori negli ultimi cinque esercizi: nomine, revoche, dimissioni, mancate riconferme. Segnala ogni avvicendamento anomalo o anticipato rispetto al mandato.
- Analizza le relazioni dei precedenti revisori e del collegio sindacale: riporta tutti i rilievi, i richiami di informativa, i giudizi con modifica, le limitazioni, le segnalazioni di irregolarità.
- Individua nei verbali le discussioni su temi contabili controversi, su dissensi interni, su operazioni con soci o parti correlate.
- Segnala indicatori di tensione finanziaria: perdite ricorrenti, riduzioni di capitale, ricapitalizzazioni, rinegoziazioni del debito, ritardi nei pagamenti fiscali e contributivi, procedure esecutive.
- Verifica la puntualità nell'approvazione e nel deposito dei bilanci, segnalando ricorsi al maggior termine e relative motivazioni.
Per ogni elemento indica il documento e la data.
Non concludere sulla accettabilità dell'incarico: elenca i fatti.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: elenco fattuale cronologico di elementi rilevanti.
```

## Output atteso

elenco fattuale cronologico di elementi rilevanti.

## Verifica del revisore (obbligatoria prima dell'uso)

riscontro sui documenti originali; integrazione con le comunicazioni con il precedente revisore, che restano procedura a carico del revisore; valutazione conclusiva di accettazione documentata in autonomia.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
