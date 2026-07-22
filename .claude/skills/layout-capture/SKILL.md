---
name: layout-capture
description: Analizza un nuovo layout UI — da descrizione testuale o da uno screenshot — e lo converte in un blocco completo per questa repo (BOB_UI_collections, libreria di pattern UI): scheda di specifica, demo HTML e aggiornamento degli indici. Usa questa skill ogni volta che l'utente descrive un nuovo layout/pattern UI da aggiungere alla collezione, allega o incolla uno screenshot di un'interfaccia chiedendo di "catturarlo", o dice cose come "aggiungi questo layout alla collezione", "cattura questo blocco", "analizza questo screenshot e crea il blocco", "trasforma questa UI in un BLOCK". Attivala anche se l'utente non nomina esplicitamente BOB_UI_collections ma sta chiaramente descrivendo un componente/layout da documentare e prototipare come gli altri blocchi della collezione.
---

# Layout Capture — da layout a blocco BOB_UI_collections

Questa skill trasforma un layout osservato (testo o screenshot) in un blocco documentato e pronto da consultare in questa repo. Applica un metodo di **estrazione strutturata in stile wiki** — ispirato al principio "LLM-WIKI": invece di descrivere il layout con prosa libera, lo si fa aderire a uno **schema fisso** (come una infobox di wiki) e si **riusa il vocabolario già stabilito** dai blocchi esistenti (nomi di pattern, ratio, scala di spaziatura, classi CSS) invece di inventarne uno nuovo per lo stesso concetto. Ogni nuovo blocco si aggancia così alla conoscenza già accumulata nella repo, invece di essere un'isola a sé.

## Perché lo schema fisso conta

Un layout descritto liberamente è difficile da confrontare con gli altri e tende a duplicare concetti già nominati (es. chiamare "carosello" un pattern che altrove si chiama "rail"). Uno schema fisso, applicato sistematicamente, rende ogni blocco: comparabile con gli altri, riutilizzabile nel CSS condiviso, e ricercabile per chi sfoglia la collezione. Per questo ogni passo qui sotto fa esplicito riferimento ai file della repo da leggere prima di scrivere qualsiasi cosa — sono la fonte di verità corrente, non uno snapshot fisso in questa skill.

## Prima di iniziare: leggi lo stato attuale della repo

Non affidarti a memoria o assunzioni: lo stato della repo evolve. Prima di analizzare il nuovo layout, leggi (in questo ordine):

1. **`agent.md`** — regole di design system: unità relative obbligatorie (`rem`, `%`, `vw`, `vh`, mai `px`), scala di spacing, ratio standard, breakpoint responsive (`48rem`, `75rem`), e le sezioni "Demo HTML — foglio di stile condiviso" e "Demo HTML — indice (index.html)", che questa skill deve seguire alla lettera nei passi 4–5.
2. **`assets/demo/bob__demo.css`** — l'unico foglio di stile condiviso da tutte le demo. Contiene sia classi per-blocco sia una sezione "PRIMITIVI CONDIVISI" (cta pill, nav arrow, avatar, rail, chip, divider) da riusare prima di crearne di nuove.
3. **`docs/ui-spec/README.md`** — indice numerato dei blocchi esistenti (per trovare il prossimo numero libero e vedere quali pattern/nomi sono già in uso).
4. Il file tematico più simile in **`docs/ui-spec/*.md`** (hero, navigation, loop-categorie, loop-prodotti, loop-post-editoriali, banner-promo, serp-e-ads, sezioni-testo) per vedere lo stile esatto delle schede esistenti e individuare blocchi simili da cui riusare vocabolario/ratio/classi.

## Passo 1 — Analisi del layout in schema fisso

A partire dal testo o dallo screenshot fornito dall'utente, compila **sempre gli stessi campi**, nello stesso ordine, indipendentemente da quanto è ricco l'input. Se uno screenshot non rende visibile un dato (es. ratio esatto di un'immagine), stimalo dal layout visibile e segnalalo come stima.

Identifica in particolare:
- **Pattern compositivo**: griglia, rail/carosello orizzontale, collage asimmetrico, stack verticale, bento grid, hero fullscreen, tabella testuale, ecc. — usa lo stesso nome che userebbe un blocco esistente simile, non sinonimi a caso.
- **Gerarchia visiva**: cosa domina, cosa è secondario, dove va l'occhio per primo.
- **Struttura**: numero di colonne/zone e loro proporzione (es. `62% / 28%`, `50/50`, griglia `1fr 1fr`).
- **Ratio immagini**: `1:1`, `4:5`, `3:4`, `16:9`, ecc. — mai in pixel.
- **Ruoli tipografici**: titolo, metadati/sottotitolo, prezzo, CTA, badge — e le loro dimensioni relative rispetto a blocchi simili già in collezione.
- **Target devices**: mobile / tablet / desktop, e se il comportamento cambia tra loro.
- **Comportamento**: statico, scroll orizzontale, accordion, drill-down, hover — e se richiede JS o è ottenibile in puro CSS.

Prima di scrivere descrizioni nuove per concetti già visti, controlla se un blocco esistente in `docs/ui-spec/` usa già lo stesso pattern (es. "rail orizzontale" è già BLOCK-002) e cross-referenzialo esplicitamente in una tabella "Differenza da BLOCK-0XX", come fanno già molte schede esistenti — è il modo in cui la repo mantiene i concetti agganciati tra loro invece di duplicarli.

**Output di questo passo**: presenta all'utente un riepilogo strutturato con questi campi esatti, PRIMA di scrivere qualsiasi file (l'utente deve poter correggere l'interpretazione prima che diventi un commit):

```
Descrizione: ...
Geometrie precise: (tabella markdown, unità relative)
Ratio immagini: ...
Target devices: ...
Posizione tipica: ...
Formato compatto: ... (1–2 righe)
Fonte: ... (chiedi all'utente se non deducibile: app/sito osservato)
```

## Passo 2 — Numero e collocazione del blocco

1. Apri `docs/ui-spec/README.md`, trova il numero `BLOCK-0XX` più alto nella tabella "Blocchi per numero" e assegna il successivo.
2. Scegli il file tematico giusto in `docs/ui-spec/` in base al contenuto (non alla forma): un carosello di prodotti va in `loop-prodotti.md`, non necessariamente insieme ad altri caroselli in `loop-categorie.md`. Se nessun file esistente è pertinente, crea un nuovo file `docs/ui-spec/<nome-tema>.md` seguendo l'intestazione delle altre schede e aggiungilo alla tabella "File" in `docs/ui-spec/README.md`.

## Passo 3 — Scrivi la scheda di specifica

Aggiungi al file scelto una sezione `## BLOCK-0XX — Nome del blocco` con **esattamente** questi campi, nello stesso ordine e formato delle schede esistenti (guarda una scheda vicina come modello di formattazione esatta):

- `### Descrizione`
- `### Geometrie precise` — tabella markdown `| Elemento | Misura relativa |`, solo `rem`/`%`/`vw`/`vh`, mai `px`
- `### Ratio immagini` (se rilevante, altrimenti ometti)
- `### Target devices`
- `### Posizione tipica`
- `### Formato compatto`
- `### Fonte`

Se il blocco è concettualmente vicino a uno esistente, aggiungi anche una tabella `### Differenza da BLOCK-0XX` come fanno più schede della repo.

## Passo 4 — Crea la demo HTML

Crea `assets/demo/BLOCK-0XX_slug-descrittivo.html`:

- Importa **solo** `assets/demo/bob__demo.css` (`<link rel="stylesheet" href="bob__demo.css" />`), percorso relativo perché entrambi i file vivono in `assets/demo/`. Nessun `<style>` inline, nessun framework CSS esterno (Bootstrap, Tailwind), a parte l'eccezione Swiper.js descritta sotto.
- Usa **solo** classi `bob__{nome_classe}_{modificatore}`. Prima riusa quelle già in `bob__demo.css` (in particolare i primitivi condivisi: `bob__cta_pill`, `bob__nav_arrow`, `bob__avatar`, `bob__rail`/`bob__rail_item`, `bob__chip`, `bob__divider`). Aggiungi nuove classi a `bob__demo.css` solo se davvero manca l'equivalente, mantenendo la naming convention e i separatori a commento per sezione già presenti nel file.
- CSS moderno e responsivo: Grid/Flexbox, `clamp()` dove utile, breakpoint a `48rem`/`75rem` coerenti con `agent.md`. Per rail semplici (scroll orizzontale senza controlli espliciti) usa `bob__rail` con `scroll-snap` — zero JS.
- **Swiper.js** (via CDN, solo per l'HTML di quel blocco, mai aggiunto a `bob__demo.css` come dipendenza globale) solo se il blocco richiede davvero frecce prev/next con stato disabled, una pagination/progress bar sincronizzata, o un effetto coverflow/card-centrale — cose che il puro CSS non copre in modo pulito. Se un semplice scroll-snap basta, preferiscilo: meno dipendenze, più leggero.
- Popola il markup con contenuti placeholder plausibili (testo realistico nella lingua della repo, immagini da un placeholder service tipo picsum.photos con seed stabili) — segui lo stile già usato in `BLOCK-003_two-column-results-grid.html` come riferimento di qualità/tono.
- Verifica mentalmente (o descrivendo il comportamento atteso) che il layout regga su mobile (~375–390px), tablet (`≥48rem`) e desktop (`≥75rem`) prima di considerarlo finito.

## Passo 5 — Aggiorna gli indici

Due file vanno aggiornati nella stessa modifica, mai lasciati disallineati:

1. **`docs/ui-spec/README.md`** — aggiungi una riga alla tabella "Blocchi per numero" con numero, nome e file.
2. **`index.html`** (root della repo) — trova (o crea, se il blocco non era già in indice) la card `BLOCK-0XX`: cambia il tag da `<span class="bob__catalog_card bob__catalog_card_pending">` ad `<a class="bob__catalog_card bob__catalog_card_ready" href="assets/demo/BLOCK-0XX_slug.html">`, e lo stato da `bob__catalog_card_status_pending`/"In arrivo" a `bob__catalog_card_status_ready`/"Demo". Se la sezione tematica corretta non esiste ancora in `index.html`, crea una nuova `<section class="bob__catalog_section">` seguendo lo schema delle sezioni esistenti.

## Passo 6 — Riepilogo finale

Chiudi con un breve riepilogo per l'utente: numero blocco assegnato, file toccati (scheda, demo HTML, eventuali nuove classi in `bob__demo.css`, indici aggiornati), e un'unica frase su eventuali scelte non ovvie fatte durante l'analisi (es. "ho stimato il ratio immagine a 4:5 non essendo misurabile nello screenshot").

## Note

- Se l'utente fornisce solo un'idea vaga ("un carosello di offerte tipo quello di Amazon"), chiedi uno screenshot o una descrizione più precisa della struttura prima di inventare geometrie — le misure relative in `docs/ui-spec/` devono riflettere un pattern osservato reale, non un'invenzione (vedi principio "Fonte reale" in `agent.md`).
- Se il layout non si adatta a nessuna categoria esistente e nemmeno giustifica un nuovo file tematico, chiedi conferma prima di crearne uno: meglio consolidare in un file esistente se il tema è affine.
