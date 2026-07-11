# Banner e promo

Banner promozionali, editorial stack e carousel di servizi. Pattern conversion-oriented.

---

## BLOCK-005 — Editorial stacked banner stack

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

## BLOCK-011 — Service card carousel (icon + title + description + CTA)

### Descrizione
Carosello orizzontale di card servizi o sezioni informative, **senza immagini fotografiche**. Ogni card è un rettangolo bianco su sfondo grigio neutro, con icona pictogram in cima, titolo display bold, descrizione breve e CTA circolare ghost. Il blocco è orientato all'esplorazione dei servizi di supporto o delle macro-sezioni del sito. L'assenza di foto lo rende leggero, scalabile e adatto a contesti istituzionali, utility o "come funziona".

### Struttura card
- **Icona pictogram**: outline icon (~40 px), posizionata in alto nella card — rappresenta il servizio specifico (es. persona con cappello = consulente, carrello = acquisto online). Icona diversa per ogni card
- **Titolo display**: testo bold molto grande, domina visivamente la card (es. "Acquistare in IKEA")
- **Descrizione**: 2–3 righe di testo regular colore dark/muted, spiega brevemente il servizio o la sezione
- **CTA circolare ghost**: bottone outline circolare con freccia `→` inside, posizionato in basso a sinistra della card (~56–64 px diametro, bordo sottile dark, sfondo trasparente)
- **Nessuna immagine fotografica** — sfondo card bianco puro, angoli arrotondati, elevation leggera (ombra sottile o bordo grigio)

### Navigazione
- **Frecce prev/next esterne**: bottoni circolari filled dark (sfondo nero pieno, icona `<` `>` bianca), sovrapposti parzialmente ai bordi laterali del carousel — accessibili anche senza swipe
- **Progress bar lineare**: linea sottile full-width sotto il carousel; segmento attivo in dark (nero o blu scuro), resto grigio chiaro — indica la posizione corrente senza dots o numeri
- **Touch swipe**: gesture orizzontale sull'area card
- **Overflow visivo**: card precedente e successiva parzialmente visibili ai bordi (~1 card dominante + 2 bordi parziali)

### Footer del blocco
- **Link "Visualizza tutti i servizi"**: riga tappabile full-width — testo bold a sinistra, chevron `>` a destra — separa il carousel dal contenuto sottostante e offre accesso all'archivio completo

### Card visibili all'avvio
**1 card dominante** (~80% viewport) con bordi delle card adiacenti visibili ai lati

### Ratio card
~**3:4** o quasi quadrata — card alta e larga, contenuto ben distanziato internamente con padding generoso

### Target devices
Mobile (primario). Su desktop: 2–3 card visibili contemporaneamente, frecce esterne diventano il metodo principale di navigazione.

### Posizione tipica
Sezione "Servizi e supporto" / "Come funziona" — mid-page o pagina dedicata ai servizi, dopo l'hero o come blocco standalone in homepage.

### Formato compatto
Sfondo grigio neutro. Card bianche con angoli arrotondati: icona pictogram top + titolo display bold + descrizione 2–3 righe + CTA ghost circolare bottom-left. Navigazione: frecce filled dark esterne + progress bar lineare sotto. Footer: link "Visualizza tutti" con chevron.

### Fonte
ikea.com — sezione "Servizi e supporto", mobile (browser iOS Safari)
