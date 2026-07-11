# SERP e Ads

Layout di risultati di ricerca, Local Pack Google, schede attività e formati pubblicitari. Blocchi di riferimento per ottimizzazione SEO locale, Google Ads e struttura delle informazioni aziendali.

---

## BLOCK-017 — Local Business SERP card (Google Maps Local Pack)

### Descrizione
Layout nativo di Google Maps / Local Pack su mobile in dark mode. Mostra i risultati di ricerca locale per attività commerciali con rating, distanza, orari, snippet di annuncio e bottoni CTA inline. È il primo touchpoint visivo del brand nella SERP — prima ancora del sito.

### Geometrie precise

#### Struttura generale

| Elemento | Misura |
|---|---|
| Larghezza blocco | Full-width, edge-to-edge |
| Sfondo | Nero ~**#000** (dark mode nativa Google) |
| Padding laterale card | **16px** |
| Separatore tra result card | Linea **1px** grigio scuro o spazio verticale **8–12px** |

#### Filtri pill (top)

| Elemento | Misura |
|---|---|
| Altezza pill | **32–36px** |
| Padding interno pill | **12–16px** laterale · **6–8px** verticale |
| Border-radius pill | **20px** (pill completa) |
| Font | Font-size **0.8125rem** · regular · colore bianco/grigio chiaro |
| Gap tra pill | **8px** |
| Rail | Scrollabile orizzontalmente · overflow-x visible |

#### Singola result card

| Elemento | Misura |
|---|---|
| Altezza card approssimativa | ~**130–160px** (dipende dallo snippet) |
| Padding verticale interno | **12–16px** top · **12px** bottom |
| Badge "Sponsorizzato" | Font-size **0.7rem** · regular · colore grigio chiaro · sopra il nome |
| Nome attività | Font-size **1rem** · bold · bianco · max 1 riga troncato |
| Stelle | Altezza **14–16px** · colore giallo Google `#FBBC04` |
| Punteggio numerico | Font-size **0.875rem** · bold · bianco |
| Conteggio recensioni | Font-size **0.875rem** · regular · grigio chiaro · tra parentesi |
| Categoria | Font-size **0.8125rem** · regular · grigio chiaro muted |
| Stato apertura | Font-size **0.8125rem** · rosso `#EA4335` (chiuso) o verde `#34A853` (aperto) |
| Orario riapertura | Font-size **0.8125rem** · grigio chiaro · inline dopo lo stato |
| Distanza + modalità | Font-size **0.8125rem** · grigio chiaro |
| Snippet annuncio | **2 righe** max · font-size **0.8125rem** · grigio chiaro · prime parole come link colorato |
| Thumbnail immagini | **2 foto** in colonna verticale · formato **~1:1** · larghezza ~**64–72px** · border-radius **4–8px** · posizione destra |
| Gap testo ↔ thumbnail | **12px** |

#### Bottoni CTA inline

| Elemento | Misura |
|---|---|
| Altezza bottone | **32–36px** |
| Padding interno | **12–14px** laterale |
| Border-radius | **20px** (pill) |
| Bordo | **1px** grigio medio |
| Sfondo | Trasparente (ghost/outline) |
| Font | Font-size **0.8125rem** · regular · bianco |
| Icona | **14–16px** · allineata sinistra del testo |
| Gap tra bottoni | **8px** |
| Bottoni | `📞 Chiama` · `🌐 Sito web` · `➡ Indicazioni` — sempre tutti e tre visibili |

#### Barra di ricerca persistente (fixed bottom)

| Elemento | Misura |
|---|---|
| Altezza | **44–52px** |
| Posizione | Fixed bottom, sopra la home bar iOS |
| Contenuto | Icona lente + query attiva (es. "arredo bagno") |
| Sfondo | Grigio scuro o nero |

### Dark mode
- Sfondo: `#000` o quasi-nero
- Testo primario: bianco `#FFF`
- Testo secondario: grigio `#9AA0A6`
- Stelle: giallo `#FBBC04`
- Aperto: verde `#34A853`
- Chiuso: rosso `#EA4335`
- Bottoni CTA: outline grigio `1px #5F6368`

### Implicazioni per il sito
| Elemento SERP | Azione sul sito/GBP |
|---|---|
| Nome troncato a 1 riga | Prime 25 caratteri = parole chiave principali |
| Rating + recensioni | Sollecitare attivamente recensioni Google |
| Snippet annuncio 2 righe | Headline Google Ads: keyword nella prima parola |
| 2 thumbnail 1:1 | Caricare foto quadrate ad alta qualità su GBP |
| Bottone "Sito web" | Sito deve caricare in <2s da mobile |

### Target devices
**Mobile esclusivo** — layout nativo Google Maps browser mobile. Desktop: Local Pack a 3 colonne con mappa affiancata.

### Posizione tipica
SERP Google — risultati locali per ricerche con intento locale ("arredo bagno [città]", "piastrelle vicino a me").

### Formato compatto
Dark mode #000. Filtri pill 32px top scrollabili. Card ~140px: badge sponsor + nome bold bianco + stelle gialle + punteggio + categoria grigia + stato rosso/verde + distanza + snippet 2 righe + 2 thumbnail 1:1 64px destra + 3 CTA pill ghost 32px. Barra ricerca fixed bottom 48px.

### Fonte
Google Maps — SERP locale, mobile browser iOS (screenshot notturno)
