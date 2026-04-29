# Tree of Decisions

A decision-mapping tool built around a simple idea: every significant decision has fruit — consequences that ripple forward in time, some immediate and some long-term. This project visualizes those decisions and their fruit as an interactive tree, with each node linked to the decisions that made it possible.

## What It Is

Decisions are nodes. Fruit flows downward. The tree shows how choices create the conditions for future choices — and how consequences compound over time.

Node types:
- **Gold nodes** — God's decisions
- **Other colors** — Human decisions (TBD as the project grows)

The visualization is built with D3.js: dark background, upward-growing branches, hover to see the full fruit of each decision.

## First Project: The Bible

Our first mapping project is the entire Bible — worked through passage by passage, from Genesis forward.

**Genesis 1** is the starting point. The first chapter contains no human decisions at all — it is a pure cascade of divine choices, each one creating the substrate for the next. When the first human decision arrives in Chapter 3, it will land with full visual weight against that gold background. The tree will make visible what biblical commentary rarely shows in this form.

**Live visualization:** [https://jkh2.github.io/tree-of-decisions/](https://jkh2.github.io/tree-of-decisions/)

## Progress

**59 nodes mapped across Genesis 1–4**

| Chapter | Scope | Nodes | Status |
|---------|-------|-------|--------|
| Genesis 1 | The Creation Week — Days 1–7, naming, blessings, dominion commission | 13 | ✅ Complete |
| Genesis 2 | Garden, vocation, first command, woman, marriage covenant | 18 | ✅ Complete |
| Genesis 3 | Serpent, the Fall, judgments, Protoevangelium, garments, banishment | 15 | ✅ Complete |
| Genesis 4 | Cain and Abel, God's warning, murder, pursuit, mercy on Cain, Seth, first worship | 13 | ✅ Complete |
| Genesis 5–9 | Genealogies, Noah, the Flood | — | 🔜 Next |

**Node types in use:**
- 🟡 Gold — God's decisions
- 🔵 Blue — Human decisions
- 🟢 Green — Commands
- 🟣 Purple — Blessings
- 🩵 Teal — Promises (good)
- 🟠 Orange — Promises (warning)
- 🔴 Dark red — Adversary

## Data Format

Decision data lives in `data/` as JSON files. Each file maps a passage or chapter. The schema:

```json
{
  "id": "unique-id",
  "label": "Short label",
  "actor": "God | Human name",
  "decision": "What was decided",
  "immeditae_fruit": "What followed immediately",
  "long_term_fruit": "What this made possible over time",
  "reference": "Genesis 1:1",
  "children": []
}
```

## Running Locally

Open `index.html` directly in a browser — no server required. Data is embedded inline.

## Built With

- [D3.js v7](https://d3js.org/) — tree layout and SVG rendering
- Vanilla HTML/CSS/JS — no build step
