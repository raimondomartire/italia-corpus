# A.1.1 — Inventario e conformità del fascicolo di accettazione

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.A — Controllo preliminare di conformità documentale
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- visura camerale aggiornata; statuto vigente; atto costitutivo; libro soci o elenco soci; verbali di assemblea degli ultimi tre esercizi; verbali dell’organo amministrativo dell’ultimo esercizio; bilanci approvati degli ultimi tre esercizi con nota integrativa e relazione sulla gestione; relazioni del precedente revisore; relazioni del collegio sindacale; organigramma.

## Carta di lavoro / output prodotto

A05 – PBC (documenti richiesti alla società) e G01 – Indice del permanent audit file — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: visura camerale aggiornata; statuto vigente; atto costitutivo; libro soci o elenco soci; verbali di assemblea degli ultimi tre esercizi; verbali dell’organo amministrativo dell’ultimo esercizio; bilanci approvati degli ultimi tre esercizi con nota integrativa e relazione sulla gestione; relazioni del precedente revisore; relazioni del collegio sindacale; organigramma.

Svolgi il controllo di conformità preliminare del fascicolo di accettazione.
- Elenca i documenti ricevuti indicando per ciascuno: tipologia, data, periodo di riferimento, presenza di firma o sottoscrizione, formato.
- Confronta l'elenco con la documentazione attesa per un incarico di revisione legale di prima nomina e indica cosa manca.
- Segnala ogni difformità: documenti non aggiornati, periodi non coperti, documenti privi di firma, versioni multiple dello stesso documento, pagine mancanti, illeggibilità.
- Segnala le incoerenze tra documenti: ad esempio dati della visura camerale non allineati allo statuto, capitale sociale difforme tra visura e bilancio, composizione degli organi non allineata tra visura e verbali.
Non procedere con analisi di merito. Questo è un controllo di completezza.
Presenta il risultato in tre tabelle: Ricevuti | Mancanti | Difformità rilevate.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: tre tabelle di controllo.
```

## Output atteso

tre tabelle di controllo.

## Verifica del revisore (obbligatoria prima dell'uso)

riscontrare a campione l’esistenza dei documenti elencati; verificare che le mancanze segnalate siano reali; formalizzare la richiesta integrativa alla società.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
