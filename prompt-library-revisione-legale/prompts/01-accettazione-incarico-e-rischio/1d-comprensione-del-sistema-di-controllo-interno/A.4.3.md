# A.4.3 — Controlli generali informatici

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.D — Comprensione del sistema di controllo interno
> **Fase AuditFlow:** Pianificazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- descrizione dell’infrastruttura IT; elenco degli applicativi e delle versioni; matrice delle autorizzazioni e dei profili utente; policy di accesso e di password; procedure di backup e di disaster recovery; log delle modifiche ai sistemi; contratti con fornitori IT e con eventuali outsourcer; relazioni di audit sui fornitori di servizi.

## Carta di lavoro / output prodotto

C11 – Sistemi IT — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: descrizione dell’infrastruttura IT; elenco degli applicativi e delle versioni; matrice delle autorizzazioni e dei profili utente; policy di accesso e di password; procedure di backup e di disaster recovery; log delle modifiche ai sistemi; contratti con fornitori IT e con eventuali outsourcer; relazioni di audit sui fornitori di servizi.

Analizza la documentazione informatica ed esponi:
- L'architettura applicativa rilevante per l'informativa finanziaria: quali sistemi generano dati contabili, come dialogano, dove risiedono i dati, chi li gestisce.
- La gestione degli accessi: come vengono creati, modificati e revocati gli utenti; quali profili esistono; chi dispone di privilegi amministrativi; come sono gestiti gli accessi degli amministratori di sistema e dei fornitori.
- Dalla matrice delle autorizzazioni, individua le combinazioni di funzioni attribuite al medesimo utente che risultano incompatibili tra loro, in particolare: chi può sia inserire un fornitore sia autorizzare un pagamento; chi può sia registrare una vendita sia emettere una nota di credito; chi può sia modificare l'anagrafica dipendenti sia autorizzare i cedolini; chi può sia effettuare registrazioni contabili sia modificarle o cancellarle.
- La gestione delle modifiche ai programmi e il controllo sulle personalizzazioni.
- Continuità operativa e integrità dei dati: backup, tracciabilità delle modifiche, inalterabilità delle registrazioni contabili.
- Dipendenza da fornitori esterni e presenza di attestazioni di controllo sui loro processi.
Per il punto 3 presenta una tabella: Utente o profilo | Funzioni cumulate | Rischio teorico che ne deriva. Basati esclusivamente sulla matrice fornita.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)



## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
