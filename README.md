# Retasc docs

Source for **[docs.retasc.com](https://docs.retasc.com)** — the Retasc onboarding +
billing documentation, built with [Mintlify](https://mintlify.com).

Mintlify deploys this repo on every push to `main`.

## Structure

| File | What |
|------|------|
| `docs.json` | Mintlify config — theme, navigation, custom domain |
| `style.css` | Brand styling ported from the retasc.com landing (dark, `#5a9fd4`, Space Grotesk / Inter / JetBrains Mono) |
| `index.mdx` | Landing / overview |
| `quickstart.mdx` | One-command onboarding (`retasc init`) |
| `onboarding.mdx` | Full onboarding walkthrough |
| `billing.mdx` | Metering, rate card, spending cap, re-authorization |
| `logo/`, `favicon.svg` | Brand assets |

## Local preview

```bash
npm i -g mint
mint dev
```

> Note: these pages are also mirrored in the `retasc` monorepo under `docs/`
> (added in RTSC-60). This repo is the Mintlify deploy source.
