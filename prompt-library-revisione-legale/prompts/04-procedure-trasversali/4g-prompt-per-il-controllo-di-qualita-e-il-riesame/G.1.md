# G.1 — Supporto al responsabile del riesame della qualità (ISQM 2)

> Parte 4 — Procedure trasversali e situazioni particolari · 4.G — Prompt per il controllo di qualità e il riesame
> **Fase AuditFlow:** Completamento — vedi [`riferimenti/10-mappatura-auditflow.md`](../../../riferimenti/10-mappatura-auditflow.md)

## Documenti da allegare

- le carte di lavoro dell'incarico già compilate e i memorandum conclusivi; la bozza della relazione; la documentazione dei giudizi significativi.

## Carta di lavoro / output prodotto

Documentazione del riesame della qualità dell'incarico (a cura del responsabile del riesame) — bozza da compilare a partire dai documenti sopra indicati; l’evidenza resta il documento sottostante e la carta di lavoro va verificata e sottoscritta dal revisore.

## Prompt

```
Ruolo e contesto: Agisci come collaboratore di revisione legale che supporta procedure trasversali o situazioni particolari dell'incarico.
Documenti allegati a questa istanza: le carte di lavoro dell'incarico già compilate e i memorandum conclusivi; la bozza della relazione; la documentazione dei giudizi significativi.

Sono il responsabile del riesame della qualità dell'incarico. Aiutami a preparare il riesame sui giudizi significativi.
- Elenca i giudizi significativi rilevabili dalle carte di lavoro (significatività, valutazione del rischio, stime, continuità aziendale, frode, giudizio) e, per ciascuno, l'evidenza richiamata.
- Individua i punti in cui la conclusione non discende chiaramente dall'evidenza descritta, o in cui l'evidenza risulti ottenuta o elaborata con l'ausilio dell'agente senza una verifica documentata.
- Formula le domande da porre al responsabile dell'incarico.
Non esprimere una valutazione di qualità: il riesame e le conclusioni sono del responsabile del riesame. Non riscrivere le carte di lavoro.

Vincoli permanenti: Opera esclusivamente sul fascicolo di questa società e di questo team. Basa ogni affermazione solo sui documenti forniti, citando per ciascuna il documento di provenienza. Se un'informazione necessaria non è presente, dichiarala come lacuna: non colmarla con ipotesi. Non esprimere conclusioni di revisione, giudizi di adeguatezza o valutazioni di ragionevolezza.
Vincolo anti-allucinazione: Non citare numeri di paragrafo di principi di revisione o contabili se non sei certo. Se un'informazione ti manca, dichiaralo esplicitamente invece di ipotizzarla. Distingui chiaramente ciò che deriva dal testo che ti ho fornito da ciò che aggiungi tu.
Formato atteso: elenco dei giudizi significativi e domande per il riesame.
```

## Output atteso

elenco dei giudizi significativi e domande per il riesame.

## Verifica del revisore (obbligatoria prima dell'uso)

la valutazione obiettiva è del responsabile del riesame, che non è membro del team dell'incarico (ISQM Italia 2).

## Personalizzazione

Adatta le parti tra parentesi quadre e i riferimenti a documenti/carte di lavoro alla nomenclatura interna dello Studio. Il "Ruolo e contesto" e i "Vincoli permanenti" in testa al prompt possono essere spostati nelle istruzioni di sistema dell'agente se questo viene configurato in modo persistente per l'incarico; in tal caso il prompt operativo può limitarsi al testo centrale.
