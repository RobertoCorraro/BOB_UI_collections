# Hero

Blocchi hero fullscreen a tutta viewport: apertura di pagina, storytelling di collezione, introduzione di categoria. Posizione sempre al top della pagina, sopra ogni altro contenuto.

---

## BLOCK-014 — Hero categoria con overlay, breadcrumb e immagine secondaria sovrapposta

### Descrizione
Hero fullscreen per pagine di categoria. L'immagine di sfondo occupa l'intero viewport; il titolo editoriale in serif è sovrapposto in alto a sinistra. Un breadcrumb centrato con divisore verticale `|` sopra separa il titolo dall'immagine secondaria sovrapposta in basso, che anticipa visivamente i contenuti della categoria. Widget flottanti (accesso riservato, chat) sono posizionati agli angoli inferiori. Il pattern comunica lusso, editorialità e contesto di navigazione simultaneamente.

### Struttura
- **Immagine di sfondo**: foto ambientazione fullscreen, nessun crop, copre il 100% del viewport
- **Titolo display serif**: headline grande, bianco, sovrapposto in alto a sinistra — serif comunica luxury/editoriale
- **Divisore verticale** `|`: linea sottile centrata orizzontalmente, separa visivamente titolo e breadcrumb
- **Breadcrumb**: testo uppercase muted centrato (`HOME > NOME CATEGORIA`), posizionato a metà altezza del viewport
- **Immagine secondaria sovrapposta**: foto di dettaglio o ambientazione correlata, posizionata in basso al centro/destra, parzialmente fuori dal visual principale — crea profondità e layer visivo
- **Link gallery**: testo uppercase con freccia diagonale `↘ GALLERY` bottom-left
- **Widget flottante login**: icona chiave in box bianco, bottom-left sopra il link gallery — accesso area riservata
- **Chat bubble**: bottone circolare bottom-right

### Tipografia
- Titolo: serif display, font-weight 700–900, bianco, molto grande (display size)
- Breadcrumb: sans-serif uppercase, font-weight 400, bianco/muted, lettera-spacing ampio
- Link gallery: sans-serif uppercase, piccolo, bianco

### Ratio immagini
- Immagine principale: fullscreen, ratio libero adattato al viewport (tipicamente 9:16 su mobile)
- Immagine secondaria: ~3:4 portrait, sovrapposta con offset rispetto ai bordi del viewport

### Target devices
Mobile (primario). Su desktop: immagine principale + immagine secondaria affiancate, oppure split layout con testo a sinistra e immagine a destra.

### Posizione tipica
Top della pagina categoria (es. `/bagni-in-marmo`, `/cucine`, `/outdoor`) — primo blocco dopo la navbar, occupa il 100% del viewport iniziale.

### Formato compatto
Fullscreen ambientazione + titolo serif overlay top-left + divisore verticale + breadcrumb centrato + immagine secondaria sovrapposta bottom-center + link gallery bottom-left + widget flottanti angoli.

### Fonte
Sito piastrelle/marmo — pagina categoria, mobile (screenshot iOS)

---

## BLOCK-015 — Hero collezione con CTA pill

### Descrizione
Hero fullscreen per landing di collezione o campagna. Immagine di ambientazione molto scura e atmosferica occupa l'intero viewport; il testo è sovrapposto nella metà inferiore con brand name, nome collezione, sottotitolo descrittivo e un bottone CTA pill outline bianco. Nessun elemento di navigazione: il blocco è puramente narrativo e conversion-oriented. L'unico gesto possibile è premere la CTA o scorrere verso il basso.

### Struttura
- **Immagine di sfondo**: foto ambientazione fullscreen, dominante scuro/moody, copre il 100% del viewport
- **Brand name**: testo regular/light bianco, dimensione media — identifica la serie o il brand (es. "Kronos")
- **Nome collezione**: headline grande, sans-serif regular o medium, bianco — seconda riga visivamente più pesante del brand name
- **Sottotitolo**: testo descrittivo 1–2 righe, regular, bianco, dimensione più piccola — claim narrativo della collezione
- **Bottone CTA pill outline**: bordo bianco, sfondo trasparente, testo uppercase letterspacing, dimensione generosa — unica azione disponibile nella fold
- **Scroll indicator**: elemento semicircolare parzialmente visibile bottom-right — segnala la presenza di contenuto sotto

### Differenza da BLOCK-014

| | BLOCK-014 Hero categoria | BLOCK-015 Hero collezione |
|---|---|---|
| Scopo | Navigazione + orientamento | Storytelling + conversione |
| Breadcrumb | ✅ presente | ❌ assente |
| CTA esplicita | ❌ (link gallery testuale) | ✅ bottone pill |
| Immagine secondaria | ✅ sovrapposta | ❌ solo sfondo |
| Widget flottanti | ✅ login + chat | ❌ solo scroll indicator |
| Tono | Editoriale luxury | Campaign/brand storytelling |

### Tipografia
- Brand name: sans-serif light/regular, bianco, medium size
- Nome collezione: sans-serif regular/medium, bianco, display size
- Sottotitolo: sans-serif regular, bianco, body size
- CTA: sans-serif uppercase, lettera-spacing ampio, small/medium size

### Ratio immagini
Fullscreen, ratio libero adattato al viewport (tipicamente 9:16 su mobile). Immagine deve funzionare con testo bianco sovrapposto — necessario gradiente scuro nella metà inferiore o immagine già dark.

### Overlay consigliato
Gradiente lineare `from transparent to rgba(0,0,0,0.5–0.7)` nella metà inferiore per garantire leggibilità del testo su qualsiasi immagine.

### Target devices
Mobile (primario). Desktop: immagine fullwidth con testo centrato o posizionato a sinistra, CTA più grande.

### Posizione tipica
Landing di collezione, pagina campagna, homepage stagionale — primo blocco sopra tutto, occupa il 100% del viewport.

### Formato compatto
Fullscreen dark ambientazione + brand name + nome collezione display + sottotitolo + CTA pill outline bianco + scroll indicator bottom-right.

### Fonte
Sito ceramiche/piastrelle — landing collezione, mobile (screenshot iOS)
