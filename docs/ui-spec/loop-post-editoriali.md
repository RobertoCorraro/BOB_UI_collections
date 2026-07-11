# Loop post ed editoriali

Caroselli e layout per post, articoli, profili utente e contenuti editoriali.

---

## BLOCK-001 — Asymmetric media collage

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

## BLOCK-004 — People suggestion carousel

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

## BLOCK-013 — Article teaser carousel

### Descrizione
Carosello orizzontale di anteprime editoriali con immagine hero in alto e blocco testuale ampio sotto, separato visivamente dall'immagine. La card mostra un articolo, progetto o case study; la card successiva è visibile parzialmente sul lato destro per comunicare chiaramente la presenza di altri contenuti e invitare allo swipe. Non è un hero singolo né un banner stack: è un pattern di browsing editoriale.

### Struttura card
- **Immagine hero**: visual ampio, ratio landscape, full-width nella parte superiore della card
- **Overflow laterale**: la card successiva compare parzialmente a destra; il contenuto non è centrato in una singola card isolata ma in un carousel con preview del prossimo item
- **Titolo editoriale**: headline grande, bold, multilinea, posizionata sotto l'immagine su fondo bianco
- **Metadati uppercase**: luogo, paese, testata, data o categoria, separati dal titolo e con tracking/weight più istituzionale
- **Nessun bottone esplicito**: l'intera card è tappabile

### Distinzione da altri pattern

| Pattern | Differenza chiave |
|---|---|
| Hero header | Il hero è singolo, senza overflow né swipe laterale |
| Banner stack | Il banner stack impila elementi verticalmente; qui la navigazione è orizzontale |
| Editorial banner overlay | Nell'overlay il testo sta sopra l'immagine; qui il testo è sotto, separato |
| Results card | La results card è più compatta e ripetitiva; qui la card è ampia, narrativa, magazine-like |

### Card visibili all'avvio
**1 card dominante + preview della successiva** sul lato destro

### Ratio immagini
~**16:9** o **3:2** landscape. L'immagine deve avere abbastanza respiro da funzionare come apertura narrativa dell'articolo.

### Navigazione
- **Touch swipe** orizzontale su mobile
- **Overflow intenzionale** della card successiva come affordance primaria
- Su desktop: preferibile carousel con **2 card visibili** + frecce prev/next, oppure lista editoriale verticale con immagine a sinistra e testo a destra

### Target devices
Mobile (primario). Desktop non come griglia 3-up: meglio 2-up o layout editoriale list per preservare il peso del titolo e la qualità narrativa.

### Posizione tipica
Homepage editoriale, sezione magazine, portfolio progetti, archivio case study — subito dopo hero o come blocco "storie in evidenza".

### Formato compatto
Card editoriale ampia: immagine landscape sopra, titolo grande sotto, metadati uppercase. Carousel orizzontale con 1 card dominante + prossima parziale a destra. Nessun CTA esplicito, card intera tappabile.

### Fonte
Sito editoriale/architettura — mobile (screenshot iOS)
