# Loop prodotti

Griglie, caroselli e card per listing e visualizzazione di prodotti, risultati e destinazioni.

---

## BLOCK-003 — Two-column results grid

### Descrizione
Griglia simmetrica a 2 colonne con card uniformi, media sopra e testo sotto. Adatta a listing di risultati: facilita scansione, confronto e ripetizione visiva.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Colonne | 2 colonne simmetriche da `1fr 1fr` |
| Gap tra colonne | `0.5rem–0.75rem` |
| Gap tra righe | `0.5rem–0.75rem` |
| Padding laterale griglia | `0.75rem–1rem` |
| Ratio immagine | `1:1` o `4:5` |
| Border-radius immagine | `0.5rem–0.75rem` |
| Larghezza card | Circa `(100% - padding - gap) / 2` |
| Testo sotto immagine | Padding `0.5rem` laterale · `0.25rem–0.375rem` verticale |
| Titolo card | `0.8125rem–0.875rem` · bold/semibold · max 2 righe |
| Metadati / prezzo | `0.75rem` |
| Gap titolo → metadati | `0.125rem–0.25rem` |
| Altezza zona testo | `2.5rem–3.5rem` |
| Altezza card totale | `13rem–17.5rem` a seconda del ratio immagine |
| Background card | Bianco · bordo o ombra lieve · border-radius `0.5rem–0.75rem` |

### Target devices
Mobile + tablet + desktop.

### Posizione tipica
Pagina risultati / listing page — corpo centrale, dopo filtri o header di sezione.

### Formato compatto
Griglia 2 colonne, gap `0.5rem–0.75rem`, padding laterale `0.75rem–1rem`. Card con immagine `1:1` o `4:5`, border-radius `0.5rem–0.75rem`, testo compatto sotto in `2.5rem–3.5rem` di altezza.

### Fonte
Google — sito mobile (google.com su browser mobile)

---

## BLOCK-007 — Destination detail card

### Descrizione
Card informativa per una destinazione di viaggio con immagine, dati essenziali e CTA primaria. Due varianti responsive: horizontal (desktop) e vertical (mobile).

### Varianti

| Caratteristica | `horizontal` (desktop) | `vertical` (mobile) |
|---|---|---|
| Orientamento | Immagine a sinistra, testo a destra | Immagine full-card, testo overlay |
| Sfondo card | Bianco, testo dark | Immagine full-bleed, testo bianco |
| Descrizione | Completa | Troncata |
| Bottone CTA | Fill scuro | Fill chiaro |
| Ratio immagine | `1:1` o `4:5` | Full-width overlay |

### Struttura elementi (condivisi)
- Immagine con angoli arrotondati
- Titolo bold grande
- Sottotitolo muted
- Descrizione multi-riga
- Metadati inline
- CTA pill
- Icona cuore

### Target devices
- `horizontal`: Desktop e tablet landscape
- `vertical`: Mobile (primario), tablet portrait

### Posizione tipica
Listing page / sezione risultati di ricerca voli o destinazioni.

### Formato compatto
Card con immagine, titolo, sottotitolo, descrizione, metadati e CTA pill. Layout orizzontale su desktop, verticale overlay su mobile.

### Note di implementazione
Un solo componente con breakpoint CSS o prop `orientation="horizontal|vertical"`.

### Fonte
UI concept — app viaggi/voli (stile Skyscanner/Google Flights mobile)

---

## BLOCK-012 — Masonry inspiration grid (2 colonne)

### Descrizione
Griglia a 2 colonne con altezze variabili (masonry): ogni immagine mantiene il proprio ratio nativo senza crop, creando un ritmo visivo organico.

### Caratteristiche chiave
- 2 colonne simmetriche
- Altezze variabili
- Zero testo sulle card
- Angoli arrotondati
- Scroll infinito
- Tap → dettaglio

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
Griglia 2 col, altezze variabili, zero testo. Gap `0.5rem`, border-radius `0.625rem`.

### Fonte
iperceramica.it — sezione Ambienti, mobile (browser iOS Safari)

---

## BLOCK-016 — Brand mini bar

### Descrizione
Blocco orizzontale compatto a due zone impilate verticalmente: zona visiva sopra (immagine landscape + immagine campione quadrata sovrapposta) e zona dati sotto (sfondo bianco, testo strutturato). Altezza contenuta, orientamento orizzontale dominante.

### Geometrie precise

#### Zona visiva (superiore)
| Elemento | Geometria relativa |
|---|---|
| Immagine ambientazione | Full-width · ratio `16:9` o `3:2` · altezza ~`55%–60%` del blocco |
| Immagine campione sovrapposta | `1:1` quadrata · larghezza ~`40%–45%` della zona visiva · bottom-right · overflow verso il basso `30%–40%` della propria altezza |
| Border-radius campione | `0–0.25rem` |

#### Zona dati (inferiore)
| Elemento | Geometria relativa |
|---|---|
| Altezza zona dati | ~`40%–45%` del blocco |
| Padding interno | `1rem` laterale · `0.75rem` verticale |
| Badge | `0.625rem` · uppercase bold |
| Titolo | `2rem–2.5rem` · sans-serif black/extrabold |
| Sezioni dati | label `0.6rem` + valori `0.75rem` · gap `0.5rem` |
| Valori doppi | 2 righe · interlinea `1.1` |
| Lista colori | inline |

#### Proporzioni complessive
| | Misura relativa |
|---|---|
| Altezza totale mobile | `26rem–31.25rem` |
| Larghezza | Full-width, edge-to-edge |
| Variante desktop | Zona visiva `55%–60%` · zona dati `40%–45%` affiancate |

### Target devices
Mobile + tablet + desktop.

### Posizione tipica
Ovunque serva comunicare identità + dati in poco spazio: scheda prodotto, banner brand, listing catalogo.

### Formato compatto
Striscia full-width alta `26rem–31.25rem`. Immagine landscape sopra, campione `1:1` sovrapposto bottom-right con overflow del `30%–40%`. Zona bianca sotto con badge, titolo display e sezioni dati compatte.

### Fonte
Sito ceramiche/piastrelle — scheda prodotto mobile (screenshot iOS)
