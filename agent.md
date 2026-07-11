# Agent Skills — Web Design & UI/UX

Questo file definisce le competenze e i principi operativi da applicare quando si lavora con i blocchi della collezione BOB_UI_collections. Serve come riferimento per agenti AI, designer e developer che usano questa repo.

---

## Core skills

### Lettura del layout
- Identificare la struttura a griglia di un blocco: numero di colonne, gerarchia visiva, distribuzione del peso visivo
- Riconoscere il pattern compositivo (simmetrico, asimmetrico, collage, lista, griglia uniforme)
- Distinguere blocchi orientati alla scoperta (discovery) da blocchi orientati ai risultati (results)

### Ratio e proporzioni
- Applicare ratio standard: 1:1 (quadrato), 4:5 (verticale social), 3:4 (ritratto), 16:9 (landscape)
- Mantenere coerenza di ratio all’interno dello stesso blocco
- Non deformare le immagini: usare sempre object-fit: cover con punto focale centrato o definito

### Spacing e ritmo visivo
- Usare un sistema di spacing basato su multipli di 4 o 8 px
- Applicare padding laterale consistente (16–24 px su mobile)
- Mantenere gap uniforme tra card nello stesso blocco (8–12 px)
- Distinguere padding interno alla card da gap tra card

### Tipografia nei blocchi
- Titoli delle card: massimo 2 righe, troncati con ellipsis
- Metadati secondari: font size ridotto, colore secondario, non competono con il titolo
- Label nei rail orizzontali: testo breve, leggibile su sfondo immagine se in overlay

### Comportamento responsive
- Mobile-first: progettare prima per 375–390 px di larghezza
- Tablet: adattare il layout espandendo colonne o aumentando dimensione card (768–834 px)
- Desktop: valutare se il blocco scala bene o va ripensato in un container dedicato (1280+ px)
- I blocchi con scroll orizzontale (rail) sono nativi da touch: su desktop valutare la transizione a griglia

### Touch e interazione
- Touch target minimo: 44x44 px (Apple HIG) o 48x48 dp (Material Design)
- Elementi tappabili chiaramente distinti da elementi decorativi
- Feedback visivo al tap: stato pressed, highlight o ripple
- Evitare elementi interattivi troppo vicini tra loro su mobile

---

## Pattern di riferimento

### Asymmetric media collage
- Usare quando si vuole presentare un set di contenuti con forte gerarchia visiva
- Il blocco principale deve avere peso visivo dominante
- Ideale per apertura di sezioni editorial, profili, album

### Horizontal discovery rail
- Usare per stimolare la navigazione laterale e la scoperta di categorie correlate
- Le card devono mostrare parzialmente l’elemento successivo per comunicare lo scroll
- Abbinare sempre a una lista di query o tag sotto per dare un secondo livello di accesso

### Two-column results grid
- Usare per elenchi di risultati omogenei (prodotti, immagini, articoli)
- Le card devono avere altezza percepita uniforme per facilitare la scansione
- Includere sempre titolo e almeno un metadato secondario (fonte, autore, categoria)

---

## Checklist prima di aggiungere un blocco

- [ ] Il blocco ha un nome componente chiaro e univoco
- [ ] Il ratio delle immagini è definito
- [ ] I target devices sono specificati
- [ ] La fonte (app o sito) è documentata
- [ ] Il formato compatto è scritto in una riga
- [ ] Lo screenshot è disponibile o segnato come TODO in `assets/screenshots/`
- [ ] Il blocco è stato testato visivamente su mobile (almeno in anteprima)

---

## Principi generali

- **Mobile-first sempre**: se un blocco non funziona su mobile, non entra in collezione
- **Fonte reale**: ogni blocco deve provenire da un pattern osservato su un prodotto reale
- **Conversion-oriented**: privilegiare blocchi che guidano l’utente verso un’azione chiara
- **Coerenza visiva**: ratio, spacing e tipografia devono essere coerenti tra i blocchi della stessa pagina
- **No decor fine a se stesso**: ogni elemento visivo deve avere una funzione informativa o di navigazione
