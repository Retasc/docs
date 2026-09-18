# Retasc docs

Source for **[docs.retasc.com](https://docs.retasc.com)**. Mintlify deploys this
repo on every push to `main`.

The look is the design system on Mintlify's shell (`style.css`,
`operations/design-system.md` §docs.retasc.com in the monorepo). The reference
tables, pictures of the Dash, icons, wordmark, favicon and social cards are
**generated from the monorepo**, not typed here:

| From the monorepo | Into this repo |
|---|---|
| `scripts/docs-facts.py` | tool table in `mcp-tools.mdx`, command table in `cli.mdx`, proof sentence on `index.mdx`, one OG card per page |
| `scripts/docs-shots.py` | `images/ui/` — four cuts a Dash screen (two palettes × two widths) |
| `scripts/docs-icons.py` | `icons/` (Radix) and every `icon=` on a page |
| `scripts/gen-icons.py` | `favicon.svg`, `logo/{dark,light}.svg` |
| `scripts/gen-og-guides.py --docs` | `images/og/<slug>.png` (also run by docs-facts) |

`--check` on those scripts fails CI in the monorepo when this checkout is behind.
Do not edit the generated blocks by hand; they are marked
`{/* docs-facts:… */}`.

## Structure

| File | What |
|------|------|
| `docs.json` | Mintlify config: theme, navigation, custom domain |
| `style.css` | Design-system tokens on Mintlify's shell |
| `*.mdx` | Pages |
| `logo/`, `favicon.svg` | Wordmark and favicon, from `gen-icons.py` |
| `icons/` | Radix set, from `docs-icons.py` |
| `images/ui/` | Dash captures |
| `images/og/` | Per-page social cards |

## Local preview

```bash
npm i -g mint
mint dev
```
