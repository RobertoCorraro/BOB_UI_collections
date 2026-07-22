# Agent Skills — Web Design & UI/UX

Questo file definisce le competenze e i principi operativi da applicare quando si lavora con i blocchi della collezione BOB_UI_collections. Serve come riferimento per agenti AI, designer e developer che usano questa repo.

---

## Core skills

### Lettura del layout
- Identificare la struttura a griglia di un blocco: numero di colonne, gerarchia visiva, distribuzione del peso visivo
- Riconoscere il pattern compositivo (simmetrico, asimmetrico, collage, lista, griglia uniforme)
- Distinguere blocchi orientati alla scoperta (discovery) da blocchi orientati ai risultati (results)

### Ratio e proporzioni
- Applicare ratio standard: `1:1` (quadrato), `4:5` (verticale social), `3:4` (ritratto), `16:9` (landscape), `2:5` e `1:3` (portrait stretto per caroselli compatti)
- Mantenere coerenza di ratio all’interno dello stesso blocco
- Non deformare le immagini: usare sempre `object-fit: cover` con punto focale centrato o definito
- Le proporzioni tra aree (es. colonna sinistra `62%` vs destra `28%`) si esprimono sempre in `%` relativa al contenitore, mai in pixel

### Unità di misura — regola fondamentale

**Non usare mai pixel fissi nelle specifiche geometriche.** Le misure devono essere relative e scalabili:

| Cosa si misura | Unità da usare |
|---|---|
| Testo (font-size, line-height) | `rem` |
| Spaziatura (padding, gap, margin) | `rem` |
| Larghezze di card / colonne | `%` o `vw` |
| Altezze di blocchi / card | `rem` o range descrittivo (`min(52vh, 25rem)`) |
| Icone, avatar, bullet | `rem` |
| Border-radius standard | `rem` (es. `0.75rem`, `1rem`) |
| Border-radius pill | `9999px` |
| Touch target minimo | `2.75rem` (≡ 44px Apple HIG) |
| Ratio immagini | rapporto puro (es. `3:4`) — mai px |

> **Perché:** i pixel fissi non scalano tra device, risoluzioni e zoom. Le unità relative rispettano le preferenze utente, si adattano a tutti i viewport e sono coerenti con il sistema di design.

### Spacing e ritmo visivo
- Usare un sistema di spacing basato su multipli di `0.25rem` (equivalente ai multipli di 4px nella logica 1rem=16px)
- Padding laterale su mobile: `1rem–1.5rem` (equivalente a 16–24px)
- Gap uniforme tra card nello stesso blocco: `0.5rem–0.75rem`
- Distinguere padding interno alla card da gap tra card

### Tipografia nei blocchi
- Titoli delle card: massimo 2 righe, troncati con `text-overflow: ellipsis`
- Metadati secondari: font-size ridotto (`0.75rem` circa), colore secondario
- Label nei rail orizzontali: testo breve, leggibile su sfondo immagine se in overlay
- Uppercase solo per badge, metadati istituzionali e label di sezione — mai per titoli card

### Comportamento responsive
- **Mobile-first**: progettare per `375–390px` larghezza (in pratica: contenitore fluido)
- **Tablet**: adattare il layout espandendo colonne o aumentando dimensione card (`min-width: 48rem`)
- **Desktop**: valutare se il blocco scala o va ripensato in un container dedicato (`min-width: 75rem`)
- I blocchi con scroll orizzontale (rail) sono nativi da touch: su desktop valutare la transizione a griglia
- I breakpoint si esprimono sempre in `rem` (es. `48rem`, `75rem`), mai in px

### Touch e interazione
- Touch target minimo: `2.75rem × 2.75rem` (equivalente a 44×44px, Apple HIG)
- Elementi tappabili chiaramente distinti da decorativi
- Feedback visivo al tap: stato pressed, highlight o ripple
- Evitare elementi interattivi troppo vicini su mobile

---

## Demo HTML — foglio di stile condiviso

Quando si crea o modifica una demo HTML di un blocco (`assets/demo/*.html`), vale una regola aggiuntiva e vincolante:

### Un solo foglio di stile

Tutte le demo HTML devono importare **lo stesso file CSS**: [`assets/demo/bob__demo.css`](assets/demo/bob__demo.css).

- Non creare un file `.css` per singolo blocco.
- Non usare blocchi `<style>` inline nell'HTML.
- Non introdurre framework CSS esterni (Bootstrap, Tailwind, ecc.): il CSS è scritto a mano, coerente con le unità relative descritte sopra. Fa eccezione **Swiper.js** per i soli blocchi carousel che lo richiedono — vedi sotto.

Nel file HTML del blocco, lo stylesheet va importato così (percorso relativo, dato che HTML e CSS vivono entrambi in `assets/demo/`):

```html
<link rel="stylesheet" href="bob__demo.css" />
```

### Naming delle classi

Ogni classe deve seguire la struttura:

```
bob__{nome_classe}_{modificatore}
```

- `nome_classe`: nome del componente/elemento, parole separate da `_` (es. `product_card`, `demo_intro_badge`, `section_header`)
- `modificatore`: opzionale, per varianti di stato o stile (es. `old`, `discount`, `new`)
- Esempi reali già in uso: `.bob__product_card`, `.bob__product_card_img_wrap`, `.bob__product_card_badge_discount`

`bob__demo.css` include anche un set di **primitivi condivisi** (cerca la sezione `PRIMITIVI CONDIVISI` nel file) pensati per essere riusati tra blocchi diversi: `bob__cta_pill` (+ `_filled` / `_outline` / `_outline_light` / `_ghost`), `bob__nav_arrow` (+ `_ghost`), `bob__avatar` (+ `_sm` / `_md` / `_lg`), `bob__rail` / `bob__rail_item` (scroll orizzontale con `scroll-snap`, senza JS), `bob__chip` (+ `_active`), `bob__divider` (+ `_light`).

### Prima di aggiungere un nuovo blocco demo

1. **Controlla prima le classi già presenti** in `bob__demo.css`, inclusi i primitivi condivisi sopra — riusale se coprono il bisogno, non duplicarle con un nome diverso o un valore leggermente differente.
2. Se non esiste una classe adatta al nuovo blocco, **aggiungi la nuova classe direttamente a `bob__demo.css`**, seguendo la naming convention e mantenendo il file ordinato per sezione (usa i separatori a commento `/* ─── Nome sezione ─── */` come già presente nel file).
3. Non creare un secondo file CSS, nemmeno per una demo isolata o sperimentale: `bob__demo.css` resta l'unico foglio di stile per tutte le demo HTML della collezione.
4. Se una classe esistente va bene solo in parte, preferisci aggiungere un **modificatore** (`bob__{nome_classe}_{nuovo_modificatore}`) piuttosto che riscrivere la classe base o crearne una parallela.

### Carousel: CSS scroll-snap prima, Swiper.js solo se serve

Per rail semplici (scroll orizzontale libero, nessun controllo prev/next) usa `bob__rail` / `bob__rail_item` con `scroll-snap` — zero JS, zero dipendenze.

Usa **Swiper.js** (via CDN, solo JS/CSS della libreria, nessun altro framework) solo quando la spec richiede funzionalità che il puro CSS non copre in modo pulito: frecce prev/next con stato disabled, progress bar/pagination sincronizzata, coverflow o card centrale dominante con pannelli laterali. Importa Swiper via CDN direttamente nell'HTML del blocco che lo richiede (non va aggiunto a `bob__demo.css` né reso una dipendenza globale delle altre demo).

---

## Demo HTML — indice (`index.html`)

La repo ha un **indice unico** in `index.html` (root, servito da GitHub Pages) che elenca tutti i blocchi raggruppati per file di spec, con lo stato di ciascuno (`bob__catalog_card_status_ready` se la demo esiste ed è linkata, `bob__catalog_card_status_pending` se manca ancora).

**Ogni volta che si aggiunge, rimuove o sposta una demo HTML in `assets/demo/`, `index.html` va aggiornato nella stessa modifica**:

1. Trova la card del blocco in `index.html` (cercare il numero `BLOCK-0XX`).
2. Se la demo è nuova: cambia il tag da `<span class="bob__catalog_card bob__catalog_card_pending">` ad `<a class="bob__catalog_card bob__catalog_card_ready" href="assets/demo/BLOCK-0XX_nome-file.html">`, e lo stato interno da `bob__catalog_card_status_pending` (testo "In arrivo") a `bob__catalog_card_status_ready` (testo "Demo").
3. Se un blocco nuovo non era ancora presente nell'indice (perché aggiunto ex novo, non dai 23 blocchi già documentati), crea una nuova card nella sezione corretta (o crea una nuova `<section class="bob__catalog_section">` se è un nuovo file di spec).
4. Non lasciare mai `index.html` disallineato con lo stato reale di `assets/demo/`: è l'unico punto di ingresso per vedere le demo via GitHub Pages.

---

## Analisi di nuovi layout → nuovo blocco

Per analizzare un nuovo layout (da descrizione testuale o screenshot) e trasformarlo in un blocco completo (scheda in `docs/ui-spec/`, entry in `docs/ui-spec/README.md`, demo HTML + eventuali classi CSS, voce in `index.html`), usa la skill **layout-capture** (vedi `.claude/skills/layout-capture/SKILL.md` in questa repo). Non improvvisare un formato diverso: la skill applica lo stesso schema a campi fissi già in uso in tutti i blocchi esistenti, cross-referenziando pattern e classi già disponibili prima di introdurne di nuovi.

---

## Pattern di riferimento

### Asymmetric media collage
- Usare quando si vuole presentare un set di contenuti con forte gerarchia visiva
- Il blocco principale deve avere peso visivo dominante
- Layout `50/50`, gap `0.25rem`, zero border-radius, edge-to-edge

### Horizontal discovery rail
- Usare per stimolare la navigazione laterale e la scoperta di categorie correlate
- Le card mostrano parzialmente l’elemento successivo (overflow intenzionale)
- Card `1:1` da `5rem–6rem`, abbinate a lista di query sotto

### Two-column results grid
- Usare per elenchi di risultati omogenei (prodotti, immagini, articoli)
- Card uniformi con altezza percepita costante
- Griglia `1fr 1fr`, gap `0.5rem–0.75rem`, padding laterale `0.75rem–1rem`

---

## Checklist prima di aggiungere un blocco

- [ ] Il blocco ha un nome componente chiaro e univoco
- [ ] Il ratio delle immagini è definito
- [ ] Le geometrie usano esclusivamente unità relative (`rem`, `%`, `vw`, `vh`)
- [ ] I target devices sono specificati
- [ ] La fonte (app o sito) è documentata
- [ ] Il formato compatto è scritto in 1–2 righe
- [ ] Lo screenshot è disponibile o segnato come TODO in `assets/screenshots/`
- [ ] Il blocco è stato testato visivamente su mobile
- [ ] Se è presente una demo HTML, usa `assets/demo/bob__demo.css` e la naming convention `bob__{nome_classe}_{modificatore}`
- [ ] `index.html` riflette lo stato reale della demo (ready/pending)

---

## Principi generali

- **Mobile-first sempre**: se un blocco non funziona su mobile, non entra in collezione
- **Unità relative sempre**: nessun pixel fisso nelle specifiche — solo `rem`, `%`, `vw`, `vh`
- **Fonte reale**: ogni blocco deve provenire da un pattern osservato su un prodotto reale
- **Conversion-oriented**: privilegiare blocchi che guidano l’utente verso un’azione chiara
- **Coerenza visiva**: ratio, spacing e tipografia devono essere coerenti tra i blocchi della stessa pagina
- **No decor fine a se stesso**: ogni elemento visivo deve avere una funzione informativa o di navigazione
