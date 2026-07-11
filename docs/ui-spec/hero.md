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

---

## BLOCK-018 — Sliding feature carousel

### Descrizione
Carosello orizzontale con una card principale dominante e due pannelli laterali più stretti che anticipano altri contenuti. Il blocco funziona come hero di scelta tra segmenti, piani o categorie, con forte gerarchia visiva e chiara affordance di navigazione laterale. La card attiva comunica il messaggio principale (titolo, sottotitolo, UI preview o immagine editoriale), mentre le sezioni laterali agiscono da reveal contestuale e invitano alla navigazione.

### Struttura
- **Card principale**: occupa il `60%–68%` della larghezza — immagine o contenuto editoriale dominante, titolo, sottotitolo, eventuale CTA o widget preview
- **Pannelli laterali**: `16%–20%` ciascuno — anteprime parziali delle card adiacenti, sempre visibili per comunicare la presenza di altri contenuti
- **CTA / action chip**: pill circolare o rettangolare in basso al centro o in basso a destra della card attiva — unica azione primaria visibile
- **Gap tra pannelli**: costante e stretto, segnala la separazione senza interrompere il flusso visivo

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale blocco | Full-width, edge-to-edge |
| Card principale | `60%–68%` della larghezza disponibile |
| Pannello laterale visibile | `16%–20%` ciascuno |
| Gap tra pannelli | `0.5rem–0.75rem` |
| Altezza blocco | `24rem–30rem` oppure `min(70vh, 32rem)` |
| Border-radius card | `1rem–1.5rem` |
| Ratio immagine card principale | `3:4` o `4:5` |
| Titolo card | `1.5rem–2rem` |
| Sottotitolo / body card | `0.875rem–1rem` |
| CTA / action chip | `2.25rem–2.75rem` alto, pill |
| Padding interno card | `1rem–1.25rem` |

### Comportamento
- Swipe orizzontale su mobile (touch-native).
- Click/tap sui pannelli laterali per portare la card in focus su desktop.
- Frecce prev/next opzionali su desktop.
- Una sola card deve risultare chiaramente attiva alla volta — le laterali restano visibili ma con scala o opacità ridotta se necessario.

### Differenza da BLOCK-002 (Discovery rail)

| | BLOCK-002 Discovery rail | BLOCK-018 Sliding feature carousel |
|---|---|---|
| Scopo | Navigazione orizzontale di categorie | Hero di scelta tra segmenti macro |
| Dimensione card | Piccola, uniforme | Grande dominante + laterali ridotti |
| Contenuto card | Icona/label | Immagine + titolo + sottotitolo + CTA |
| Posizione | Mid-page | Top / hero |
| Suggestion list sotto | ✅ | ❌ |

### Target devices
Mobile e desktop. Su mobile ottimale se i pannelli laterali restano visibili almeno per `15%–18%`. Su desktop la card principale può espandersi ulteriormente.

### Posizione tipica
Hero di onboarding/scelta piano, landing con segmenti di prodotto (Personal / Business / Freelance), apertura di sezione con macro-categorie.

### Formato compatto
Carousel full-width con card attiva ampia (`~65%`) + due side panels stretti (`~18%` ciascuno) che anticipano le alternative. Swipe o click per cambiare focus. Forte gerarchia visiva, zero ambiguità su cosa è attivo.

### Fonte
App fintech / finanza personale — hero onboarding scelta piano, desktop (screenshot)

---

## BLOCK-020 — Split hero: testo su sfondo bianco + immagine full-width sotto

### Descrizione
Hero desktop a due bande orizzontali impilate che insieme formano il viewport iniziale. La banda superiore è bianca con navbar integrata e contenuto testuale; la banda inferiore è un’immagine fotografica full-width edge-to-edge senza overlay. Il taglio netto tra sfondo bianco e immagine crea un effetto di reveal potente — la foto emerge come un paesaggio da sotto il testo. Tono corporate/istituzionale, alta respirabilità tipografica.

### Struttura
- **Banda superiore** (~`45%–50%` del viewport): sfondo bianco
  - Navbar con logo sinistra, voci di menu centrate, CTA pill destra
  - Label descrittiva breve flush-left (es. "Who we are?") + corpo piccolo sotto
  - Headline display grande a destra o centro-destra — sans-serif bold, molto grande
  - Elemento decorativo grafico centrato in muted (es. simbolo brand, watermark leggero)
- **Banda inferiore** (~`50%–55%` del viewport): immagine fotografica
  - Full-width, edge-to-edge, nessun padding laterale
  - Nessun overlay, nessun testo sovrapposto
  - Logo o elemento brand sovrapposto in basso a sinistra (opzionale)
  - Nessuna CTA — il blocco è puramente narrativo/identitario

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Altezza totale blocco | `100vh` o `min(100vh, 56rem)` |
| Banda superiore | `45%–50%` dell’altezza totale |
| Banda inferiore | `50%–55%` dell’altezza totale |
| Separazione tra bande | Taglio netto, `0` gap, nessun divisore visibile |
| Padding laterale banda superiore | `1.5rem–3rem` (allineato al contenitore) |
| Headline display | `3rem–5rem` · font-weight 700–900 |
| Label descrittiva sinistra | `0.75rem–0.875rem` · regular · max 2 righe |
| Elemento decorativo | `30%–40%` della larghezza · opacità `5%–15%` · centrato |
| Immagine inferiore | Full-width · `object-fit: cover` · nessun border-radius |
| Logo brand sovrapposto | Bottom-left · `2rem–3rem` di altezza |

### Differenza da BLOCK-015 (Hero collezione)

| | BLOCK-015 Hero collezione | BLOCK-020 Split hero |
|---|---|---|
| Testo | Overlay su immagine | Sfondo bianco separato |
| Immagine | Fullscreen sotto tutto | Banda inferiore autonoma |
| Navbar | Su immagine o trasparente | Su sfondo bianco |
| Tono | Campaign / moody | Corporate / istituzionale |
| CTA | ✅ pill outline | ❌ (solo navbar) |

### Target devices
Desktop (primario). Su tablet: le proporzioni si mantengono con font leggermente ridotto. Su mobile: le due bande si impilano, la foto diventa un blocco a sé con ratio `16:9` o `4:3`.

### Posizione tipica
Homepage corporate, sito istituzionale, landing brand — primo blocco dopo la navbar, occupa il 100% del viewport iniziale.

### Formato compatto
Viewport diviso in due bande orizzontali ~50/50: superiore bianca con navbar + headline display + label descrittiva + watermark decorativo; inferiore foto full-width edge-to-edge senza overlay. Taglio netto tra le due zone.

### Fonte
Sito corporate / agritech / istituzionale — desktop (screenshot)
