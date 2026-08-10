# A.3.2 — Verifica dei requisiti di indipendenza

> Parte 1 — Accettazione dell’incarico, indipendenza e valutazione del rischio · 1.C — Verifiche per l’accettazione dell’incarico
> **Fase AuditFlow:** Accettazione — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- visura camerale della società e delle società del gruppo; elenco degli incarichi in essere dello studio e del network; elenco dei servizi diversi dalla revisione prestati o proposti; dichiarazioni di indipendenza del personale assegnato; composizione del team; storico degli incarichi di revisione presso il cliente; elenco delle relazioni finanziarie e personali dichiarate.

## Carta di lavoro / output prodotto

B02 – Attestazione di indipendenza e B03 – Verifica dell’indipendenza — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta il responsabile dell'incarico nella fase di accettazione, indipendenza e valutazione del rischio.
Documenti allegati a questa istanza: visura camerale della società e delle società del gruppo; elenco degli incarichi in essere dello studio e del network; elenco dei servizi diversi dalla revisione prestati o proposti; dichiarazioni di indipendenza del personale assegnato; composizione del team; storico degli incarichi di revisione presso il cliente; elenco delle relazioni finanziarie e personali dichiarate.

Svolgi l'analisi dei potenziali rischi per l'indipendenza rispetto a questo incarico. Esamina e riporta in tabella, per ciascuna delle seguenti categorie, gli elementi che emergono dalla documentazione fornita:
- Relazioni finanziarie: partecipazioni, finanziamenti, garanzie, rapporti di credito o debito tra revisore, personale del team, loro familiari e la società o le entità del gruppo.
- Relazioni di affari o di lavoro: rapporti commerciali, precedenti rapporti di lavoro subordinato o di collaborazione, incarichi presso il cliente ricoperti da persone del team.
- Relazioni familiari e personali tra componenti del team e amministratori, sindaci, dirigenti o soci della società.
- Servizi diversi dalla revisione prestati o in corso di negoziazione: descrivili, indica il soggetto che li presta all'interno del network, il corrispettivo e il periodo.
- Durata dell'incarico e dell'associazione delle persone chiave: calcola gli anni di incarico continuativo e gli anni di presenza del responsabile e degli altri soggetti chiave.
- Rilevanza economica: rapporto tra corrispettivi complessivi da questo cliente e ricavi totali dello studio, se il dato è disponibile.
- Presenza di rapporti con entità del gruppo o con parti correlate che possano generare le medesime criticità.
Per ciascun elemento rilevato indica: la fattispecie, il documento di origine, la categoria di minaccia all'indipendenza cui è riconducibile (interesse personale, autoriesame, patrocinio, familiarità, intimidazione). Non valutare la significatività della minaccia né l'adeguatezza delle eventuali misure di salvaguardia. Segnala separatamente le informazioni che ti mancano per completare l'analisi.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: mappatura delle minacce con classificazione e tracciamento delle fonti.
```

## Output atteso

mappatura delle minacce con classificazione e tracciamento delle fonti.

## Verifica del revisore (obbligatoria prima dell'uso)

la valutazione della significatività delle minacce e l’individuazione delle misure di salvaguardia sono di esclusiva competenza del responsabile dell’incarico. L’agente non dispone né dei dati economici complessivi dello studio né della conoscenza dei rapporti non formalizzati. Le dichiarazioni di indipendenza restano procedura autonoma.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
