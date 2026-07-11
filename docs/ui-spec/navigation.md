# Navigation patterns

Pattern di navigazione globale: footer, menu principale, drawer.

---

## BLOCK-006 — Accordion footer nav

### Descrizione
Navigazione da footer mobile strutturata come lista di sezioni a fisarmonica (accordion). Ogni sezione ha un titolo in maiuscolo con icona chevron (^ o v) a destra che indica lo stato aperto/chiuso. Tappando il titolo, il pannello si espande mostrando i link interni; tappando di nuovo si chiude. Un divisore orizzontale separa ogni sezione. Lo sfondo è scuro (dark mode), i titoli sono bianchi e in grassetto, i link sono grigi/muted per creare gerarchia visiva immediata. Il pattern sostituisce su mobile la classica colonna di link del footer desktop, comprimendo lo spazio verticale e rendendo la navigazione esplorabile su richiesta.

### Nome tecnico del pattern
**Accordion** (detto anche: collapsible footer nav, expandable footer sections, footer accordion). In HTML/CSS si implementa tipicamente con `<details>` + `<summary>` oppure con JavaScript toggle su classi CSS.

### Struttura sezione
- **Header row**: titolo sezione in MAIUSCOLO, bold, allineato a sinistra + icona chevron (∨ chiuso / ∧ aperto) allineata a destra — row full-width tappabile
- **Divisore**: linea orizzontale sottile (1 px) tra ogni sezione
- **Pannello espanso**: lista verticale di link testuali, stile muted/grigio, spacing generoso tra le voci (min 44 px touch target per voce)
- **Evidenziazione item attivo**: peso del font aumentato (semibold o bold) per indicare la pagina/sezione corrente

### Stati
| Stato | Chevron | Pannello |
|---|---|---|
| Chiuso (default) | ∨ (freccia giù) | nascosto |
| Aperto | ∧ (freccia su) | visibile, espanso |

### Comportamento
- **Uno o più pannelli aperti contemporaneamente**: entrambi i comportamenti sono validi; Deghi mostra più sezioni aperte in simultanea
- **Animazione**: slide-down consigliata (max 200ms ease-out) per non rallentare la navigazione
- **Touch target**: l'intera header row è tappabile, non solo il testo o l'icona

### Tipografia
- Titolo sezione: uppercase, font-weight 700, colore bianco o quasi-bianco
- Link interni: sentence case, font-weight 400, colore grigio muted (es. #999 o simile)
- Item attivo: font-weight 600–700, colore bianco pieno

### Colori (da screenshot Deghi)
- Sfondo: dark (#1a1a1a o simile)
- Titolo sezione: bianco
- Link: grigio chiaro/muted
- Divisori: grigio scuro sottile

### Ratio immagini
Nessuna immagine. Blocco puramente testuale e navigazionale.

### Target devices
**Mobile (esclusivo)**. Su tablet e desktop il footer torna alla versione a colonne affiancate — l'accordion non serve su schermi larghi dove lo spazio verticale non è un vincolo.

### Posizione tipica
Footer — fondo pagina, dopo i contenuti principali e prima del copyright/note legali.

### Formato compatto
Lista verticale di sezioni: titolo uppercase + chevron / divisore / pannello espandibile con link muted. Dark background, zero immagini, puro testo navigazionale.

### Fonte
deghi.it — footer homepage mobile (browser iOS)

---

## BLOCK-010 — Sliding panel navigation (drill-down)

### Descrizione
Pattern di navigazione mobile a pannelli sovrapposti: ogni tap su una voce di livello superiore sostituisce lateralmente l'intero viewport con un nuovo pannello contenente le sotto-voci. Il livello terziario usa invece un accordion inline (expand in-place verticale) senza aprire un nuovo pannello. È il pattern standard per navigazioni gerarchiche profonde su mobile, usato da iOS Settings, Amazon, IKEA e molti e-commerce premium.

### Nome tecnico del pattern
**Sliding panel navigation** — detto anche:
- **Drill-down navigation** (nome semantico: si "scende" nella gerarchia)
- **Multi-level slide-in menu** (nome descrittivo dell'animazione)
- **Cascading panel nav** (variante con pannelli sovrapposti visibili parzialmente)

Distinzione chiave dall'**accordion**: nell'accordion il contenuto si espande nello stesso pannello verso il basso; qui ogni livello sostituisce lateralmente l'intero viewport con un pannello nuovo.

### Struttura a 3 livelli

| Livello | Contenuto | Animazione |
|---|---|---|
| **L1 — Root** | Categorie principali con chevron → (es. Living, Dining, Home Office…) + voci senza chevron per link diretti (es. New Arrivals) | Pannello iniziale, nessuna animazione |
| **L2 — Sub-categoria** | Nuovo pannello: ← back + titolo centrato + lista voci L2 | Slide-in da destra (~300ms ease-in-out), L1 esce a sinistra |
| **L3 — Accordion inline** | Voci L2 con `+`/`−`: tap espande sotto-voci inline, `+` diventa `−` | Expand verticale in-place, nessun cambio pannello |

### Dettagli strutturali

**Header pannello L2**
- Freccia `←` back a sinistra — torna al pannello L1
- Titolo centrato = nome categoria selezionata (es. "Living")
- Navbar superiore (logo, search, account, cart, ×) sempre fissa e visibile in tutti i pannelli

**Indicatori di navigabilità sulle voci**
- Chevron `>` a destra = drill-down disponibile (apre pannello L2)
- `+` a destra = accordion inline disponibile (espande L3 in-place)
- Nessuna icona = link diretto, nessun sotto-livello

**Footer fisso**
- Riga di link secondari (es. Favorites, Support, Trade, Locations) — identica in tutti i pannelli
- Sfondo leggermente grigio, visivamente separato dal contenuto principale

### Comportamento animazione
- **L1 → L2**: pannello L2 entra da destra, L1 scorre fuori a sinistra (slide orizzontale, ~300ms ease-in-out)
- **L2 → L1 (back)**: inversione — L1 rientra da sinistra, L2 esce a destra
- **Accordion L3**: slide-down verticale in-place (max 200ms ease-out), nessun cambio di pannello

### Tipografia (da screenshot Knoll)
- Voci L1 con drill-down: font-weight bold, colore dark
- Voci L1 senza drill-down (link diretti): font-weight bold, nessun chevron
- Voci L2 con accordion: font-weight bold + icona `+`/`−`
- Voci L3 (accordion espanso): font-weight regular, indent leggero, colore muted/dark

### Ratio immagini
Nessuna immagine. Blocco puramente testuale e navigazionale.

### Target devices
**Mobile (esclusivo)** nella forma sliding panel. Su desktop la stessa gerarchia si implementa con mega-menu orizzontale a colonne — il pattern non si adatta a schermi larghi, va sostituito.

### Posizione tipica
Menu di navigazione principale — si attiva da hamburger icon o da tap sulla × nella navbar. Copre l'intero viewport come overlay o drawer laterale.

### Formato compatto
Drawer full-height. L1: lista voci bold con divisori e chevron `>` o link diretto. Tap → slide-in pannello L2 (← back + titolo centrato + voci). Voci con `+` espandono L3 in-place (accordion). Footer fisso con link secondari in tutti i pannelli.

### Fonte
knoll.com — menu mobile (browser iOS Safari)
