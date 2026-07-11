# UI Block Specifications

## Asymmetric media collage

### Descrizione
Layout a due colonne 50/50; una colonna contiene un blocco verticale dominante, l'altra due blocchi quadrati impilati. Il blocco è pensato per aprire una sezione con forte gerarchia visiva e preview compatta.

### Ratio immagini
Card principale 3:4 o 4:5; card secondarie 1:1.

### Target devices
Mobile + tablet. Desktop solo se inserito in un contenitore più ampio o come modulo editoriale.

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
