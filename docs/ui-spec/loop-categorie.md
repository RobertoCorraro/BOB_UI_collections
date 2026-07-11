# Loop categorie

Caroselli e loop di navigazione per macro-categorie, discovery e browsing per tipo.

---

## BLOCK-002 — Horizontal discovery rail + suggestion list

### Descrizione
Rail orizzontale di card con immagine e label, seguita da una lista verticale di query tappabili. Il blocco guida la scoperta con browsing visuale sopra e azione rapida sotto.

### Geometrie precise

#### Rail orizzontale (zona superiore)

| Elemento | Misura |
|---|---|
| Altezza card | **80–96px** (card compatta, quasi quadrata) |
| Larghezza card | **80–96px** — ratio **1:1** |
| Gap tra card | **8–12px** |
| Padding laterale rail | **12–16px** da sinistra |
| Immagine | Full-card, ratio 1:1 · border-radius **8–10px** |
| Label testo | Sotto l'immagine · font-size **0.7–0.75rem** · centrata · 1 riga troncata · colore dark |
| Gap immagine → label | **4–6px** |
| Card visibili | **4–5 card intere** + overflow parziale a destra |

#### Suggestion list (zona inferiore)

| Elemento | Misura |
|---|---|
| Altezza riga | **44–52px** (touch target minimo 44px) |
| Padding riga | **12–16px** laterale · **0** verticale (altezza fissa) |
| Testo query | Font-size **0.875–1rem** · regular · colore dark |
| Icona trailing | Freccia `→` o chevron `>` · **16–20px** · colore muted · allineata destra |
| Divisore | Linea 1px grigio chiaro · full-width |
| Numero righe visibili | **4–6 righe** dipende dal viewport |

### Target devices
Mobile + tablet. Desktop opzionale, ma non prioritario.

### Posizione tipica
Mid-page / sezione discovery — dopo un risultato principale o come blocco esplorativo secondario.

### Formato compatto
Rail: card 1:1 ~88px, gap 8–12px, padding-left 16px, label sotto 0.75rem. List: righe 44–52px, divisori 1px, icona trailing destra.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-008 — Filtered category carousel con frecce prev/next

### Descrizione
Carosello orizzontale di card categoria con filtro inline (segmented control) nell'header e navigazione esplicita tramite frecce prev/next in basso.

### Geometrie precise

#### Header row

| Elemento | Misura |
|---|---|
| Altezza header row | **40–48px** |
| Titolo sezione | Font-size **1.25–1.5rem** · bold · allineato sinistra |
| Segmented control | Altezza **32–36px** · border-radius **20px** (pill) · padding interno **8–12px** laterale |
| Voce inattiva | Testo dark · nessuno sfondo |
| Voce attiva | Pill filled scura (dark/nero) · testo bianco bold |
| Posizione segmented control | Allineato a destra nella header row |

#### Griglia card (carousel)

| Elemento | Misura |
|---|---|
| Colonna sinistra (card intera) | **~62% viewport** |
| Colonna destra (card overflow) | **~28–30% viewport** visibile (card destra tronca ~65% nascosta) |
| Gap tra card | **8–12px** |
| Padding laterale sinistro | **16px** |
| Ratio immagine card | **3:4** portrait |
| Altezza immagine su mobile | ~**220–280px** |
| Border-radius immagine | **12–16px** |
| Label sotto immagine | Font-size **1–1.125rem** · bold · colore dark · margin-top **8px** |
| Altezza card totale | ~**260–320px** (immagine + label) |

#### Navigazione prev/next (sotto le card)

| Elemento | Misura |
|---|---|
| Bottone circolare | Diametro **36–44px** · border 1px grigio · sfondo trasparente (ghost) |
| Icona chevron | **16–20px** · colore dark |
| Gap tra i due bottoni | **8–12px** |
| Posizione | Bottom-left, sotto le card · margin-top **12–16px** |

### Target devices
Mobile (primario). Su desktop frecce diventano metodo principale.

### Posizione tipica
Mid-page / sezione categoria — dopo l'hero o come blocco di navigazione per macro-categorie.

### Formato compatto
Header: titolo bold + segmented control pill 32px destra. Carousel: card sinistra 62% + destra overflow 28%, ratio 3:4, border-radius 12–16px, label bold sotto. Prev/next ghost circolari 40px bottom-left.

### Fonte
Sito web piastrelle/ceramica — mobile (browser iOS), sezione Ambienti

---

## BLOCK-009 — Category showcase numerato

### Descrizione
Carosello orizzontale di card che rappresentano le macro-categorie principali di un portfolio o servizio. Ogni card mostra un'immagine di copertina con un numero gigante sovrapposto in basso al centro.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Numero card visibili | **5 card intere** contemporaneamente su mobile (375px) |
| Larghezza card | ~**64–68px** (375px ÷ 5 card − gap) |
| Gap tra card | **4–6px** |
| Padding laterale blocco | **8–12px** |
| Ratio immagine | **2:5** o **1:3** portrait stretto |
| Altezza immagine | ~**160–200px** · border-radius top **8–10px** |
| Numero overlay | Font-size ~**40–60% altezza card** · sans-serif extrabold/black · bianco · opacity **0.85–1** · centrato bottom |
| Nome categoria | Font-size **0.6–0.7rem** · bold · centrato · sotto l'immagine · max 2 righe |
| Tag descrittivi | Font-size **0.55–0.6rem** · regular · muted/grigio · centrati · sotto il nome · max 2 righe |
| Altezza zona testo | ~**48–60px** |
| Altezza card totale | ~**220–260px** |
| Border-radius card | **8–10px** in alto · **0** o **4px** in basso |

### Schema visivo (5 card su 375px)
```
[  ][  ][  ][  ][  ]
 1    2    3    4    5
~65px ciascuna + gap 5px
```

### Target devices
Mobile (primario). Su desktop valutare layout a griglia fissa o carousel con card più larghe.

### Posizione tipica
Homepage / pagina portfolio — sezione navigazione per macro-aree, dopo l'hero.

### Formato compatto
5 card visibili ~65px wide, gap 4–6px. Immagine portrait 1:3, ~180px alta, border-radius 8px top. Numero overlay bold bianco 50% altezza card, centrato bottom. Nome bold 0.65rem + 2 tag muted 0.6rem sotto.

### Fonte
App/sito portfolio architettura — mobile (screenshot iOS)
