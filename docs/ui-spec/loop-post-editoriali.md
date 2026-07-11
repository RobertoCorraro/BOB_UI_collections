# Loop post ed editoriali

Caroselli e layout per post, articoli, profili utente e contenuti editoriali.

---

## BLOCK-001 — Asymmetric media collage

### Descrizione
Layout a due colonne 50/50; una colonna contiene un blocco verticale dominante, l'altra due blocchi quadrati impilati. Il blocco è pensato per aprire una sezione con forte gerarchia visiva e preview compatta.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale | Full-width, edge-to-edge, `0` padding laterale esterno |
| Colonne | 2 colonne simmetriche, `50% / 50%` della larghezza disponibile |
| Gap tra colonne | `0.25rem–0.375rem` |
| Gap tra card nella colonna destra | `0.25rem–0.375rem` |
| Card sinistra dominante | Altezza = `100%` del blocco · ratio `3:4` o `4:5` |
| Card destra superiore | Altezza = `50%` del blocco meno metà gap · ratio `1:1` |
| Card destra inferiore | Altezza = `50%` del blocco meno metà gap · ratio `1:1` |
| Altezza totale blocco | `min(52vh, 25rem)` circa |
| Border-radius | `0` |
| Testo | Nessun testo sovrapposto |
| Padding interno blocco | `0` |

### Ratio immagini
Card principale: `3:4` o `4:5` portrait. Card secondarie: `1:1`.

### Target devices
Mobile + tablet. Desktop solo se inserito in un contenitore più ampio o come modulo editoriale.

### Posizione tipica
Top of feed / apertura sezione contenuti — prima schermata dopo hero o navbar.

### Formato compatto
2 colonne `50/50`, gap `0.25rem–0.375rem`, edge-to-edge. Colonna sinistra: 1 card portrait dominante. Colonna destra: 2 card quadrate impilate. Nessun testo, nessun border-radius.

### Fonte
App Facebook — mobile (iOS/Android)

---

## BLOCK-004 — People suggestion carousel

### Descrizione
Carosello orizzontale di card persone con overflow intenzionale: la card successiva è visibile a metà per comunicare la presenza di altri elementi e invitare allo scroll. Ogni card contiene un avatar circolare grande, titolo, sottotitolo con avatar piccolo e testo contestuale, e un bottone CTA primario full-width in fondo alla card.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza card | `44vw–48vw`, con `max-width: 11.25rem` |
| Altezza card | `14rem–16rem` |
| Card visibili | `1` card intera + circa `0.5` della successiva |
| Gap tra card | `0.5rem–0.75rem` |
| Padding interno card | `0.75rem–1rem` laterale · `1rem` verticale |
| Avatar principale | `1:1` circolare · diametro `4.5rem–5rem` · centrato in alto |
| Avatar secondario | `1:1` circolare · diametro `1.5rem–1.75rem` |
| Titolo nome | `0.875rem` circa · bold · 1 riga |
| Sottotitolo | `0.75rem` regular muted |
| Gap titolo → sottotitolo | `0.25rem–0.375rem` |
| Bottone CTA | `100%` della larghezza utile · altezza `2.25rem–2.5rem` · border-radius `9999px` |
| Close button × | box tappabile `1.25rem–1.5rem`, con padding esterno `0.5rem` |
| Background card | Bianco o grigio chiarissimo · border-radius `0.75rem–1rem` |

### Target devices
Mobile. Tablet e desktop non consigliati nella versione carosello; valutare layout a griglia su schermi larghi.

### Posizione tipica
Feed / home page — inserito inline nel flusso dei contenuti, tipicamente dopo i primi post o come blocco dedicato nella sezione esplora.

### Formato compatto
Carosello orizzontale, gap `0.5rem–0.75rem`. Card larghe `44vw–48vw`, alte `14rem–16rem`, border-radius `0.75rem–1rem`: avatar grande centrato in cima, nome, sottotitolo, CTA pill full-width in basso. Overflow della card successiva ~50%.

### Fonte
App Instagram — mobile (iOS/Android), sezione "Suggeriti per te"

---

## BLOCK-013 — Article teaser carousel

### Descrizione
Carosello orizzontale di anteprime editoriali con immagine hero in alto e blocco testuale ampio sotto, separato visivamente dall'immagine. La card mostra un articolo, progetto o case study; la card successiva è visibile parzialmente sul lato destro.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza card | `85%–90%` del viewport |
| Overflow card successiva | `10%–15%` del viewport visibile a destra |
| Gap tra card | `0.75rem–1rem` |
| Padding laterale esterno blocco | `1rem` |
| Immagine hero | Ratio `16:9` o `3:2` · full-width della card · border-radius top `0.75rem` |
| Altezza immagine | `11rem–13.75rem` circa |
| Zona testo | Sfondo bianco · padding `0.75rem–1rem` · border-radius bottom `0.75rem` |
| Titolo editoriale | `1.25rem–1.5rem` · bold/extrabold · max 3 righe |
| Metadati uppercase | `0.625rem–0.75rem` · tracking ampio |
| Gap metadati → titolo | `0.375rem–0.5rem` |
| Altezza zona testo | `6.25rem–8.75rem` |
| Altezza card totale | `18.75rem–22.5rem` |
| Background card | Bianco · border-radius `0.75rem` · bordo o ombra lieve |

### Card visibili all'avvio
1 card dominante + preview della successiva sul lato destro.

### Target devices
Mobile (primario). Desktop: 2-up carousel o lista editoriale verticale con immagine a sinistra.

### Posizione tipica
Homepage editoriale, sezione magazine, portfolio progetti — dopo hero o come blocco "storie in evidenza".

### Formato compatto
Card larga `85%–90vw`, gap `0.75rem–1rem`. Immagine `16:9` alta `11rem–13.75rem`, border-radius top `0.75rem`. Zona testo bianca con padding `0.75rem–1rem`: metadati uppercase + titolo grande fino a 3 righe.

### Fonte
Sito editoriale/architettura — mobile (screenshot iOS)

---

## BLOCK-019 — Asymmetric editorial project grid

### Descrizione
Griglia desktop a tre colonne con pesi visivi diversi, pensata per mostrare un portfolio di progetti recenti o case study. La colonna sinistra ha una card grande verticale; la colonna centrale impila due card di altezze diverse; la colonna destra è stretta con una sola card verticale e CTA esplicita. Il pattern bilancia scoperta visiva e conversione: ogni progetto ha un titolo leggibile, e la colonna centrale include un badge azione freccia diagonale ↗ per stimolare il click.

### Struttura card
- **Colonna sinistra** (~`38%`): card grande verticale, immagine dominante, titolo + sottotitolo sotto — nessun overlay, leggibilità diretta
- **Colonna centrale** (~`38%`): due card impilate verticalmente
  - Card superiore: immagine + titolo overlay in basso + badge freccia diagonale ↗ in alto a destra
  - Card inferiore: immagine + label testuale sotto — più compatta
- **Colonna destra** (~`20%–24%`): card stretta verticale, immagine, titolo + metadato sotto, CTA pill "See more" in basso
- **Heading sezione**: titolo testuale "Latest Projects" o equivalente, posizionato sopra la griglia, flush-left

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale blocco | Full-width con padding contenitore `1.5rem–3rem` |
| Colonna sinistra | `~38%` della larghezza disponibile |
| Colonna centrale | `~38%` della larghezza disponibile |
| Colonna destra | `~20%–24%` della larghezza disponibile |
| Gap tra colonne | `0.75rem–1rem` |
| Altezza card sinistra | `100%` del blocco · ratio `3:4` o `4:5` |
| Altezza card centrale superiore | `55%–60%` del blocco · ratio `4:3` o `16:9` |
| Altezza card centrale inferiore | `38%–42%` del blocco · ratio `16:9` |
| Altezza card destra | `100%` del blocco · ratio `2:3` |
| Gap tra card impilate (colonna centrale) | `0.5rem–0.75rem` |
| Altezza totale blocco | `22rem–30rem` su desktop |
| Border-radius card | `0.75rem–1rem` |
| Badge freccia ↗ | `2rem–2.25rem` · cerchio · top-right della card |
| Titolo card | `0.875rem–1.125rem` · bold · max 2 righe |
| Metadato / categoria | `0.75rem` · muted · 1 riga |
| CTA pill | `auto` larghezza · altezza `2rem–2.25rem` · border-radius `9999px` · bordo sottile |
| Padding testo sotto card | `0.5rem–0.75rem` verticale |

### Differenza da BLOCK-001 (Asymmetric media collage)

| | BLOCK-001 | BLOCK-019 |
|---|---|---|
| Colonne | 2 simmetriche `50/50` | 3 con pesi diversi `38/38/24` |
| Testo | Nessuno | Titolo, metadato, CTA |
| Badge azione ↗ | ❌ | ✅ colonna centrale |
| CTA esplicita | ❌ | ✅ colonna destra |
| Scopo | Media discovery | Portfolio showcase con conversione |
| Target device | Mobile | Desktop (primario) |

### Comportamento hover (desktop)
- Card con badge ↗: scala leggera `scale(1.02)` o overlay scuro al passaggio del mouse
- CTA "See more": cambio stato su hover (es. fill del bottone)
- Titoli: restano sempre leggibili, nessun effetto di nascondimento

### Target devices
Desktop (primario). Su tablet: semplificare a 2 colonne con la colonna destra che cade sotto. Su mobile: stack verticale di card singole.

### Posizione tipica
Sezione "Latest Projects", "Case studies", "Portfolio" — tipicamente nella seconda metà di una homepage agency, studio creativo o freelance designer.

### Formato compatto
Griglia desktop 3 colonne asimmetriche `38/38/24`, gap `0.75rem–1rem`. Sinistra: card grande portrait con titolo sotto. Centro: 2 card impilate, superiore con badge ↗. Destra: card stretta con CTA pill "See more".

### Fonte
Sito agency / studio design — desktop (screenshot)
