# BOB_UI_collections

Raccolta di blocchi UI di riferimento ispirati a pattern reali trovati su app e siti mobile. Ogni blocco è documentato con campi standard per facilitare il reuso, la prototipazione e la comunicazione con il team di sviluppo.

---

## Struttura della repo

```
BOB_UI_collections/
├── README.md
├── docs/
│   └── ui-spec.md          # Specifiche dei blocchi UI
├── assets/
│   └── screenshots/        # Screenshot di riferimento per ogni blocco (vedi sotto)
└── agent.md                # Skills di web design e UI/UX per l'utilizzo dei blocchi
```

---

## Campi per ogni blocco

Ogni blocco nella collezione deve essere documentato con i seguenti campi:

| Campo | Descrizione |
|---|---|
| `Nome componente` | Nome identificativo del blocco |
| `Descrizione` | Scopo e struttura del blocco |
| `Struttura card` | Dettaglio degli elementi interni alla card (se presente) |
| `Ratio immagini` | Proporzioni delle immagini usate nel blocco |
| `Target devices` | Dispositivi consigliati: mobile / tablet / desktop |
| `Formato compatto` | Sintesi visiva del layout in una riga |
| `Fonte` | App o sito dove il pattern è stato osservato |
| `Screenshot` | Riferimento al file immagine in `assets/screenshots/` |

---

## Screenshot di riferimento

> ⚠️ **Work in progress** — La cartella `assets/screenshots/` è predisposta per accogliere gli screenshot di riferimento per ogni blocco. I file devono essere caricati manualmente seguendo la naming convention:
>
> ```
> BLOCK-001_asymmetric-media-collage.jpeg
> BLOCK-002_discovery-rail.jpeg
> BLOCK-003_two-column-grid.jpeg
> BLOCK-004_people-suggestion-carousel.jpeg
> ```

---

## Come aggiungere un nuovo blocco

1. Aggiungi la scheda in `docs/ui-spec.md` con tutti i campi obbligatori
2. Carica lo screenshot in `assets/screenshots/` con la naming convention `BLOCK-XXX_nome-blocco.jpeg`
3. Aggiorna la lista screenshot in questo README
