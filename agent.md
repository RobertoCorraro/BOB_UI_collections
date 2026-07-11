# Agent Skills — Web Design & UI/UX

Questo file definisce le competenze e i principi operativi da applicare quando si lavora con i blocchi della collezione BOB_UI_collections. Serve come riferimento per agenti AI, designer e developer che usano questa repo.

---

## Core skills

### Lettura del layout
- Identificare la struttura a griglia di un blocco: numero di colonne, gerarchia visiva, distribuzione del peso visivo
- Riconoscere il pattern compositivo (simmetrico, asimmetrico, collage, lista, griglia uniforme)
- Distinguere blocchi orientati alla scoperta (discovery) da blocchi orientati ai risultati (results)

### Ratio e proporzioni
- Applicare ratio standard: `1:1` (quadrato), `4:5` (verticale social), `3:4` (ritratto), `16:9` (landscape), `2:5` e `1:3` (portrait stretto per caroselli compatti)
- Mantenere coerenza di ratio all’interno dello stesso blocco
- Non deformare le immagini: usare sempre `object-fit: cover` con punto focale centrato o definito
- Le proporzioni tra aree (es. colonna sinistra `62%` vs destra `28%`) si esprimono sempre in `%` relativa al contenitore, mai in pixel

### Unità di misura — regola fondamentale

**Non usare mai pixel fissi nelle specifiche geometriche.** Le misure devono essere relative e scalabili:

| Cosa si misura | Unità da usare |
|---|---|
| Testo (font-size, line-height) | `rem` |
| Spaziatura (padding, gap, margin) | `rem` |
| Larghezze di card / colonne | `%` o `vw` |
| Altezze di blocchi / card | `rem` o range descrittivo (`min(52vh, 25rem)`) |
| Icone, avatar, bullet | `rem` |
| Border-radius standard | `rem` (es. `0.75rem`, `1rem`) |
| Border-radius pill | `9999px` |
| Touch target minimo | `2.75rem` (≡ 44px Apple HIG) |
| Ratio immagini | rapporto puro (es. `3:4`) — mai px |

> **Perché:** i pixel fissi non scalano tra device, risoluzioni e zoom. Le unità relative rispettano le preferenze utente, si adattano a tutti i viewport e sono coerenti con il sistema di design.

### Spacing e ritmo visivo
- Usare un sistema di spacing basato su multipli di `0.25rem` (equivalente ai multipli di 4px nella logica 1rem=16px)
- Padding laterale su mobile: `1rem–1.5rem` (equivalente a 16–24px)
- Gap uniforme tra card nello stesso blocco: `0.5rem–0.75rem`
- Distinguere padding interno alla card da gap tra card

### Tipografia nei blocchi
- Titoli delle card: massimo 2 righe, troncati con `text-overflow: ellipsis`
- Metadati secondari: font-size ridotto (`0.75rem` circa), colore secondario
- Label nei rail orizzontali: testo breve, leggibile su sfondo immagine se in overlay
- Uppercase solo per badge, metadati istituzionali e label di sezione — mai per titoli card

### Comportamento responsive
- **Mobile-first**: progettare per `375–390px` larghezza (in pratica: contenitore fluido)
- **Tablet**: adattare il layout espandendo colonne o aumentando dimensione card (`min-width: 48rem`)
- **Desktop**: valutare se il blocco scala o va ripensato in un container dedicato (`min-width: 75rem`)
- I blocchi con scroll orizzontale (rail) sono nativi da touch: su desktop valutare la transizione a griglia
- I breakpoint si esprimono sempre in `rem` (es. `48rem`, `75rem`), mai in px

### Touch e interazione
- Touch target minimo: `2.75rem × 2.75rem` (equivalente a 44×44px, Apple HIG)
- Elementi tappabili chiaramente distinti da decorativi
- Feedback visivo al tap: stato pressed, highlight o ripple
- Evitare elementi interattivi troppo vicini su mobile

---

## Pattern di riferimento

### Asymmetric media collage
- Usare quando si vuole presentare un set di contenuti con forte gerarchia visiva
- Il blocco principale deve avere peso visivo dominante
- Layout `50/50`, gap `0.25rem`, zero border-radius, edge-to-edge

### Horizontal discovery rail
- Usare per stimolare la navigazione laterale e la scoperta di categorie correlate
- Le card mostrano parzialmente l’elemento successivo (overflow intenzionale)
- Card `1:1` da `5rem–6rem`, abbinate a lista di query sotto

### Two-column results grid
- Usare per elenchi di risultati omogenei (prodotti, immagini, articoli)
- Card uniformi con altezza percepita costante
- Griglia `1fr 1fr`, gap `0.5rem–0.75rem`, padding laterale `0.75rem–1rem`

---

## Checklist prima di aggiungere un blocco

- [ ] Il blocco ha un nome componente chiaro e univoco
- [ ] Il ratio delle immagini è definito
- [ ] Le geometrie usano esclusivamente unità relative (`rem`, `%`, `vw`, `vh`)
- [ ] I target devices sono specificati
- [ ] La fonte (app o sito) è documentata
- [ ] Il formato compatto è scritto in 1–2 righe
- [ ] Lo screenshot è disponibile o segnato come TODO in `assets/screenshots/`
- [ ] Il blocco è stato testato visivamente su mobile

---

## Principi generali

- **Mobile-first sempre**: se un blocco non funziona su mobile, non entra in collezione
- **Unità relative sempre**: nessun pixel fisso nelle specifiche — solo `rem`, `%`, `vw`, `vh`
- **Fonte reale**: ogni blocco deve provenire da un pattern osservato su un prodotto reale
- **Conversion-oriented**: privilegiare blocchi che guidano l’utente verso un’azione chiara
- **Coerenza visiva**: ratio, spacing e tipografia devono essere coerenti tra i blocchi della stessa pagina
- **No decor fine a se stesso**: ogni elemento visivo deve avere una funzione informativa o di navigazione
