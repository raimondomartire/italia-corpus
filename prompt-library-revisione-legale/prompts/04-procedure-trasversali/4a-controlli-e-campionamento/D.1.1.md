# D.1.1 — Progettazione dei test di conformità sui controlli

> Parte 4 — Procedure trasversali e situazioni particolari · 4.A — Controlli e campionamento
> **Fase AuditFlow:** Esecuzione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- descrizione del controllo da testare; procedura formalizzata; evidenza documentale prodotta dal controllo; popolazione delle operazioni del periodo; matrice delle autorizzazioni; descrizione del flusso del processo fornita dalla società.

## Carta di lavoro / output prodotto

C10 – Questionario sul sistema di controllo interno (progettazione dei test sui controlli) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: descrizione del controllo da testare; procedura formalizzata; evidenza documentale prodotta dal controllo; popolazione delle operazioni del periodo; matrice delle autorizzazioni; descrizione del flusso del processo fornita dalla società.

Sto pianificando i test di conformità sul seguente controllo: [DESCRIZIONE]. Il rischio cui il controllo risponde è: [RISCHIO].
- Descrivi il controllo come risulta dalla documentazione, indicando: chi lo esegue, con quale frequenza, su quale popolazione, con quale evidenza documentale, cosa accade quando il controllo rileva un'eccezione.
- Classifica il controllo: manuale o automatico, preventivo o successivo, controllo di processo o controllo di supervisione.
- Individua gli attributi verificabili del controllo, cioè gli elementi che devono essere presenti nell'evidenza perché il controllo risulti eseguito. Elencali in modo che io possa costruire una scheda di test.
- Indica quale evidenza documentale consente di verificare ciascun attributo.
- Segnala gli attributi per i quali la documentazione descritta non lascia traccia verificabile: sono i punti in cui il test non potrà essere svolto per ispezione e richiederà osservazione o riesecuzione.
- Segnala le dipendenze del controllo da altri controlli o da dati prodotti da sistemi: se il controllo si basa su un report, l'affidabilità del report è essa stessa oggetto di verifica. Elenca questi elementi.
Non concludere sull'efficacia del controllo né sulla possibilità di farvi affidamento.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: scheda di test con attributi verificabili e dipendenze.
```

## Output atteso

scheda di test con attributi verificabili e dipendenze.

## Verifica del revisore (obbligatoria prima dell'uso)

la corrispondenza tra controllo descritto e controllo operante va verificata direttamente. L’agente lavora sulla descrizione, non sull’operatività.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
