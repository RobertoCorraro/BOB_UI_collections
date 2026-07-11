# UI Block Specifications

## Asymmetric media collage

### Descrizione
Layout a due colonne 50/50; una colonna contiene un blocco verticale dominante, l'altra due blocchi quadrati impilati. Il blocco è pensato per aprire una sezione con forte gerarchia visiva e preview compatta.

### Ratio immagini
Card principale 3:4 o 4:5; card secondarie 1:1.

### Target devices
Mobile + tablet. Desktop solo se inserito in un contenitore più ampio o come modulo editoriale.

### Posizione tipica
Top of feed / apertura sezione contenuti — prima schermata dopo hero o navbar.

### Formato compatto
2 colonne uguali: una con 1 card verticale, l'altra con 2 card quadrate sovrapposte. Spacing ridotto, composizione compatta, lettura immediata da mobile.

### Fonte
App Facebook — mobile (iOS/Android)

---

## Horizontal discovery rail + suggestion list

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

## Two-column results grid

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

## People suggestion carousel

### Descrizione
Carosello orizzontale di card persone con overflow intenzionale: la card successiva è visibile a metà per comunicare la presenza di altri elementi e invitare allo scroll. Ogni card contiene un avatar circolare grande, titolo (nome utente), sottotitolo con avatar piccolo e testo contestuale (es. amici in comune), e un bottone CTA primario full-width in fondo alla card. Il blocco è progettato per stimolare connessioni sociali o suggerire profili rilevanti.

### Struttura card
- **Avatar**: immagine circolare, grande, centrata nella parte superiore della card
- **Titolo**: nome utente, testo bold, centrato
- **Sottotitolo**: avatar secondario piccolo (circolare) + testo contestuale breve (es. "1 in comune"), allineati in riga, centrati
- **Bottone CTA**: full-width, colore primario, testo breve e diretto (es. "Segui"), posizionato in fondo alla card
- **Close button**: icona × in alto a destra per ignorare il suggerimento

### Ratio immagini
Avatar principale 1:1 con clip circolare; avatar secondario nel sottotitolo 1:1 piccolo (24–32 px).

### Target devices
Mobile. Tablet e desktop non consigliati nella versione carosello; valutare layout a griglia su schermi larghi.

### Posizione tipica
Feed / home page — inserito inline nel flusso dei contenuti, tipicamente dopo i primi post o come blocco dedicato nella sezione esplora.

### Formato compatto
Carosello orizzontale con 1 card visibile + metà della successiva. Card con avatar circolare grande, nome, sottotitolo contestuale e bottone CTA full-width.

### Fonte
App Instagram — mobile (iOS/Android), sezione "Suggeriti per te"

---

## Editorial stacked banner stack

### Descrizione
Serie di banner editoriali full-width impilati verticalmente, senza gap o con gap minimo. Ogni banner è un'immagine di prodotto o ambientazione con testo sovrapposto in basso a sinistra: titolo bold (parola chiave in colore brand) e sottotitolo con eventuale link inline colorato. Il blocco è conversion-oriented: ogni banner promuove una categoria, collezione o novità specifica. A differenza dei blocchi discovery, qui il testo è parte integrante del visual e non appare sotto l'immagine.

### Struttura banner
- **Immagine di sfondo**: foto prodotto o ambientazione, full-width, edge-to-edge
- **Titolo overlay**: testo bold, colore bianco + keyword in colore brand (es. arancio), posizionato in basso a sinistra sull'immagine
- **Sottotitolo overlay**: testo più piccolo, con parole chiave colorate o link inline
- **Nessun bottone esplicito**: l'intera area del banner è tappabile (card-as-CTA)

### Ratio immagini
Ogni banner ~**5:3** o **16:9 leggermente compresso**. Altezza stimata 220–280 px su iPhone standard. Full-width senza padding laterale.

### Target devices
Mobile (primario). Desktop richiede adattamento: limitare la larghezza massima o aumentare il ratio per evitare immagini eccessivamente basse.

### Posizione tipica
Homepage / landing page — corpo centrale dopo l'hero, usato come sezione promozionale editoriale.

### Formato compatto
Stack verticale di banner full-width edge-to-edge. Testo overlay bottom-left con titolo bianco + keyword brand-color. Nessun bottone, intera area tappabile.

### Differenza dai blocchi discovery
| Caratteristica | Blocchi discovery (BLOCK-001/002/003/004) | Editorial banner stack |
|---|---|---|
| Testo sull'immagine | ❌ | ✅ overlay bottom-left |
| Scroll direction | orizzontale o griglia | verticale impilato |
| Scopo | navigazione/esplorazione | promozione/conversione |
| Bottone esplicito | ✅ (alcuni) | ❌ (banner intero = CTA) |
| Metadati commerciali | ❌ | keyword prodotto + link |

### Fonte
deghi.it — homepage mobile (browser iOS, Safari/Chrome)

---

## Accordion footer nav

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

## Destination detail card

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

## Filtered category carousel con frecce prev/next

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

## Category showcase numerato

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

---

## Sliding panel navigation (drill-down)

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
