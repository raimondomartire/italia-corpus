# B.2.2 — Analisi delle registrazioni contabili

> Parte 2 — Verifiche periodiche sulla regolare tenuta della contabilità · 2.B — Regolarità formale delle scritture e dei libri

## Documenti da allegare

- estrazione completa del libro giornale del periodo in formato elaborabile, con campi: data operazione, data registrazione, numero protocollo, causale, conto, descrizione, importo dare, importo avere, utente inseritore, riferimento documento.

## Carta di lavoro / output prodotto

F03 – Check list della verifica periodica e C05 – Controlli antifrode sul libro giornale — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta le verifiche periodiche sulla regolare tenuta della contabilità.
Documenti allegati a questa istanza: estrazione completa del libro giornale del periodo in formato elaborabile, con campi: data operazione, data registrazione, numero protocollo, causale, conto, descrizione, importo dare, importo avere, utente inseritore, riferimento documento.

Analizza l'estrazione delle registrazioni contabili del periodo.
- Fornisci le statistiche descrittive: numero totale di registrazioni, distribuzione per mese, per causale, per utente, importo medio e mediano, valori estremi.
- Verifica la quadratura: per ciascuna registrazione, dare e avere coincidono? elenca le registrazioni sbilanciate.
- Identifica e isola le registrazioni che presentano le seguenti caratteristiche, elencandole in tabelle separate: a) registrazioni manuali, non generate da procedure automatiche; b) registrazioni effettuate in giorni festivi o fuori dall'orario ordinario; c) registrazioni con importi tondi al di sopra di [SOGLIA]; d) registrazioni con data operazione distante oltre [N] giorni dalla data di registrazione; e) registrazioni con descrizione assente, generica o non intelligibile; f) registrazioni effettuate da utenti che compiono poche operazioni o che non risultano abitualmente addetti alla contabilità; g) registrazioni con contropartite contabili insolite rispetto alla frequenza osservata nel periodo; h) registrazioni con importo superiore a [SOGLIA]; i) registrazioni di rettifica, storno o inversione di precedenti scritture; j) registrazioni concentrate negli ultimi giorni del periodo; k) registrazioni che movimentano direttamente conti di patrimonio netto, fondi, o conti transitori e sospesi.
- Per i conti transitori e i conti in sospeso, esponi la movimentazione e il saldo residuo, segnalando le partite non chiuse e la loro anzianità.
- Elenca le registrazioni che compaiono in più di una delle categorie precedenti, in ordine di numero di criteri soddisfatti.
Esponi i criteri e le soglie che hai applicato. Il risultato del punto 5 è la mia priorità di selezione per l'esame documentale.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
```

## Output atteso



## Verifica del revisore (obbligatoria prima dell'uso)

l’estrazione è un supporto di selezione. Le registrazioni selezionate vanno esaminate sui documenti giustificativi originali. La logica di estrazione va verificata su un sottoinsieme di controllo di cui si conosca l’esito atteso.

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
