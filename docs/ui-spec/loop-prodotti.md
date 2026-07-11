# Loop prodotti

Griglie, caroselli e card per listing e visualizzazione di prodotti, risultati e destinazioni.

---

## BLOCK-003 — Two-column results grid

### Descrizione
Griglia simmetrica a 2 colonne con card uniformi, media sopra e testo sotto. Il blocco è adatto a collezioni di risultati perché facilita scansione, confronto e ripetizione visiva.

### Ratio immagini
1:1 oppure 4:5.

### Target devices
Mobile + tablet + desktop.

### Posizione tipica
Pagina risultati / listing page — corpo centrale della pagina, dopo filtri o header di sezione.

### Formato compatto
Griglia 2 colonne con card uniformi, immagini 1:1 o 4:5, titolo troncato e metadati sotto. Layout ripetitivo, ordinato e facilmente scalabile.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-007 — Destination detail card

### Descrizione
Card informativa per una destinazione di viaggio con immagine, dati essenziali (prezzo, codice aeroporto) e CTA primaria "Search flights". Il blocco ha due varianti di layout responsive che condividono gli stessi elementi e lo stesso scopo: **horizontal** (desktop) e **vertical** (mobile). La variazione è esclusivamente di layout, non di contenuto né di funzione — si implementa come un unico componente con prop o breakpoint CSS.

### Varianti

| Caratteristica | `horizontal` (desktop) | `vertical` (mobile) |
|---|---|---|
| Orientamento | Immagine a sinistra, testo a destra | Immagine in copertura full-card, testo overlay |
| Sfondo card | Bianco, testo dark su sfondo chiaro | Immagine full-bleed, testo bianco in overlay |
| Descrizione | Testo completo visibile | Troncata con "Read more" |
| Bottone CTA | Nero, fill scuro | Bianco, fill chiaro |
| Ratio immagine | ~1:1 o 4:5, metà larghezza card | Full-width, copre tutta la card (overlay) |

### Struttura elementi (condivisi)
- **Immagine**: foto destinazione con angoli arrotondati
- **Titolo**: nome destinazione, bold, grande
- **Sottotitolo**: categoria (es. "Economy"), peso leggero, muted
- **Descrizione**: testo multi-riga, colore muted; troncata con "Read more" nella variante vertical
- **Metadati inline**: icona tag + prezzo ("from $120") · icona aereo + codice IATA ("BAN")
- **CTA primaria**: bottone pill "Search flights"
- **Bottone secondario**: icona cuore (save/wishlist), separato dalla CTA

### Target devices
- `horizontal`: Desktop e tablet landscape
- `vertical`: Mobile (primario), tablet portrait

### Posizione tipica
Listing page / sezione risultati di ricerca voli o destinazioni — card singola o in griglia/carosello.

### Formato compatto
Card con immagine + titolo + sottotitolo + descrizione + metadati prezzo/IATA + CTA pill + cuore. Layout orizzontale su desktop (immagine sinistra), verticale con overlay su mobile.

### Note di implementazione
Un solo componente con breakpoint CSS o prop `orientation="horizontal|vertical"`. Nessun motivo di duplicare il blocco a livello di collezione.

### Fonte
UI concept — app viaggi/voli (stile Skyscanner/Google Flights mobile)

---

## BLOCK-012 — Masonry inspiration grid (2 colonne)

### Descrizione
Griglia a 2 colonne a larghezza fissa con **altezze variabili** (masonry): ogni immagine mantiene il suo ratio originale senza crop, creando un ritmo visivo irregolare e organico verticalmente. È il pattern standard per gallerie di ispirazione, moodboard e lookbook — lo stesso usato da Pinterest, Houzz e tutti i siti ispirational di interior/arredo. La variabilità delle altezze è la caratteristica definitoria: comunica abbondanza visiva e browsing libero, non catalogazione ordinata.

### Caratteristiche chiave
- **2 colonne simmetriche** — larghezza uguale (50% viewport ciascuna), gap uniforme tra le card
- **Altezze variabili** — ogni immagine rispetta il suo ratio nativo (landscape, portrait, quasi-quadrata), nessun crop forzato
- **Zero testo sulle card** — immagini pure, nessun titolo overlay, nessuna label sotto. Tutto lo spazio è visivo
- **Angoli arrotondati** — border-radius leggero su ogni immagine
- **Scroll infinito** — il layout si estende verticalmente quanto necessario, le due colonne crescono indipendentemente
- **Tap sull'immagine** → apre dettaglio/pagina prodotto/scheda ispirazione

### Navbar (da screenshot Iperceramica)
- Logo centrato con hamburger a sinistra e icone cart + search a destra
- **Tab bar** testuale sotto la navbar: voci con underline colorato brand sull'attiva (es. Prodotti / Ambienti / Offerte) + icona pin + "Negozi" a destra
- La tab bar funge da **filtro contestuale**: cambia il set di immagini mantenendo il layout masonry identico

### Differenza da BLOCK-003 (Two-column results grid)

| | BLOCK-003 | BLOCK-012 |
|---|---|---|
| Altezze card | Fisse/uniformi (crop forzato) | Variabili (ratio nativo) |
| Testo nelle card | Titolo + metadati sotto | ❌ nessuno |
| Scopo | Listing prodotti / confronto | Ispirazione visiva / browsing |
| Scroll | Paginato o lazy load | Scroll infinito |
| Interazione | Tap → PDP prodotto | Tap → dettaglio immagine/scheda |

### Implementazione CSS (moderna, unità relative)

```css
/* Masonry grid — 2 colonne mobile, scalabile */
.masonry-grid {
  columns: 2;
  column-gap: 0.5rem;
  padding: 0.5rem;
}

.masonry-grid img {
  width: 100%;
  break-inside: avoid;
  margin-bottom: 0.5rem;
  border-radius: 0.625rem;
  display: block;
}

/* Tablet: 3 colonne */
@media (min-width: 48rem) {
  .masonry-grid { columns: 3; }
}

/* Desktop: 4 colonne */
@media (min-width: 75rem) {
  .masonry-grid { columns: 4; }
}
```

Nessun pixel fisso — tutto in `rem` scalato sulla dimensione base del font. Approccio nativo CSS senza librerie JavaScript.

### Target devices
Mobile (primario, 2 colonne). Tablet: 3 colonne. Desktop: 4 colonne. Il pattern masonry scala naturalmente aumentando il numero di colonne.

### Posizione tipica
Pagina "Ambienti" / "Ispirazioni" / "Lookbook" — corpo principale della pagina, dopo navbar e tab filter. Occupa quasi l'intera altezza della pagina.

### Formato compatto
Griglia 2 colonne, altezze variabili, zero testo. Gap 0.5rem, border-radius 0.625rem. Scroll infinito. Tab bar filtro sopra. Tap → dettaglio.

### Fonte
iperceramica.it — sezione Ambienti, mobile (browser iOS Safari)

---

## BLOCK-016 — Product detail card con specifiche tecniche (PDP mobile)

### Descrizione
Scheda prodotto verticale a due zone: immagine ambientazione full-width sopra e scheda tecnica su sfondo bianco sotto. L'immagine ambientazione mostra il prodotto in contesto reale; un'immagine campione sovrapposta in basso a destra mostra la texture ravvicinata del materiale. La zona bianca presenta le specifiche in modo editoriale con tipografia compatta e strutturata. È la versione mobile di una PDP (Product Detail Page) o di una scheda catalogo digitale.

### Struttura
**Zona immagine (superiore)**
- Immagine ambientazione full-width, ratio ~16:9 o 3:2 landscape
- **Immagine campione sovrapposta**: foto texture ravvicinata, posizionata bottom-right sull'ambientazione, ratio ~3:4 portrait, sfondo bianco o neutro — mostra la superficie reale del materiale

**Zona scheda tecnica (inferiore, sfondo bianco)**
- **Badge "NEW"**: label uppercase bold, piccola, posizionata sopra il nome prodotto
- **Nome prodotto**: display extra-large, sans-serif bold/black, colore dark — voce dominante della scheda
- **SIZE**: lista orizzontale di misure in cm + conversione in pollici (es. `60x120 · 80x80 · 60x60`), due righe tipografiche sovrapposte (cm sopra, pollici sotto), uppercase compatto
- **FINISHES**: lista di finiture con icona quadrata/strutturata a sinistra + nome finitura bold + nome tecnico inglese muted a destra
- **COLORS**: lista orizzontale di nomi colore uppercase separati da `|` (es. `CREMA | TAUPE | GRIS`)
- Tutte le sezioni usano label uppercase bold come header di sezione (`SIZE`, `FINISHES`, `COLORS`)

### Tipografia
- Nome prodotto: sans-serif black/extrabold, display size, dark
- Badge NEW: uppercase bold, piccolo, dark
- Label sezione: uppercase bold, piccolo, tracking ampio, dark
- Valori: mix bold (nome finitura) + regular muted (nome tecnico inglese)
- Misure: uppercase compatto, due righe sovrapposte cm/pollici

### Ratio immagini
- Ambientazione: ~16:9 o 3:2 landscape, full-width
- Campione sovrapposto: ~3:4 portrait, ~45% larghezza card, angoli retti o leggermente arrotondati

### Target devices
Mobile + tablet (primario). Desktop: zona immagine a sinistra + scheda tecnica a destra in layout split 50/50 o 60/40.

### Posizione tipica
PDP (Product Detail Page) — blocco principale sopra la fold. Oppure scheda catalogo in loop su pagina collezione.

### Formato compatto
Immagine ambientazione landscape + campione texture sovrapposto bottom-right. Sotto: badge NEW + nome prodotto display + SIZE (misure cm/pollici) + FINISHES (icona + nome) + COLORS (lista inline). Sfondo bianco, tipografia compatta uppercase.

### Fonte
Sito ceramiche/piastrelle — scheda prodotto mobile (screenshot iOS)
