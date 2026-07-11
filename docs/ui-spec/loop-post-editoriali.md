# Loop post ed editoriali

Caroselli e layout per post, articoli, profili utente e contenuti editoriali.

---

## BLOCK-001 — Asymmetric media collage

### Descrizione
Layout a due colonne 50/50; una colonna contiene un blocco verticale dominante, l'altra due blocchi quadrati impilati. Il blocco è pensato per aprire una sezione con forte gerarchia visiva e preview compatta.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Larghezza totale | Full-width, edge-to-edge, 0 padding laterale esterno |
| Colonne | 2 colonne simmetriche, **50% / 50%** larghezza viewport ciascuna |
| Gap tra colonne | **4–6px** (gap visivo minimo, quasi assente) |
| Gap tra card nella colonna destra | **4–6px** (stesso gap del gap tra colonne) |
| Card sinistra (verticale dominante) | Altezza = **100% dell'altezza del blocco** · ratio **3:4** o **4:5** portrait |
| Card destra superiore (quadrata) | Altezza = **50% dell'altezza del blocco** − metà gap · ratio **1:1** |
| Card destra inferiore (quadrata) | Altezza = **50% dell'altezza del blocco** − metà gap · ratio **1:1** |
| Altezza totale blocco su mobile | ~**340–400px** su iPhone standard (375px wide) |
| Border-radius | **0** — nessun arrotondamento, immagini a bordo vivo |
| Testo | Nessun testo sovrapposto sulle card — immagini pure |
| Padding interno blocco | **0** laterale · **0** verticale — blocco completamente edge-to-edge |

### Schema visivo (ASCII)
```
┌──────────┬──────────┐
│          │  [1:1]   │
│  [3:4]   ├──────────┤
│          │  [1:1]   │
└──────────┴──────────┘
  50%         50%
```

### Ratio immagini
Card principale: **3:4** o **4:5** portrait. Card secondarie: **1:1** quadrate.

### Target devices
Mobile + tablet. Desktop solo se inserito in un contenitore più ampio o come modulo editoriale.

### Posizione tipica
Top of feed / apertura sezione contenuti — prima schermata dopo hero o navbar.

### Formato compatto
2 colonne 50/50, gap 4–6px, edge-to-edge. Colonna sinistra: 1 card portrait 3:4, altezza intera. Colonna destra: 2 card quadrate 1:1 impilate. Nessun testo, nessun border-radius.

### Fonte
App Facebook — mobile (iOS/Android)

---

## BLOCK-004 — People suggestion carousel

### Descrizione
Carosello orizzontale di card persone con overflow intenzionale: la card successiva è visibile a metà per comunicare la presenza di altri elementi e invitare allo scroll. Ogni card contiene un avatar circolare grande, titolo (nome utente), sottotitolo con avatar piccolo e testo contestuale (es. amici in comune), e un bottone CTA primario full-width in fondo alla card.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Larghezza card | ~**160–180px** (circa 45–48% viewport mobile 375px) |
| Altezza card | ~**220–260px** |
| Card visibili | **1 card intera + metà della successiva** (overflow ~50% card destra) |
| Gap tra card | **8–12px** |
| Padding interno card | **12–16px** laterale · **16px** verticale |
| Avatar principale | Circolare **1:1** · diametro ~**72–80px** · centrato in cima alla card · margin-top ~16px |
| Avatar secondario (sottotitolo) | Circolare **1:1** · diametro **24–28px** · inline a sinistra del testo contestuale |
| Titolo nome | Font-weight bold · font-size ~**0.875rem** · centrato · 1 riga, troncato |
| Sottotitolo | Avatar piccolo inline + testo ~**0.75rem** regular muted · centrato |
| Gap titolo → sottotitolo | **4–6px** |
| Bottone CTA | Full-width (100% larghezza card − padding) · altezza **36–40px** · border-radius **20px** (pill) · colore primario filled |
| Gap sottotitolo → bottone | **auto** (bottone pinned al fondo con margin-top: auto o flexbox) |
| Close button × | **20–24px** · posizione top-right · padding **8px** |
| Background card | Bianco o grigio molto chiaro · border-radius card **12–16px** |
| Sfondo sezione | Grigio chiaro o bianco |

### Target devices
Mobile. Tablet e desktop non consigliati nella versione carosello; valutare layout a griglia su schermi larghi.

### Posizione tipica
Feed / home page — inserito inline nel flusso dei contenuti, tipicamente dopo i primi post o come blocco dedicato nella sezione esplora.

### Formato compatto
Carosello orizzontale, gap 8–12px. Card ~160×240px, border-radius 12–16px: avatar circolare 72–80px centrato in cima + nome bold centrato + avatar 24px + testo contestuale + CTA pill full-width bottom pinned. Overflow 50% card successiva. Close × top-right.

### Fonte
App Instagram — mobile (iOS/Android), sezione "Suggeriti per te"

---

## BLOCK-013 — Article teaser carousel

### Descrizione
Carosello orizzontale di anteprime editoriali con immagine hero in alto e blocco testuale ampio sotto, separato visivamente dall'immagine. La card mostra un articolo, progetto o case study; la card successiva è visibile parzialmente sul lato destro.

### Geometrie precise

| Elemento | Misura |
|---|---|
| Larghezza card | ~**85–90% viewport** — card dominante con overflow destro visibile |
| Overflow card successiva | ~**10–15% viewport** visibile a destra |
| Gap tra card | **12–16px** |
| Padding laterale esterno blocco | **16px** da sinistra (la card non è edge-to-edge) |
| Immagine hero | Ratio **16:9** o **3:2** landscape · full-width della card · border-radius top **12px** |
| Altezza immagine su mobile | ~**180–220px** |
| Zona testo (sotto immagine) | Sfondo bianco · padding **12–16px** · border-radius bottom **12px** |
| Titolo editoriale | Font-weight bold/extrabold · font-size **1.25–1.5rem** · max 3 righe · colore dark |
| Metadati uppercase | Font-size **0.625–0.75rem** · uppercase · lettera-spacing ampio · colore muted · sopra o sotto il titolo |
| Gap metadati → titolo | **6–8px** |
| Altezza zona testo | ~**100–140px** dipende dalle righe del titolo |
| Altezza card totale | ~**300–360px** su mobile |
| Background card | Bianco · border-radius **12px** · ombra leggera o bordo grigio sottile |

### Card visibili all'avvio
**1 card dominante + preview della successiva** sul lato destro (~10–15% visibile)

### Target devices
Mobile (primario). Desktop: 2-up carousel o lista editoriale verticale con immagine a sinistra.

### Posizione tipica
Homepage editoriale, sezione magazine, portfolio progetti — dopo hero o come blocco "storie in evidenza".

### Formato compatto
Card ~88% viewport, padding-left 16px, gap 12–16px. Immagine 16:9 border-radius top 12px, altezza ~200px. Zona testo bianca padding 12–16px: metadati uppercase 0.75rem + titolo bold 1.375rem max 3 righe. Altezza totale ~330px.

### Fonte
Sito editoriale/architettura — mobile (screenshot iOS)
