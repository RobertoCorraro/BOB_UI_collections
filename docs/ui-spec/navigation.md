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
