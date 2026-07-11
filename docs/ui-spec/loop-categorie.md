# Loop categorie

Caroselli e loop di navigazione per macro-categorie, discovery e browsing per tipo.

---

## BLOCK-002 — Horizontal discovery rail + suggestion list

### Descrizione
Rail orizzontale di card con immagine e label, seguita da una lista verticale di query tappabili. Il blocco guida la scoperta con browsing visuale sopra e azione rapida sotto.

### Geometrie precise

#### Rail orizzontale (zona superiore)

| Elemento | Misura relativa |
|---|---|
| Lato card | `5rem–6rem`, ratio `1:1` |
| Gap tra card | `0.5rem–0.75rem` |
| Padding laterale rail | `0.75rem–1rem` |
| Immagine | Full-card · border-radius `0.5rem–0.625rem` |
| Label testo | `0.7rem–0.75rem` · 1 riga troncata · centrata |
| Gap immagine → label | `0.25rem–0.375rem` |
| Card visibili | `4–5` intere + overflow parziale |

#### Suggestion list (zona inferiore)

| Elemento | Misura relativa |
|---|---|
| Altezza riga | `2.75rem–3.25rem` |
| Padding riga | `0.75rem–1rem` laterale |
| Testo query | `0.875rem–1rem` |
| Icona trailing | `1rem–1.25rem` |
| Divisore | `1px` full-width |
| Numero righe visibili | `4–6` |

### Target devices
Mobile + tablet. Desktop opzionale, ma non prioritario.

### Posizione tipica
Mid-page / sezione discovery — dopo un risultato principale o come blocco esplorativo secondario.

### Formato compatto
Rail: card `1:1` da `5rem–6rem`, gap `0.5rem–0.75rem`, padding-left `0.75rem–1rem`, label sotto. List: righe alte `2.75rem–3.25rem`, divisori sottili, icona trailing a destra.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-008 — Filtered category carousel con frecce prev/next

### Descrizione
Carosello orizzontale di card categoria con filtro inline (segmented control) nell'header e navigazione esplicita tramite frecce prev/next in basso.

### Geometrie precise

#### Header row

| Elemento | Misura relativa |
|---|---|
| Altezza header row | `2.5rem–3rem` |
| Titolo sezione | `1.25rem–1.5rem` · bold |
| Segmented control | Altezza `2rem–2.25rem` · border-radius `9999px` · padding interno `0.5rem–0.75rem` |
| Voce attiva | Pill filled scura |
| Posizione segmented control | Allineato a destra |

#### Griglia card (carousel)

| Elemento | Misura relativa |
|---|---|
| Card intera visibile | `~62%` del viewport |
| Card parziale visibile | `~28%–30%` del viewport |
| Gap tra card | `0.5rem–0.75rem` |
| Padding laterale sinistro | `1rem` |
| Ratio immagine card | `3:4` portrait |
| Altezza immagine | `14rem–17.5rem` |
| Border-radius immagine | `0.75rem–1rem` |
| Label sotto immagine | `1rem–1.125rem` · bold · margin-top `0.5rem` |
| Altezza card totale | `16.25rem–20rem` |

#### Navigazione prev/next

| Elemento | Misura relativa |
|---|---|
| Bottone circolare | Diametro `2.25rem–2.75rem` |
| Icona chevron | `1rem–1.25rem` |
| Gap tra bottoni | `0.5rem–0.75rem` |
| Posizione | Sotto le card · margin-top `0.75rem–1rem` |

### Target devices
Mobile (primario). Su desktop frecce diventano metodo principale.

### Posizione tipica
Mid-page / sezione categoria — dopo l'hero o come blocco di navigazione per macro-categorie.

### Formato compatto
Header con titolo bold + segmented control pill alto `2rem–2.25rem`. Carousel: card principale `62vw`, card successiva parziale `28vw`, gap `0.5rem–0.75rem`, immagini `3:4` con border-radius `0.75rem–1rem`. Frecce ghost circolari `2.25rem–2.75rem` sotto.

### Fonte
Sito web piastrelle/ceramica — mobile (browser iOS), sezione Ambienti

---

## BLOCK-009 — Category showcase numerato

### Descrizione
Carosello orizzontale di card che rappresentano le macro-categorie principali di un portfolio o servizio. Ogni card mostra un'immagine di copertina con un numero gigante sovrapposto in basso al centro.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Numero card visibili | `5` intere contemporaneamente su mobile |
| Larghezza card | `16%–18%` della larghezza disponibile |
| Gap tra card | `0.25rem–0.375rem` |
| Padding laterale blocco | `0.5rem–0.75rem` |
| Ratio immagine | `2:5` o `1:3` portrait stretto |
| Altezza immagine | `10rem–12.5rem` |
| Border-radius top | `0.5rem–0.625rem` |
| Numero overlay | Altezza visiva pari a `40%–50%` dell'altezza immagine |
| Nome categoria | `0.6rem–0.7rem` · bold · max 2 righe |
| Tag descrittivi | `0.55rem–0.6rem` · regular muted |
| Altezza zona testo | `3rem–3.75rem` |
| Altezza card totale | `13.75rem–16.25rem` |

### Target devices
Mobile (primario). Su desktop valutare layout a griglia fissa o carousel con card più larghe.

### Posizione tipica
Homepage / pagina portfolio — sezione navigazione per macro-aree, dopo l'hero.

### Formato compatto
5 card visibili, larghe `16%–18%` con gap `0.25rem–0.375rem`. Immagine portrait stretta `2:5` alta `10rem–12.5rem`, numero overlay molto grande in basso. Nome bold e tag muted sotto.

### Fonte
App/sito portfolio architettura — mobile (screenshot iOS)
