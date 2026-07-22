# BOB_UI_collections

Raccolta di blocchi UI di riferimento ispirati a pattern reali trovati su app e siti mobile. Ogni blocco è documentato con campi standard per facilitare il reuso, la prototipazione e la comunicazione con il team di sviluppo.

---

## Struttura della repo

```
BOB_UI_collections/
├── README.md
├── agent.md                # Skills di web design e UI/UX, incluse le regole per le demo HTML
├── docs/
│   └── ui-spec/
│       ├── README.md           # Indice dei blocchi per numero e file
│       ├── hero.md
│       ├── navigation.md
│       ├── loop-categorie.md
│       ├── loop-prodotti.md
│       ├── loop-post-editoriali.md
│       ├── banner-promo.md
│       └── serp-e-ads.md
└── assets/
    ├── screenshots/            # Screenshot di riferimento per ogni blocco
    └── demo/                   # Demo HTML standalone dei blocchi
        ├── bob__demo.css           # Stylesheet condiviso da tutte le demo
        └── BLOCK-003_two-column-results-grid.html
```

---

## Campi per ogni blocco

Ogni blocco deve essere documentato con i seguenti campi:

| Campo | Descrizione |
|---|---|
| `Descrizione` | Scopo e struttura del blocco |
| `Geometrie precise` | Misure in unità relative (vedi convenzioni sotto) |
| `Ratio immagini` | Proporzioni delle immagini nel blocco |
| `Target devices` | Mobile / tablet / desktop |
| `Posizione tipica` | Dove compare nella pagina |
| `Formato compatto` | Sintesi del layout in 1–2 righe |
| `Fonte` | App o sito dove il pattern è stato osservato |

---

## Convenzioni di misura

Le specifiche geometriche usano esclusivamente **unità relative**. I pixel fissi non sono usati nelle specifiche, perché non scalano tra device e densità di schermo diverse.

| Cosa si misura | Unità preferita | Esempi |
|---|---|---|
| Dimensioni testo | `rem` | `0.875rem`, `1.25rem` |
| Spaziature, padding, gap | `rem` | `0.5rem`, `1rem`, `1.5rem` |
| Larghezze di card o colonne | `%` o `vw` | `50%`, `62%`, `44vw` |
| Altezze di blocco o card | `rem` o proporzione descrittiva | `14rem`, `min(52vh, 25rem)` |
| Icone e avatar | `rem` | `1.5rem`, `4.5rem` |
| Border-radius | `rem` o `9999px` per pill | `0.75rem`, `9999px` |
| Ratio immagini | rapporto (es. `16:9`, `3:4`) | non usare px |
| Touch target minimo | `2.75rem` (44px equivalente) | da Apple HIG / Material Design |

> **Regola base:** se una misura cambia tra un iPhone 14 e un iPhone 16 Pro Max, va espressa in unità relative, non in pixel.

---

## Demo HTML dei blocchi

Ogni blocco documentato in `docs/ui-spec/` può avere una demo HTML standalone in `assets/demo/`, per rendere la specifica immediatamente previewabile (es. via GitHub Pages) senza affidarsi solo a uno screenshot.

**Tutte le demo condividono un unico foglio di stile**: [`assets/demo/bob__demo.css`](assets/demo/bob__demo.css). Nessuna demo ha CSS inline o un file `.css` proprio, e non vengono usati framework esterni (Bootstrap, Tailwind, ecc.).

Le classi seguono la naming convention:

```
bob__{nome_classe}_{modificatore}
```

Es. `.bob__product_card`, `.bob__product_card_img_wrap`, `.bob__product_card_badge_discount`.

Quando si aggiunge un nuovo blocco demo: riusare le classi già presenti in `bob__demo.css` se coprono il bisogno; se non esiste una classe adatta, estendere `bob__demo.css` con nuove classi/modificatori coerenti con la convenzione, invece di creare un nuovo file CSS. La regola completa, pensata per agenti AI, è in [`agent.md`](agent.md#demo-html--foglio-di-stile-condiviso).

---

## Screenshot di riferimento

> ⚠️ **Work in progress** — La cartella `assets/screenshots/` è predisposta per gli screenshot di ogni blocco. Naming convention:
>
> ```
> BLOCK-001_asymmetric-media-collage.jpeg
> BLOCK-002_discovery-rail.jpeg
> BLOCK-003_two-column-grid.jpeg
> ...
> ```

---

## Come aggiungere un nuovo blocco

1. Scegli il file tematico corretto in `docs/ui-spec/`
2. Aggiungi la scheda con tutti i campi obbligatori
3. Usa **solo unità relative** nelle geometrie
4. Carica lo screenshot in `assets/screenshots/` con la naming convention
5. Se aggiungi anche una demo HTML, seguine le regole in [`agent.md`](agent.md#demo-html--foglio-di-stile-condiviso): stesso `bob__demo.css`, naming `bob__{nome_classe}_{modificatore}`
6. Aggiorna l'indice in `docs/ui-spec/README.md`
