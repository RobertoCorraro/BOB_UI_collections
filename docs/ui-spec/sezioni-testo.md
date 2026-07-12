# Sezioni testo e copy

Blocchi a dominanza testuale: mission, valori, lista servizi, manifesti, about. Nessuna immagine primaria — la gerarchia è costruita interamente con tipografia, peso, colore e spaziatura.

---

## BLOCK-021 — Editorial mission block con video embed e social proof card

### Descrizione
Blocco desktop a dominanza testuale con headline display centrata a peso misto (bold nero + regular grigio nello stesso paragrafo), affiancata da un video embed a sinistra e una social proof card a destra. Il pattern bilancia narrazione del brand, prova sociale e contenuto multimediale in un’unica sezione compatta.

### Struttura
- **Label categoria** (top-center): testo uppercase o slash-prefixed muted (es. `/Features`) — ancora di sezione
- **Headline display centrata**: testo grande multiriga con **mix bold/muted nello stesso paragrafo** — le parole chiave in nero bold, il testo descrittivo continuo in grigio regular — crea gerarchia senza usare dimensioni diverse
- **Video embed** (bottom-left, ~`60%–65%` larghezza): rettangolo con border-radius, play button circolare centrato, label nome speaker bottom-left, citazione testimonial bottom come caption con cursore animato
- **Social proof card** (bottom-right, ~`30%–35%` larghezza): card bianca con brand label, categoria `insights`, nome speaker grande, waveform audio, avatar circolare + testo breve di raccomandazione

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale blocco | Contenitore centrato, max `64rem–72rem` |
| Padding laterale | `1.5rem–3rem` |
| Label categoria | `0.75rem` · uppercase · tracking ampio · muted · centrata |
| Headline display | `2rem–3rem` · multiriga · centrata · max `52rem` di larghezza |
| Gap headline → zona media | `2rem–3rem` |
| Video embed larghezza | `60%–65%` della larghezza disponibile |
| Video embed ratio | `16:9` |
| Video border-radius | `0.75rem–1rem` |
| Play button | Cerchio `3rem–3.5rem` · centrato · sfondo semitrasparente |
| Label speaker video | `0.75rem` · bianco · bottom-left del video |
| Caption testimonial | `0.875rem–1rem` · bottom del video · corsivo o regular · con cursore `|` |
| Social proof card larghezza | `30%–35%` della larghezza disponibile |
| Social proof card padding | `1rem–1.25rem` |
| Nome speaker card | `1.5rem–1.75rem` · bold |
| Waveform | Elemento grafico thin, muted o brand color |
| Avatar card | Circolare · `2.5rem–3rem` · bottom-right della card |
| Gap video → card | `1rem–1.25rem` |

### Dettaglio tipografico chiave: headline a peso misto
L’headline usa **bold nero per le affermazioni core** e **regular grigio per il completamento della frase**, tutto alla stessa dimensione. Esempio:
> **“We are a team of visionary designers, strategists, and innovators** dedicated to crafting exceptional digital experiences. Our mission is to bridge creativity with functionality,”

Questo crea una scansione visiva immediata: l’occhio legge prima il bold, poi completa con il muted. Nessuna gerarchia di dimensione necessaria.

### Target devices
Desktop (primario). Su tablet: video e card si impilano verticalmente. Su mobile: headline full-width, video sotto full-width, card sotto ancora.

### Posizione tipica
Sezione about/mission nella parte alta della homepage, sezione features/valori, pagina chi siamo — dopo l’hero, prima dei servizi.

### Formato compatto
Label uppercase centrata + headline display bold/muted mista multiriga centrata + video embed `16:9` bottom-left con play e caption testimonial + social proof card bottom-right con speaker, waveform e avatar.

### Fonte
Sito agency / studio design — desktop (screenshot)

---

## BLOCK-022 — Tabella servizi testuale a tre colonne

### Descrizione
Lista servizi strutturata come tabella tipografica a tre colonne con proporzioni fisse: numero progressivo, nome servizio bold, descrizione muted. Nessuna immagine, nessun colore, nessuna icona. La gerarchia è costruita interamente con peso tipografico, dimensioni e colore del testo. Ogni riga è separata da un divisore orizzontale sottile. Pattern pulito, leggibile e rapido da scansire.

### Struttura
- **Heading sezione**: testo flush-left sopra la tabella (es. `Services`) — sans-serif regular/medium, dimensione media
- **Colonna 1** (~`10%–12%`): numero progressivo formato `/01` `/02` `/03` — muted, piccolo, allineato a sinistra — ancora visiva senza peso
- **Colonna 2** (~`25%–30%`): nome servizio — **bold**, dimensione display media — peso principale della riga
- **Colonna 3** (~`58%–65%`): descrizione breve — regular muted, corpo piccolo, max 3 righe — allineata a sinistra
- **Divisore**: `1px` border-bottom muted tra ogni riga

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale blocco | Contenitore con padding `1.5rem–3rem` |
| Colonna numero | `10%–12%` |
| Colonna nome servizio | `25%–30%` |
| Colonna descrizione | `58%–65%` |
| Gap tra colonne | `1rem–2rem` |
| Altezza riga | `auto` · padding verticale `0.875rem–1.25rem` per riga |
| Divisore riga | `1px solid` · colore `rgba(0,0,0,0.1)` o equivalente muted |
| Heading sezione | `1rem–1.25rem` · regular/medium · margin-bottom `1rem–1.5rem` |
| Numero progressivo | `0.75rem–0.875rem` · muted · font-weight 400 |
| Nome servizio | `1.125rem–1.375rem` · font-weight 600–700 |
| Descrizione | `0.75rem–0.875rem` · regular · muted · line-height `1.5` |

### Principio di scansione
L’occhio percorre verticalmente la **colonna 2** (nomi servizi in bold) prima di leggere la descrizione a destra. Il numero muted a sinistra aggiunge ritmo visivo senza distrarre. La struttura permette di aggiungere o rimuovere righe senza rompere il layout.

### Varianti
- Con hover: riga evidenziata con background muted leggero al passaggio del mouse
- Con link: nome servizio cliccabile, freccia `→` che appare on-hover nella colonna 1 al posto del numero
- Con badge: piccolo tag categoria accanto al nome (es. `Design`, `Dev`)

### Target devices
Desktop e tablet (primario). Su mobile: la colonna 3 (descrizione) collassa sotto la colonna 2, il numero rimane piccolo a sinistra.

### Posizione tipica
Sezione servizi nella homepage, pagina dedicata ai servizi, sezione “cosa facciamo” — dopo hero o mission block.

### Formato compatto
Tabella testuale 3 colonne `~11/28/61%`, righe separate da divisore `1px`. Colonna 1: numero `/01` muted piccolo. Colonna 2: nome servizio bold. Colonna 3: descrizione regular muted max 3 righe.

### Fonte
Sito agency / studio design — desktop (screenshot)

---

## BLOCK-023 — Stats & media bento grid

### Descrizione
Bento grid 2×3 asimmetrica che alterna stat card numeriche, blocchi fotografici e un blocco testuale descrittivo. Due palette di cella: dark (grigio scuro, quasi nero) per le stat e light (grigio chiarissimo/bianco) per testo e foto. Ogni stat card include un badge freccia ↗ bottom-right. Il pattern comunica risultati misurabili e credibilità con forte impatto visivo, senza bisogno di grafici o infografiche.

### Struttura celle

**Riga superiore** (3 colonne):
- **Cella 1** (~`25%`, dark): stat numerica grande + label descrittiva sotto + badge ↗ bottom-right
- **Cella 2** (~`47%`, foto): immagine fotografica full-fill, border-radius, nessun testo
- **Cella 3** (~`28%`, dark): stat numerica grande + label descrittiva + badge ↗ bottom-right

**Riga inferiore** (3 colonne):
- **Cella 4** (~`25%`, light): testo descrittivo con parole chiave bold e testo regular muted in mix (stesso pattern BLOCK-021)
- **Cella 5** (~`28%`, dark): stat numerica grande + label descrittiva + badge ↗ bottom-right
- **Cella 6** (~`47%`, foto): immagine fotografica full-fill, border-radius, nessun testo

**Pattern di alternanza colori**: dark/foto/dark — light/dark/foto. Le foto e il blocco testuale rompono la monotonia delle stat card.

### Geometrie precise

| Elemento | Misura relativa |
|---|---|
| Larghezza totale blocco | Full-width con padding contenitore `1.5rem–3rem` |
| Gap tra celle | `0.5rem–0.75rem` |
| Altezza riga | `12rem–16rem` per riga · entrambe le righe uguali |
| Cella stretta (stat/testo) | `~25%–28%` larghezza |
| Cella larga (foto) | `~45%–50%` larghezza |
| Border-radius celle | `1rem–1.25rem` |
| Stat numerica | `2.5rem–3.5rem` · font-weight 700–900 · bianco |
| Label stat | `0.75rem–0.875rem` · regular · bianco/muted chiaro · max 2 righe |
| Gap stat → label | `0.25rem–0.375rem` |
| Badge ↗ | Cerchio `1.75rem–2rem` · bottom-right della cella · sfondo scuro leggermente più chiaro o bordo |
| Padding interno celle stat | `1rem–1.25rem` |
| Cella testo padding | `1rem–1.25rem` |
| Testo cella descrittiva | `0.75rem–0.875rem` · mix bold nero + regular muted |
| Sfondo celle dark | `#1a1a1a`–`#2d2d2d` o colore brand scuro |
| Sfondo celle light | `#f5f5f5`–`#ebebeb` o bianco |
| Immagine foto | `object-fit: cover` · full-fill della cella · nessun overlay |

### Heading sezione
Titolo flush-left sopra la griglia (es. `About Us`) — sans-serif regular/medium, dimensione `1.25rem–1.5rem`, margin-bottom `1rem–1.5rem`.

### Differenza da layout a sole stat

| | Solo stat grid | BLOCK-023 Bento grid |
|---|---|---|
| Celle | Tutte numeriche | Miste: stat + foto + testo |
| Ritmo visivo | Uniforme | Variato per forma e colore |
| Informazione | Solo dati | Dati + contesto visivo + narrativa |
| Impatto | Dati freddi | Dati + brand storytelling |

### Varianti d’uso
- **About Us**: stat di business (x2 conversion, 90% retention) + foto prodotto/team
- **Social proof**: stat clienti + foto ambiente + testo testimonial
- **Risultati campagna**: KPI + foto before/after + testo insight

### Comportamento hover (desktop)
- Celle stat: leggero `scale(1.01)` o cambio opacità badge ↗
- Celle foto: lieve zoom `scale(1.03)` dell’immagine interna
- Badge ↗: cambio colore/fill su hover — segnala navigabilità

### Target devices
Desktop (primario). Su tablet: griglia 2×2 con celle foto full-width. Su mobile: stack verticale, celle stat a piena larghezza, foto con ratio `16:9`.

### Posizione tipica
Sezione “About Us”, “I nostri risultati”, “Perché sceglierci” — nella metà inferiore della homepage, dopo i servizi o prima dei testimonial.

### Formato compatto
Bento grid 2×3, gap `0.5rem–0.75rem`, border-radius `1rem`. Alternanza dark (stat + badge ↗) / foto / light (testo bold+muted). Stat numerica `2.5rem–3.5rem` bold bianca + label small.

### Fonte
Sito agency / studio design — sezione About Us, desktop (screenshot)
