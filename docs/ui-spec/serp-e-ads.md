# SERP e Ads

Layout di risultati di ricerca, Local Pack Google, schede attività e formati pubblicitari. Blocchi di riferimento per ottimizzazione SEO locale, Google Ads e struttura delle informazioni aziendali.

---

## BLOCK-017 — Local Business SERP card (Google Maps Local Pack)

### Descrizione
Layout nativo di Google Maps / Local Pack su mobile in dark mode. Mostra i risultati di ricerca locale per attività commerciali con rating, distanza, orari, snippet di annuncio e bottoni CTA inline. È il primo touchpoint visivo del brand nella SERP — prima ancora del sito.

### Geometrie precise

#### Struttura generale

| Elemento | Misura relativa |
|---|---|
| Larghezza blocco | Full-width, edge-to-edge |
| Sfondo | Nero pieno o quasi-nero |
| Padding laterale card | `1rem` |
| Separatore tra result card | `1px` o spazio verticale `0.5rem–0.75rem` |

#### Filtri pill (top)

| Elemento | Misura relativa |
|---|---|
| Altezza pill | `2rem–2.25rem` |
| Padding interno pill | `0.75rem–1rem` laterale · `0.375rem–0.5rem` verticale |
| Border-radius pill | `9999px` |
| Font | `0.8125rem` |
| Gap tra pill | `0.5rem` |
| Rail | Scrollabile orizzontalmente |

#### Singola result card

| Elemento | Misura relativa |
|---|---|
| Altezza card | `8rem–10rem` circa |
| Padding verticale interno | `0.75rem–1rem` top · `0.75rem` bottom |
| Badge sponsor | `0.7rem` |
| Nome attività | `1rem` · bold · 1 riga troncata |
| Stelle | altezza visiva `0.875rem–1rem` |
| Punteggio numerico | `0.875rem` |
| Conteggio recensioni | `0.875rem` |
| Categoria | `0.8125rem` |
| Stato apertura | `0.8125rem` |
| Orario riapertura | `0.8125rem` |
| Distanza + modalità | `0.8125rem` |
| Snippet annuncio | max 2 righe · `0.8125rem` |
| Thumbnail immagini | 2 foto in colonna · ratio `1:1` · lato `4rem–4.5rem` · border-radius `0.25rem–0.5rem` |
| Gap testo ↔ thumbnail | `0.75rem` |

#### Bottoni CTA inline

| Elemento | Misura relativa |
|---|---|
| Altezza bottone | `2rem–2.25rem` |
| Padding interno | `0.75rem–0.875rem` laterale |
| Border-radius | `9999px` |
| Bordo | `1px` |
| Sfondo | Trasparente |
| Font | `0.8125rem` |
| Icona | `0.875rem–1rem` |
| Gap tra bottoni | `0.5rem` |

#### Barra di ricerca persistente

| Elemento | Misura relativa |
|---|---|
| Altezza | `2.75rem–3.25rem` |
| Posizione | Fixed bottom |
| Contenuto | lente + query attiva |
| Sfondo | grigio scuro o nero |

### Dark mode
- Sfondo: `#000` o quasi-nero
- Testo primario: bianco
- Testo secondario: grigio
- Stelle: giallo Google
- Aperto: verde Google
- Chiuso: rosso Google
- Bottoni CTA: outline grigio

### Implicazioni per il sito
| Elemento SERP | Azione sul sito/GBP |
|---|---|
| Nome troncato a 1 riga | Prime parole = keyword principali |
| Rating + recensioni | Sollecitare recensioni Google |
| Snippet annuncio 2 righe | Keyword nella prima parte |
| 2 thumbnail `1:1` | Caricare foto quadrate di alta qualità |
| Bottone "Sito web" | Sito rapido da mobile |

### Target devices
Mobile esclusivo — layout nativo Google Maps browser mobile. Desktop: Local Pack differente.

### Posizione tipica
SERP Google — risultati locali per ricerche con intento locale.

### Formato compatto
Dark mode. Filtri pill alti `2rem–2.25rem`. Card alte `8rem–10rem`: nome, rating, snippet 2 righe, 2 thumbnail `1:1` da `4rem–4.5rem`, CTA pill alte `2rem–2.25rem`. Barra ricerca fixed bottom alta `2.75rem–3.25rem`.

### Fonte
Google Maps — SERP locale, mobile browser iOS (screenshot notturno)
