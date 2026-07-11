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

## BLOCK-016 — Brand mini bar

### Descrizione
Blocco orizzontale compatto a due zone affiancate verticalmente: zona visiva sopra (immagine landscape a tutto bordo + immagine campione quadrata sovrapposta) e zona dati sotto (sfondo bianco, testo strutturato in colonne). L'altezza totale è volutamente contenuta — il blocco è una "striscia" che comunica identità, materiale e specifiche senza occupare più di una frazione dello schermo. Riutilizzabile in qualsiasi contesto: sito brand, catalogo, SERP locale, landing di prodotto, scheda in loop.

### Geometrie precise

#### Zona visiva (superiore)
| Elemento | Geometria |
|---|---|
| Immagine ambientazione | Full-width × altezza fissa ~55–60% del blocco totale · ratio **16:9** o **3:2** landscape · nessun bordo |
| Immagine campione sovrapposta | Quadrata **1:1** · larghezza ~40–45% della zona visiva · posizionata **bottom-right** con offset negativo verso il basso che sfora nella zona dati · sfondo bianco o neutro · nessun border-radius o border-radius minimo (2–4px) |
| Overlap campione su zona dati | Il campione scende di ~30–40% della propria altezza nella zona bianca sotto — crea continuità visiva tra le due zone |

#### Zona dati (inferiore, sfondo bianco)
| Elemento | Geometria |
|---|---|
| Altezza zona dati | ~40–45% del blocco totale |
| Padding interno | `1rem` laterale · `0.75rem` verticale |
| Badge (es. "NEW") | Uppercase bold · font-size ~0.625rem · lettera-spacing ampio · posizione top-left della zona |
| Nome / titolo | Sans-serif black o extrabold · font-size **display** (~2–2.5rem su mobile) · occupa ~30–35% della larghezza della zona testo (sinistra), il campione sovrapposto occupa la destra |
| Sezioni dati (SIZE, FINISHES, COLORS…) | Label uppercase bold ~0.6rem + valori regular ~0.75rem · disposte in **colonna verticale** · gap tra sezioni ~0.5rem |
| Valori con due livelli (es. cm + pollici) | Due righe sovrapposte: riga superiore bold dark · riga inferiore regular muted · interlinea stretta (~1.1) |
| Lista colori inline | Nomi uppercase separati da `·` o `|` · regular muted · stessa riga |

### Proporzioni complessive
- **Altezza totale su mobile**: ~420–500px (dipende dal contenuto della zona dati)
- **Larghezza**: full-width, edge-to-edge, nessun padding laterale esterno
- **Ratio visivo percepito**: orizzontale dominante — la zona visiva è più larga che alta, la zona dati è compatta

### Variante desktop
Su desktop le due zone si affiancano orizzontalmente invece di impilare:
- **Zona visiva**: colonna sinistra ~55–60% larghezza, altezza fissa
- **Zona dati**: colonna destra ~40–45% larghezza, allineata verticalmente al centro
- Il campione sovrapposto mantiene la stessa logica ma sfora verso destra nella zona dati

### Contenuto intercambiabile
Il blocco non è legato a nessun settore. La zona dati può contenere qualsiasi combinazione di:
- Specifiche tecniche (misure, finiture, materiali)
- Attributi di prodotto (taglia, colore, peso)
- Dati brand (anno, collezione, origine)
- Microcopy editoriale (claim, tagline, categoria)

### Target devices
Mobile + tablet + desktop. Geometrie identiche su tutti i device, solo la direzione di impilamento cambia (verticale su mobile, orizzontale su desktop).

### Posizione tipica
Ovunque sia necessario comunicare identità + dati in poco spazio verticale: scheda prodotto, banner brand, risultato SERP arricchito, listing catalogo, sezione "chi siamo" compatta.

### Formato compatto
Striscia orizzontale full-width. Zona visiva: immagine landscape 16:9 + campione 1:1 sovrapposto bottom-right con overflow nella zona dati. Zona dati sfondo bianco: badge + titolo display + sezioni dati uppercase compatte. Altezza totale ~420–500px mobile.

### Fonte
Sito ceramiche/piastrelle — scheda prodotto mobile (screenshot iOS)
