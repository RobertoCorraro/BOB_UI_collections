# CLAUDE.md

Istruzioni operative per Claude (e altri agenti AI) quando creano o modificano le **demo HTML** dei blocchi in questa repo (`assets/demo/`). Per le regole generali su geometrie, ratio e unità di misura dei blocchi, vedi `agent.md`.

---

## Regola principale: un solo foglio di stile condiviso

Tutte le demo HTML (`assets/demo/*.html`) devono importare **lo stesso file CSS**: [`assets/demo/bob__demo.css`](assets/demo/bob__demo.css).

- Non creare un file `.css` per singolo blocco.
- Non usare blocchi `<style>` inline nell'HTML.
- Non introdurre framework CSS esterni (Bootstrap, Tailwind, ecc.): il CSS è scritto a mano, coerente con le unità relative definite in `agent.md`.

Nel file HTML del blocco, lo stylesheet va importato così (percorso relativo, dato che HTML e CSS vivono entrambi in `assets/demo/`):

```html
<link rel="stylesheet" href="bob__demo.css" />
```

---

## Naming delle classi

Ogni classe deve seguire la struttura:

```
bob__{nome_classe}_{modificatore}
```

- `nome_classe`: nome del componente/elemento, parole separate da `_` (es. `product_card`, `demo_intro_badge`, `section_header`)
- `modificatore`: opzionale, per varianti di stato o stile (es. `old`, `discount`, `new`)
- Esempi reali già in uso: `.bob__product_card`, `.bob__product_card_img_wrap`, `.bob__product_card_badge_discount`

---

## Prima di aggiungere un nuovo blocco

1. **Controlla prima le classi già presenti** in `bob__demo.css` (es. `bob__product_card`, `bob__section_header`, `bob__demo_intro`).
2. Se una classe esistente copre già il bisogno, **riusala** — non duplicarla con un nome diverso o un valore leggermente differente.
3. Se non esiste una classe adatta al nuovo blocco, **aggiungi la nuova classe direttamente a `bob__demo.css`**, seguendo la naming convention sopra e mantenendo il file ordinato per sezione (usa i separatori a commento `/* ─── Nome sezione ─── */` come già presente nel file).
4. Non creare un secondo file CSS, nemmeno per una demo isolata o sperimentale: `bob__demo.css` resta l'unico foglio di stile per tutte le demo HTML della collezione.
5. Se una classe esistente va bene solo in parte, preferisci aggiungere un **modificatore** (`bob__{nome_classe}_{nuovo_modificatore}`) piuttosto che riscrivere la classe base o crearne una parallela.

---

## Perché

- Evita di duplicare stili tra blocchi simili (card, badge, griglie ricorrono spesso tra i pattern raccolti)
- Garantisce coerenza visiva tra le demo: stessi colori, spaziature, radius, breakpoint
- Mantiene le demo leggere: un solo file CSS cacheable dal browser invece di N copie inline o N file separati
