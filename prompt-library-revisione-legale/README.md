# Libreria Prompt — Revisione Legale con supporto AI

Libreria interna di **177 schede-prompt** per l'utilizzo di un agente AI a supporto della revisione legale, organizzata per fase dell'incarico, con relativa **app master** per la consultazione, la ricerca e la gestione delle schede.

Questa libreria nasce dall'estrazione e dall'espansione dei prompt contenuti nel *Manuale AI Revisione Legale v1.0*: ogni riferimento al marchio/modello proprietario originario è stato rimosso e sostituito con formulazioni generiche, adattabili al modello di carte di lavoro effettivamente in uso presso lo Studio. Ogni prompt è stato inoltre **espanso** rispetto al testo sorgente con un'impalcatura esplicita di ruolo/contesto, i vincoli permanenti e il vincolo anti-allucinazione, così da essere autosufficiente anche se usato al di fuori di un agente pre-configurato con istruzioni di sistema persistenti.

## Struttura

```
prompt-library-revisione-legale/
├── README.md                      ← questo file
├── app/                           ← app master (consultazione/ricerca/gestione)
│   ├── index.html
│   └── prompts-data.js            ← dati delle 177 schede (generati, non modificare a mano)
├── riferimenti/                   ← principi, governance, glossario, modulistica
│   ├── 01-principi-generali-e-regole-di-utilizzo.md
│   ├── 02-configurazione-agente-e-limiti.md
│   ├── 03-governance-qualita-e-monitoraggio.md
│   ├── 04-riservatezza-e-quadro-normativo.md
│   ├── 05-formazione-e-riconoscimento-errori.md
│   ├── 06-glossario.md
│   ├── 07-documentazione-standard-per-fase.md
│   ├── 08-regole-di-verifica-per-tipologia-di-output.md
│   └── 09-modulistica.md
└── prompts/                       ← le 177 schede, un file .md per scheda
    ├── 01-accettazione-incarico-e-rischio/     (19 schede — 1.A–1.E)
    ├── 02-verifiche-periodiche/                (17 schede — 2.A–2.D)
    ├── 03-bilancio-di-esercizio/               (30 schede — 3.A–3.D)
    ├── 04-procedure-trasversali/               (42 schede — 4.A–4.G)
    └── 05-note-e-memo-di-lavoro/               (69 schede — 5.A–5.H)
```

Ogni cartella di Parte è suddivisa in sottocartelle per Fase (es. `1a-controllo-preliminare-di-conformita-documentale`), rispecchiando la struttura originaria del manuale, per rendere prevedibile la posizione di ogni scheda anche navigando da riga di comando o su GitHub.

## App master

Apri [`app/index.html`](app/index.html) in un browser (nessuna installazione, nessuna dipendenza esterna, funziona anche offline aprendo il file direttamente). Consente di:

- **Navigare** l'albero Parte → Fase nella barra laterale;
- **Cercare** per codice, titolo o contenuto del prompt;
- **Aprire** una scheda e vedere documenti da allegare, output prodotto, prompt pronto all'uso, output atteso e verifica obbligatoria del revisore;
- **Copiare** il prompt espanso negli appunti o **esportarlo** come file `.txt`;
- **Salvare preferiti** e **annotazioni personali** per scheda (salvati localmente nel browser, non condivisi né inviati altrove);
- Vedere l'elenco delle schede **usate di recente**.

L'app legge i dati da `app/prompts-data.js`, generato automaticamente dal contenuto di `prompts/`. Se una scheda `.md` viene modificata a mano, rigenerare questo file (vedi § Manutenzione) per tenerlo allineato.

## Come si usa una scheda

1. Apri l'app o il file `.md` della scheda che ti serve (l'app è il modo più rapido per trovarla).
2. Verifica di avere a disposizione i **documenti da allegare** indicati.
3. Copia il **prompt** nell'agente AI in uso, insieme ai documenti-fonte pertinenti (mai le carte di lavoro: quelle sono l'output, non l'input).
4. Al termine, esegui la **verifica del revisore** indicata in coda alla scheda prima di far confluire qualunque contenuto in carta di lavoro.
5. Documenta l'utilizzo secondo la formula standard in [`riferimenti/09-modulistica.md`](riferimenti/09-modulistica.md).

Prima di usare la libreria, leggi almeno [`riferimenti/01-principi-generali-e-regole-di-utilizzo.md`](riferimenti/01-principi-generali-e-regole-di-utilizzo.md): stabilisce cosa l'agente può e non può fare, la struttura R-C-C-V-F per costruire prompt efficaci, e la procedura di verifica obbligatoria prima di inserire qualunque output in carta di lavoro. **L'agente non è mai una fonte di evidenza di revisione**: ogni output è una bozza non verificata, e la responsabilità professionale resta sempre del revisore che firma.

## Manutenzione

I file in `prompts/*.md` e `app/prompts-data.js` sono generati da uno script di estrazione a partire dal manuale sorgente. Per aggiungere una nuova scheda:

- manualmente: crea il file `.md` nella sottocartella di Fase corretta seguendo il template delle schede esistenti, poi aggiorna `app/prompts-data.js` con il record corrispondente (stesso schema JSON: `id`, `codice`, `nome`, `parte`, `fase`, `parte_folder`, `fase_folder`, `file`, `documenti`, `output_prodotto`, `prompt`, `prompt_originale`, `output_atteso`, `verifica`);
- oppure ripeti l'estrazione automatica se disponi dello script sorgente, che rigenera entrambi in modo coerente.

## Approvazione e controllo delle versioni

| Versione | Data | Redazione | Verifica | Approvazione | Modifiche rispetto alla precedente |
| --- | --- | --- | --- | --- | --- |
| 1.0 | 2026-08-10 | | | | Prima emissione della libreria: estrazione, generalizzazione ed espansione dei 177 prompt, riferimenti di governance e app master |
| | | | | | |

Riesame previsto: con periodicità almeno annuale e comunque a ogni modifica dei principi di revisione applicabili, a ogni aggiornamento rilevante della configurazione dell'agente, a seguito di incidenti sistematici e a seguito di rilievi in sede di monitoraggio interno o di ispezione esterna (vedi [`riferimenti/03-governance-qualita-e-monitoraggio.md`](riferimenti/03-governance-qualita-e-monitoraggio.md)).
