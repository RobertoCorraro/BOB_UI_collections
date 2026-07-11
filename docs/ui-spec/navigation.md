# Navigation patterns

Pattern di navigazione globale: footer, menu principale, drawer.

---

## BLOCK-006 — Accordion footer nav

### Descrizione
Navigazione da footer mobile strutturata come lista di sezioni a fisarmonica (accordion). Ogni sezione ha un titolo in maiuscolo con icona chevron a destra che indica lo stato aperto/chiuso.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Larghezza | Full-width, edge-to-edge |
| Padding laterale interno | **16–20px** |
| Altezza header row (sezione chiusa) | **48–56px** (touch target generoso) |
| Titolo sezione | Font-size **0.875rem** · uppercase · font-weight **700** · colore bianco |
| Icona chevron | **16–20px** · colore bianco/grigio chiaro · allineata destra |
| Divisore tra sezioni | Linea **1px** grigio scuro (~#333–#444) · full-width |
| Altezza riga link (pannello espanso) | **44px** (touch target minimo) |
| Font link interni | Font-size **0.875rem** · regular · colore grigio muted (~#999) |
| Indent link interni | **0** aggiuntivo — stessa x del titolo sezione |
| Padding pannello espanso | **0** superiore · **8px** inferiore (prima del divisore) |
| Gap tra link nel pannello | **0** — altezza riga fissa 44px gestisce la spaziatura |
| Item attivo | Font-weight **600–700** · colore bianco pieno |
| Sfondo footer | Dark ~**#1a1a1a** |

### Stati accordion
| Stato | Chevron | Pannello |
|---|---|---|
| Chiuso (default) | ∨ (freccia giù) | nascosto |
| Aperto | ∧ (freccia su) | visibile, espanso |

### Comportamento
- Animazione: slide-down **200ms ease-out**
- Più sezioni aperte contemporaneamente: ✅ supportato
- Touch target: intera header row tappabile

### Tipografia
- Titolo sezione: uppercase bold 0.875rem bianco
- Link interni: regular 0.875rem grigio muted
- Item attivo: semibold/bold bianco

### Target devices
**Mobile (esclusivo)**. Su tablet/desktop: footer a colonne affiancate.

### Posizione tipica
Footer — fondo pagina, dopo i contenuti e prima del copyright.

### Formato compatto
Full-width, padding 16–20px. Header row 48–56px: titolo uppercase bold bianco + chevron destra. Divisore 1px grigio scuro. Pannello espanso: righe 44px, link regular muted. Sfondo #1a1a1a. Animazione 200ms.

### Fonte
deghi.it — footer homepage mobile (browser iOS)

---

## BLOCK-010 — Sliding panel navigation (drill-down)

### Descrizione
Pattern di navigazione mobile a pannelli sovrapposti: ogni tap su una voce di livello superiore sostituisce lateralmente l'intero viewport con un nuovo pannello contenente le sotto-voci.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Larghezza pannello | **100% viewport** (full-screen, non drawer parziale) |
| Sfondo pannello | Bianco o grigio molto chiaro |
| Altezza riga voce L1/L2 | **48–56px** (touch target generoso) |
| Padding riga | **16–20px** laterale |
| Font voci L1 | Font-size **0.875–1rem** · bold · colore dark |
| Font voci L2 | Font-size **0.875–1rem** · bold · colore dark |
| Font voci L3 (accordion espanso) | Font-size **0.875rem** · regular · colore muted · indent +**16px** |
| Chevron `>` (drill-down) | **16–20px** · colore muted · allineato destra |
| `+` / `−` (accordion L3) | **20–24px** · colore dark · allineato destra |
| Divisore tra voci | Linea **1px** grigio chiaro · full-width |
| Header pannello L2 | Altezza **44–56px** · freccia `←` back 24px sinistra · titolo bold centrato |
| Animazione L1 → L2 | Slide orizzontale · **300ms ease-in-out** |
| Animazione accordion L3 | Slide-down verticale · **200ms ease-out** |
| Navbar superiore fissa | Altezza **44–56px** · sempre visibile in tutti i pannelli · contiene logo, search, account, cart, × |
| Footer fisso | Altezza **44–48px** · link secondari · sfondo grigio chiaro separato |

### Struttura a 3 livelli

| Livello | Contenuto | Animazione |
|---|---|---|
| **L1 — Root** | Categorie bold + chevron `>` o link diretto | Nessuna |
| **L2 — Sub** | ← back + titolo centrato + lista voci | Slide-in da destra 300ms |
| **L3 — Accordion** | Voci espandibili con `+`/`−` inline | Expand verticale 200ms |

### Target devices
**Mobile (esclusivo)**. Desktop: mega-menu orizzontale a colonne.

### Posizione tipica
Menu principale — si attiva da hamburger. Copre 100% viewport come overlay.

### Formato compatto
100% viewport. Navbar fissa 50px top. Righe 48–56px, padding 16–20px, divisori 1px. L1: bold + chevron/link. L2: ← back + titolo centrato + voci. L3: accordion +/− indent 16px. Animazione slide 300ms. Footer fisso 44px.

### Fonte
knoll.com — menu mobile (browser iOS Safari)
