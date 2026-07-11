# SERP e Ads

Layout di risultati di ricerca, Local Pack Google, schede attività e formati pubblicitari. Blocchi non implementati direttamente nel sito ma fondamentali come riferimento per ottimizzazione SEO locale, Google Ads e struttura delle informazioni aziendali.

---

## BLOCK-017 — Local Business SERP card (Google Maps Local Pack)

### Descrizione
Layout nativo di Google Maps / Local Pack su mobile in dark mode. Mostra i risultati di ricerca locale per attività commerciali con rating, distanza, orari, snippet di annuncio e bottoni CTA inline. È il blocco che l'utente vede **prima** di arrivare al sito — rappresenta il primo touchpoint visivo del brand nella SERP. Documentato come riferimento per ottimizzare la scheda Google Business Profile e il copy degli annunci Google Ads.

### Struttura di ogni result card
- **Label "Sponsorizzato"**: badge testo sopra il nome, presente sugli annunci a pagamento
- **Nome attività**: testo bold, può essere troncato con ellipsis se lungo — importante che le prime parole siano riconoscibili
- **Rating**: stelle gialle + punteggio numerico + conteggio recensioni in parentesi `(537)`
- **Categoria attività**: testo muted, es. "Arredo bagno", "Fornitore di materiali da cos..."
- **Stato apertura**: testo colorato — rosso `Chiuso` o verde `Aperto` + orario di riapertura
- **Distanza + modalità**: es. "km 2,980" + "Acquisti in negozio" — dati contestuali
- **Snippet annuncio**: 2 righe di testo SEA/SEO — le prime parole sono cliccabili come link, resto come testo normale. Massimo ~60–70 caratteri visibili
- **Thumbnail immagini**: 2 foto quadrate (~1:1) in colonna a destra della card — immagini del negozio o dei prodotti
- **3 bottoni CTA inline**: pill outline grigio — `📞 Chiama` · `🌐 Sito web` · `↗ Indicazioni` — sempre visibili, mai nascosti

### Filtri in cima
- Rail scrollabile orizzontale di pill outline: es. "Aperti adesso", "Valutazioni migliori"
- Pill attiva = bordo più marcato o sfondo filled
- Filtrano i risultati senza ricaricare la pagina

### Barra di ricerca persistente
- Fixed bottom, mostra la query attiva (es. "arredo bagno")
- Sempre visibile durante lo scroll — permette di modificare la ricerca

### Dark mode
- Sfondo: nero puro `#000` o quasi-nero
- Testo primario: bianco
- Testo secondario: grigio chiaro
- Stelle: giallo
- Stato chiuso: rosso brand Google
- Stato aperto: verde brand Google
- Bottoni CTA: outline grigio medio su sfondo scuro

### Implicazioni per il sito
| Elemento SERP | Azione sul sito/GBP |
|---|---|
| Nome attività troncato | Mettere le parole chiave principali nelle prime 25 caratteri |
| Rating + recensioni | Sollecitare attivamente recensioni Google — visibili prima del sito |
| Snippet annuncio | Scrivere headline Google Ads con keyword nella prima parola |
| Thumbnail immagini | Caricare foto ad alta qualità su Google Business Profile |
| Bottone "Sito web" | Il sito deve caricare in <2s da mobile — è il click successivo |
| Categoria attività | Scegliere la categoria GBP più specifica e pertinente |

### Target devices
**Mobile esclusivo** — questo layout è nativo dell'app Google Maps e del browser mobile Google. Su desktop il Local Pack ha un layout diverso (3 risultati in colonna con mappa affiancata).

### Posizione tipica
SERP Google — risultati locali, tipicamente dopo i risultati organici o in posizione #1 per ricerche con intento locale (es. "arredo bagno [città]", "piastrelle vicino a me").

### Formato compatto
Dark mode. Filtri pill top. Card: nome bold + stelle + categoria + stato aperto/chiuso + distanza + snippet 2 righe + 2 thumbnail destra + 3 bottoni CTA pill inline. Barra ricerca fixed bottom.

### Fonte
Google Maps — SERP locale, mobile browser iOS (screenshot notturno)
