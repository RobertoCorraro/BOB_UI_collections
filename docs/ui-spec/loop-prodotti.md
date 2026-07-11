# Loop prodotti

Griglie, caroselli e card per listing e visualizzazione di prodotti, risultati e destinazioni.

---

## BLOCK-003 — Two-column results grid

### Descrizione
Griglia simmetrica a 2 colonne con card uniformi, media sopra e testo sotto. Adatta a listing di risultati: facilita scansione, confronto e ripetizione visiva.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Colonne | **2 colonne simmetriche** · 50% viewport ciascuna |
| Gap tra colonne | **8–12px** |
| Gap tra righe | **8–12px** |
| Padding laterale griglia | **12–16px** (la griglia non è edge-to-edge) |
| Ratio immagine | **1:1** o **4:5** |
| Border-radius immagine | **8–12px** |
| Altezza immagine su mobile (1:1) | ~**160–180px** su viewport 375px (metà larghezza − padding − gap) |
| Testo sotto immagine | Padding interno **8px** laterale · **4–6px** verticale |
| Titolo card | Font-size **0.8125–0.875rem** · bold o semibold · max 2 righe · troncato con ellipsis |
| Metadati / prezzo | Font-size **0.75rem** · regular o bold · colore dark o brand |
| Gap titolo → metadati | **2–4px** |
| Altezza zona testo | **40–56px** fisso o auto in base al contenuto |
| Altezza card totale | ~**210–250px** (1:1) o ~**240–280px** (4:5) |
| Background card | Bianco · nessuna ombra o ombra leggerissima · border-radius card **8–12px** |

### Schema visivo
```
┌──────────┐ ┌──────────┐
│  [img]   │ │  [img]   │
│  1:1/4:5 │ │  1:1/4:5 │
├──────────┤ ├──────────┤
│ Titolo   │ │ Titolo   │
│ Prezzo   │ │ Prezzo   │
└──────────┘ └──────────┘
  ~50%           ~50%
  (- padding e gap)
```

### Target devices
Mobile + tablet + desktop.

### Posizione tipica
Pagina risultati / listing page — corpo centrale, dopo filtri o header di sezione.

### Formato compatto
Griglia 2 col, gap 10px, padding 14px laterale. Card: immagine 1:1 border-radius 10px + titolo 0.875rem bold 2 righe + prezzo 0.75rem. Altezza card ~230px.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-007 — Destination detail card

### Descrizione
Card informativa per una destinazione di viaggio con immagine, dati essenziali (prezzo, codice aeroporto) e CTA primaria "Search flights". Due varianti responsive: **horizontal** (desktop) e **vertical** (mobile).

### Varianti

| Caratteristica | `horizontal` (desktop) | `vertical` (mobile) |
|---|---|---|
| Orientamento | Immagine a sinistra, testo a destra | Immagine in copertura full-card, testo overlay |
| Sfondo card | Bianco, testo dark | Immagine full-bleed, testo bianco overlay |
| Descrizione | Testo completo visibile | Troncata con "Read more" |
| Bottone CTA | Nero fill | Bianco fill |
| Ratio immagine | ~1:1 o 4:5, metà larghezza card | Full-width overlay |

### Struttura elementi (condivisi)
- **Immagine**: foto destinazione con angoli arrotondati
- **Titolo**: nome destinazione, bold, grande
- **Sottotitolo**: categoria (es. "Economy"), peso leggero, muted
- **Descrizione**: testo multi-riga, colore muted; troncata con "Read more" su mobile
- **Metadati inline**: icona tag + prezzo ("from $120") · icona aereo + codice IATA
- **CTA primaria**: bottone pill "Search flights"
- **Bottone secondario**: icona cuore (save/wishlist)

### Target devices
- `horizontal`: Desktop e tablet landscape
- `vertical`: Mobile (primario), tablet portrait

### Posizione tipica
Listing page / sezione risultati di ricerca voli o destinazioni.

### Formato compatto
Card: immagine + titolo + sottotitolo + descrizione + metadati prezzo/IATA + CTA pill + cuore. Layout orizzontale su desktop, verticale con overlay su mobile.

### Note di implementazione
Un solo componente con breakpoint CSS o prop `orientation="horizontal|vertical"`.

### Fonte
UI concept — app viaggi/voli (stile Skyscanner/Google Flights mobile)

---

## BLOCK-012 — Masonry inspiration grid (2 colonne)

### Descrizione
Griglia a 2 colonne a larghezza fissa con **altezze variabili** (masonry): ogni immagine mantiene il suo ratio originale senza crop, creando un ritmo visivo irregolare e organico.

### Caratteristiche chiave
- **2 colonne simmetriche** — larghezza uguale (50% viewport ciascuna), gap uniforme tra le card
- **Altezze variabili** — ogni immagine rispetta il suo ratio nativo, nessun crop forzato
- **Zero testo sulle card** — immagini pure
- **Angoli arrotondati** — border-radius leggero
- **Scroll infinito**
- **Tap** → apre dettaglio/pagina prodotto

### Implementazione CSS (moderna, unità relative)

```css
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

@media (min-width: 48rem) {
  .masonry-grid { columns: 3; }
}

@media (min-width: 75rem) {
  .masonry-grid { columns: 4; }
}
```

### Target devices
Mobile (2 col) · Tablet (3 col) · Desktop (4 col).

### Posizione tipica
Pagina Ambienti / Ispirazioni / Lookbook — corpo principale dopo navbar e tab filter.

### Formato compatto
Griglia 2 col, altezze variabili, zero testo. Gap 0.5rem, border-radius 0.625rem. Scroll infinito. Tab bar filtro sopra.

### Fonte
iperceramica.it — sezione Ambienti, mobile (browser iOS Safari)

---

## BLOCK-016 — Brand mini bar

### Descrizione
Blocco orizzontale compatto a due zone impilate verticalmente: zona visiva sopra (immagine landscape + immagine campione quadrata sovrapposta) e zona dati sotto (sfondo bianco, testo strutturato). Altezza contenuta, orientamento orizzontale dominante. Riutilizzabile in qualsiasi contesto: brand, catalogo, landing, SERP arricchita.

### Geometrie precise

#### Zona visiva (superiore)
| Elemento | Geometria |
|---|---|
| Immagine ambientazione | Full-width · ratio **16:9** o **3:2** landscape · altezza ~**55–60% del blocco totale** |
| Immagine campione sovrapposta | **1:1** quadrata · larghezza ~**40–45%** della zona visiva · posizionata **bottom-right** · offset negativo verso il basso: sfora ~**30–40%** della propria altezza nella zona dati |
| Border-radius campione | **0–4px** (quasi nessuno) |

#### Zona dati (inferiore, sfondo bianco)
| Elemento | Geometria |
|---|---|
| Altezza zona dati | ~**40–45% del blocco totale** |
| Padding interno | **1rem** laterale · **0.75rem** verticale |
| Badge (es. "NEW") | Uppercase bold · font-size ~**0.625rem** · lettera-spacing ampio · top-left |
| Nome / titolo | Sans-serif black/extrabold · font-size ~**2–2.5rem** · occupa la sinistra (~55%) |
| Sezioni dati | Label uppercase bold ~**0.6rem** + valori regular **0.75rem** · colonna verticale · gap **0.5rem** |
| Valori doppi (cm + pollici) | 2 righe sovrapposte · riga sup bold dark · riga inf regular muted · interlinea **1.1** |
| Lista colori inline | Nomi uppercase separati da `·` o `\|` · regular muted |

#### Proporzioni complessive
| | Misura |
|---|---|
| Altezza totale mobile | ~**420–500px** |
| Larghezza | Full-width, edge-to-edge |
| Variante desktop | Zona visiva a sinistra ~60% · zona dati a destra ~40% · layout orizzontale |

### Target devices
Mobile + tablet + desktop.

### Posizione tipica
Ovunque sia necessario comunicare identità + dati in poco spazio: scheda prodotto, banner brand, listing catalogo.

### Formato compatto
Striscia full-width ~450px mobile. Immagine landscape 16:9 + campione 1:1 bottom-right overlap 35% in zona dati. Zona bianca: badge 0.625rem + titolo display 2rem + sezioni dati uppercase 0.625rem. Altezza totale ~450px.

### Fonte
Sito ceramiche/piastrelle — scheda prodotto mobile (screenshot iOS)
