# Sezione III — Governance del sistema, qualità e monitoraggio

Le regole di questa sezione si inquadrano nel sistema di gestione della qualità dello Studio (conformità a ISQM Italia 1 e 2 e ISA Italia 220), che tratta l'agente come risorsa tecnologica del sistema e disciplina monitoraggio, riesame della qualità e azioni correttive.

## III.1 Ruoli e responsabilità

| Ruolo | Responsabilità in materia di utilizzo dell'AI |
| --- | --- |
| Responsabile del sistema di controllo qualità | Approva il manuale e i suoi aggiornamenti; approva gli strumenti utilizzabili; definisce i livelli di autorizzazione; sovrintende al monitoraggio |
| Referente AI (designato) | Configura l'agente; gestisce le istruzioni di sistema; conduce i test periodici di affidabilità; tiene il registro degli incidenti; assicura la formazione |
| Responsabile dell'incarico | Decide se e come utilizzare l'agente sull'incarico; verifica che l'utilizzo sia documentato; risponde di ogni contenuto confluito nelle carte di lavoro |
| Componenti del team | Utilizzano l'agente nei limiti del manuale e del proprio livello di autorizzazione; verificano ogni output; documentano l'utilizzo; segnalano gli incidenti |
| Riesaminatore della qualità dell'incarico | Verifica che l'utilizzo dell'AI sia stato documentato e che le conclusioni non siano state recepite senza verifica |
| Referente IT e responsabile della protezione dei dati | Presidiano il perimetro tecnico, la configurazione degli accessi e la conformità del trattamento |

## III.2 Livelli di autorizzazione

L'utilizzo dell'agente è graduato per seniority. Il livello non riflette una gerarchia di merito ma la capacità di riconoscere un output errato: uno strumento che produce testo plausibile è tanto più pericoloso quanto minore è la competenza di chi lo verifica.

| Livello | Chi | Utilizzi consentiti |
| --- | --- | --- |
| Base | Assistant primo e secondo anno | Riconciliazioni, quadrature, estrazioni, analisi comparative descrittive, predisposizione di prospetti. Ogni output è verificato dal senior prima di confluire in carta di lavoro |
| Intermedio | Senior | Tutto il livello base, più analisi di anomalie, progettazione di procedure, campionamento, bozze di memo interni |
| Avanzato | Manager e responsabile dell'incarico | Tutte le schede, comprese quelle su stime, continuità aziendale, frode, gruppi, bozze di comunicazioni e documenti a firma |

Le schede relative a frode, continuità aziendale, indipendenza, parti correlate e antiriciclaggio non sono utilizzabili al livello base, indipendentemente dalla supervisione.

## III.3 Registro degli utilizzi

Per ogni incarico è tenuto un registro sintetico, conservato nel fascicolo (modulo in [`09-modulistica.md`](09-modulistica.md), § D.2), che riporta:

| Campo | Contenuto |
| --- | --- |
| Data | Data di utilizzo |
| Scheda | Codice della scheda prompt utilizzata, o indicazione di utilizzo non standard |
| Utente | Chi ha utilizzato l'agente |
| Area | Area di bilancio o fase interessata |
| Documenti caricati | Elenco sintetico |
| Esito del controllo di conformità | Superato / bloccato, con indicazione del motivo |
| Verifica svolta | Chi ha verificato l'output e con quale esito |
| Destinazione | Carta di lavoro in cui l'output è confluito, oppure indicazione che non è stato utilizzato |

Il registro non sostituisce la documentazione dell'utilizzo nelle singole carte di lavoro: ne consente il monitoraggio aggregato.

## III.4 Test periodici di affidabilità

L'agente va sottoposto a verifica periodica indipendente. Un sistema che ha funzionato correttamente per mesi può degradare a seguito di aggiornamenti del modello sottostante, modifiche alla configurazione o variazioni nella qualità della documentazione caricata.

Protocollo di test (modulo in [`09-modulistica.md`](09-modulistica.md), § D.4), con periodicità almeno semestrale e comunque a ogni aggiornamento della configurazione:

- **Casi con esito noto.** Si sottopongono all'agente fascicoli o estratti di cui si conosce il risultato corretto, comprensivi di errori deliberatamente inseriti. Si verifica quali errori vengono rilevati e quali no.
- **Test di completezza del blocco.** Si sottopone documentazione incompleta o difforme e si verifica che il blocco intervenga.
- **Test di falso positivo.** Si sottopone documentazione conforme e si verifica che il blocco non intervenga senza ragione.
- **Test di allucinazione.** Si formulano richieste su elementi non presenti nella documentazione e si verifica che l'agente dichiari l'assenza anziché ipotizzare.
- **Test di aderenza al perimetro.** Si verifica che l'agente non concluda, non giudichi e non citi riferimenti normativi in violazione delle istruzioni permanenti.
- **Test di riproducibilità.** Si ripete la medesima richiesta a distanza di tempo e si confrontano gli esiti.

Gli esiti sono documentati e conservati. Un esito negativo su uno qualunque dei punti *test di allucinazione*, *aderenza al perimetro* o *riproducibilità* comporta la sospensione dell'utilizzo dell'agente sull'area interessata fino alla risoluzione.

## III.5 Gestione degli incidenti

Costituisce incidente da segnalare al referente AI e al responsabile della qualità (modulo in [`09-modulistica.md`](09-modulistica.md), § D.3):

- un output errato che è confluito, anche parzialmente, in una carta di lavoro;
- un output errato che avrebbe potuto condurre a una conclusione sbagliata, anche se intercettato;
- un blocco per documentazione non conforme rivelatosi infondato;
- una mancata attivazione del blocco in presenza di documentazione difforme;
- un comportamento dell'agente non conforme alle istruzioni permanenti;
- un dubbio sull'integrità del perimetro dei dati.

**Contenuto della segnalazione:** data, incarico, scheda utilizzata, descrizione del comportamento osservato, output prodotto, conseguenza effettiva o potenziale, azione intrapresa.

**Trattamento:** il referente AI valuta se l'incidente sia isolato o sistematico, se richieda una modifica della configurazione o del manuale, e se altri incarichi possano esserne stati interessati. Gli incidenti sistematici comportano il riesame degli incarichi in cui la medesima scheda è stata utilizzata.

## III.6 Riesame e aggiornamento

Il manuale/libreria è riesaminato con periodicità almeno annuale e comunque:

- a ogni modifica dei principi di revisione applicabili;
- a ogni aggiornamento rilevante del modello o della configurazione dell'agente;
- a seguito di incidenti sistematici;
- a seguito di rilievi in sede di monitoraggio interno o di ispezione esterna.

Ogni versione è numerata, datata e approvata. Le versioni superate sono conservate (vedi tabella di approvazione e controllo versioni nel [`README`](../README.md)).
