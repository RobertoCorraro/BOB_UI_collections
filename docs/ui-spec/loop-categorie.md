# Loop categorie

Caroselli e loop di navigazione per macro-categorie, discovery e browsing per tipo.

---

## BLOCK-002 — Horizontal discovery rail + suggestion list

### Descrizione
Rail orizzontale di card con immagine e label, seguita da una lista verticale di query tappabili. Il blocco guida la scoperta con browsing visuale sopra e azione rapida sotto.

### Ratio immagini
Card del rail 1:1.

### Target devices
Mobile + tablet. Desktop opzionale, ma non prioritario.

### Posizione tipica
Mid-page / sezione discovery — dopo un risultato principale o come blocco esplorativo secondario.

### Formato compatto
1 riga scrollabile di card 1:1 con titolo sotto, seguita da lista di righe tappabili con divisori sottili e icona trailing a destra.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-008 — Filtered category carousel con frecce prev/next

### Descrizione
Carosello orizzontale di card categoria con filtro inline (segmented control) nell'header e navigazione esplicita tramite frecce prev/next in basso. Il blocco combina tre livelli: header con titolo + filtro, griglia di card con overflow intenzionale, e controlli di navigazione separati. È pensato per la navigazione per categoria in contesti editoriali o di prodotto.

### Struttura (3 livelli)
- **Header row**: titolo sezione (display, bold, allineato a sinistra) + segmented control pill a destra (es. "EFFETTI" inattivo / "AMBIENTI" attivo con pill scura filled). Il filtro cambia il set di card senza navigare altrove
- **Griglia card**: 2 colonne asimmetriche — colonna sinistra ~62% (card intera visibile), colonna destra overflow oltre il bordo (~65% visibile). Overflow intenzionale che comunica la presenza di altri item e invita allo swipe/click
- **Navigazione prev/next**: due bottoni circolari ghost/outline (bordo grigio sottile, sfondo trasparente, icona chevron ← →), posizionati in basso a sinistra sotto le card, non sovrapposti al contenuto

### Card
- **Struttura**: immagine ambientazione con angoli arrotondati + label testuale grande sotto (es. "Outdoor", "Cucina"), stile editoriale pulito
- **Nessun overlay, bottone o metadato** sull'immagine — la card è tappabile nella sua interezza
- **Ratio immagine**: ~3:4 (portrait), immagine alta e dominante

### Card visibili all'avvio
**1 card intera + 1 card parziale** (~65% visibile) — totale 2 elementi percepiti, 1 completo

### Navigazione
| Metodo | Tipo | Posizione |
|---|---|---|
| Touch swipe | Gesture orizzontale | Sull'area card |
| Freccia → | Tap bottone ghost circolare | Bottom-left, sotto le card |
| Freccia ← | Tap bottone ghost circolare | Bottom-left, accanto alla → |

### Segmented control (filtro)
- 2 voci: voce inattiva = solo testo, voce attiva = pill scura filled con testo bianco bold
- Cambia la categoria del carousel (es. da "Ambienti" a "Effetti") senza page reload
- Posizionato in alto a destra, allineato con il titolo sezione

### Target devices
Mobile (primario). Su desktop le frecce diventano il metodo principale; lo swipe rimane disponibile su touch screen.

### Posizione tipica
Mid-page / sezione categoria — dopo l'hero o come blocco di navigazione per macro-categorie di prodotto o contenuto editoriale.

### Formato compatto
Header: titolo display bold + segmented control pill. Carousel: 1 card intera + 1 parziale, immagini portrait 3:4, label sotto. Navigazione: frecce ghost circolari bottom-left.

### Fonte
sito web piastrelle/ceramica — mobile (browser iOS), sezione Ambienti

---

## BLOCK-009 — Category showcase numerato

### Descrizione
Carosello orizzontale di card che rappresentano le **macro-categorie** principali di un portfolio o servizio. Ogni card mostra un'immagine di copertina rappresentativa della categoria, con un numero gigante sovrapposto che ne indica l'ordine/ranking visivo. Il numero funge simultaneamente da elemento grafico decorativo e da wayfinding — l'utente sa sempre a che posizione si trova senza dots o indicatori separati. È un blocco ad alto impatto editoriale, tipico di portfolio creativi, architettura e design.

### Struttura card
- **Immagine di copertina**: foto editorial/progetto emblematico della categoria, full-height della card, angoli arrotondati in alto
- **Numero overlay**: cifra gigante (display extrabold/black, bianca, semi-trasparente), posizionata in basso al centro sull'immagine — dimensione ~40–50% dell'altezza card, stile puramente decorativo/wayfinding
- **Nome categoria**: titolo bold centrato sotto l'immagine, 1–2 righe (es. "House of Culture & Art")
- **2 tag descrittivi**: testo muted/grigio sotto il nome — tipo progetto + sotto-categoria (es. "Graduation Project / Cultural Design")
- **Nessun bottone esplicito**: intera card tappabile → porta all'archivio filtrato per quella categoria

### Differenza da BLOCK-008 (Filtered category carousel)

| | BLOCK-008 | BLOCK-009 |
|---|---|---|
| Contenuto card | Singolo prodotto/item | Categoria intera |
| CTA | Arrow prev/next + filtro segmented | Tap → pagina categoria |
| Navigazione | Filtro per tipo | Browse categorizzato |
| Numero overlay | Indicatore posizione nel carousel | Ranking/ordine della categoria |
| Card visibili | 1 intera + 1 parziale | 5 intere (layout stretto) |

### Card visibili all'avvio
**5 card intere** — layout a card strette (ratio ~1:3 o 2:5 portrait), tutte visibili contemporaneamente su mobile senza overflow

### Ratio immagine
~**2:5** o **1:3** portrait stretto — card molto alte e sottili, ottimizzate per mostrare più categorie insieme

### Navigazione
Touch swipe orizzontale. Nessun prev/next esplicito (a differenza di BLOCK-008).

### Target devices
Mobile (primario). Su desktop valutare layout a griglia fissa o carousel con card più larghe.

### Posizione tipica
Homepage / pagina portfolio — sezione di navigazione per macro-aree, dopo l'hero o come entry point alle categorie principali.

### Formato compatto
Carosello orizzontale, 5 card portrait strette (ratio ~1:3). Ogni card: immagine full-height + numero gigante overlay bottom-center + nome categoria bold + 2 tag muted sotto. Nessun bottone, card intera tappabile.

### Fonte
App/sito portfolio architettura — mobile (screenshot iOS)
