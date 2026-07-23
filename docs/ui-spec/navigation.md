# Navigation patterns

Pattern di navigazione globale: footer, menu principale, drawer.

---

## BLOCK-006 — Accordion footer nav

### Descrizione
Navigazione da footer mobile strutturata come lista di sezioni a fisarmonica (accordion). Ogni sezione ha un titolo in maiuscolo con icona chevron a destra che indica lo stato aperto/chiuso.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza | Full-width, edge-to-edge |
| Padding laterale interno | `1rem–1.25rem` |
| Altezza header row | `3rem–3.5rem` |
| Titolo sezione | `0.875rem` · uppercase · bold |
| Icona chevron | `1rem–1.25rem` |
| Divisore tra sezioni | `1px` full-width |
| Altezza riga link | `2.75rem` |
| Font link interni | `0.875rem` · regular |
| Indent link interni | `0` |
| Padding pannello espanso | `0 0 0.5rem 0` |
| Item attivo | font-weight `600–700` |
| Sfondo footer | dark |

### Stati accordion
| Stato | Chevron | Pannello |
|---|---|---|
| Chiuso | ∨ | nascosto |
| Aperto | ∧ | visibile |

### Comportamento
- Animazione: slide-down `200ms ease-out`
- Più sezioni aperte contemporaneamente: ✅
- Touch target: intera header row tappabile

### Tipografia
- Titolo sezione: uppercase bold `0.875rem`
- Link interni: regular `0.875rem`
- Item attivo: semibold/bold

### Target devices
Mobile esclusivo. Su tablet/desktop: footer a colonne affiancate.

### Posizione tipica
Footer — fondo pagina, dopo i contenuti e prima del copyright.

### Formato compatto
Full-width, padding `1rem–1.25rem`. Header row alta `3rem–3.5rem`, titolo uppercase bold + chevron a destra. Divisori 1px. Pannello espanso con righe link alte `2.75rem`.

### Fonte
deghi.it — footer homepage mobile (browser iOS)

---

## BLOCK-010 — Sliding panel navigation (drill-down)

### Descrizione
Pattern di navigazione mobile a pannelli sovrapposti: ogni tap su una voce di livello superiore sostituisce lateralmente l'intero viewport con un nuovo pannello contenente le sotto-voci.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza pannello | `100vw` |
| Sfondo pannello | Bianco o grigio molto chiaro |
| Altezza riga voce L1/L2 | `3rem–3.5rem` |
| Padding riga | `1rem–1.25rem` laterale |
| Font voci L1 | `0.875rem–1rem` · bold |
| Font voci L2 | `0.875rem–1rem` · bold |
| Font voci L3 | `0.875rem` · regular · indent `1rem` |
| Chevron `>` | `1rem–1.25rem` |
| `+` / `−` | `1.25rem–1.5rem` |
| Divisore tra voci | `1px` full-width |
| Header pannello L2 | Altezza `2.75rem–3.5rem` · freccia back `1.5rem` · titolo centrato |
| Animazione L1 → L2 | Slide orizzontale `300ms ease-in-out` |
| Animazione accordion L3 | Slide-down `200ms ease-out` |
| Navbar superiore fissa | Altezza `2.75rem–3.5rem` |
| Footer fisso | Altezza `2.75rem–3rem` |

### Struttura a 3 livelli

| Livello | Contenuto | Animazione |
|---|---|---|
| L1 — Root | Categorie bold + chevron o link diretto | Nessuna |
| L2 — Sub | Back + titolo + lista voci | Slide-in da destra |
| L3 — Accordion | Voci espandibili inline | Expand verticale |

### Target devices
Mobile esclusivo. Desktop: mega-menu orizzontale a colonne.

### Posizione tipica
Menu principale — si attiva da hamburger. Copre il viewport come overlay.

### Formato compatto
Overlay `100vw`. Navbar fissa alta `2.75rem–3.5rem`. Righe navigazione alte `3rem–3.5rem`, padding laterale `1rem–1.25rem`, divisori 1px. L3 con indent `1rem`. Footer fisso `2.75rem–3rem`.

### Fonte
knoll.com — menu mobile (browser iOS Safari)

---

## BLOCK-024 — Sticky top navbar: logo + ricerca + hamburger animato

### Descrizione
Barra di navigazione sticky in cima al viewport, sempre visibile durante lo scroll. Tre zone allineate in riga: logo a sinistra, campo di ricerca a pillola al centro (occupa lo spazio residuo), icona hamburger a destra che si anima trasformandosi in una X al click, per aprire il menu principale.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Altezza barra | `3.5rem–4rem` |
| Padding laterale | `1rem–1.25rem` |
| Gap tra le tre zone | `0.75rem–1rem` |
| Logo font-size | `1.125rem–1.25rem` · bold |
| Barra ricerca — altezza | `2.5rem` |
| Barra ricerca — border-radius | `9999px` (pill) |
| Barra ricerca — larghezza | flex-grow su mobile, max `28rem` da tablet in su |
| Font placeholder ricerca | `0.8125rem` |
| Icona lente | `1rem` |
| Hamburger — touch target | `2.75rem × 2.75rem` (Apple HIG) |
| Hamburger — larghezza linee | `1.375rem` |
| Hamburger — spessore linee | `0.125rem` |
| Hamburger — gap tra linee | `0.3125rem` |
| Sfondo barra | Bianco, ombra leggera |
| Z-index | Sopra il contenuto scrollabile |

### Stati hamburger
| Stato | Aspetto | Animazione |
|---|---|---|
| Chiuso | 3 linee orizzontali parallele | — |
| Aperto | X (linea 1 e 3 ruotate 45°/−45°, linea 2 dissolta) | `250ms ease` |

### Comportamento
- `position: sticky; top: 0`, sempre visibile indipendentemente dallo scroll
- Click/tap sull'hamburger: toggla stato aperto/chiuso, animazione CSS pura (transform + opacity), zero JS per la grafica dell'icona — solo un toggle di classe/attributo
- Touch target minimo rispettato anche se le linee visive sono più piccole
- Barra di ricerca: focus state con bordo/ombra accentuata

### Target devices
Mobile-first: barra compatta sempre visibile da `375px`. Tablet (`≥48rem`) e desktop (`≥75rem`): stessa struttura a 3 zone, ricerca centrale con larghezza massima e contenuto centrato nel container.

### Posizione tipica
Header — prima riga della pagina, sticky in cima, sopra hero/contenuto.

### Formato compatto
Barra sticky alta `3.5rem–4rem`, padding laterale `1rem–1.25rem`. Logo bold a sinistra, search pill (`h 2.5rem`) al centro flex-grow, hamburger animato (linee → X, `250ms ease`) a destra in touch target `2.75rem`.

### Differenza da BLOCK-020
BLOCK-020 (Split hero navbar) vive dentro l'hero con menu orizzontale nascosto su mobile e nessuna ricerca. BLOCK-024 è una navbar standalone sempre sticky, con ricerca integrata al centro e hamburger animato, pensata per restare visibile indipendentemente da un hero.

### Fonte
Pattern sintetizzato da richiesta diretta dell'utente (navbar mobile-first generica in stile app/e-commerce) — nessuno screenshot o sito specifico da citare come fonte.
