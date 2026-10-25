# a2d2.dev

Source for the static site of **A²D² — Agentic Agile Driven Development** (智能体敏捷驱动开发), served at <https://a2d2.dev>.

- Plain HTML/CSS, no build step:
  - `index.html` — homepage: “The next agile is agentic.” plus the three essays A²D² starts from (English titles and abstracts, linking to the Chinese originals)
  - `essays/index.html` — `/essays`: the three essays as one English long-form essay, by @neolf (Neov)
  - `zh/index.html`, `zh/essays/index.html` — Chinese counterparts at `/zh` and `/zh/essays` (hreflang-linked; English is x-default)
  - `style.css`, `favicon.svg`, `og.png`
  - `vercel.json` — `cleanUrls` / no trailing slash, so `/essays`, `/zh`, `/zh/essays` are the canonical URLs
- Type: Source Serif 4 (headings, long-form) + Inter (UI, abstracts) from Google Fonts with `display=swap`; Chinese pages add Noto Serif SC 600 for headings, body uses the system Chinese sans stack. Light ivory theme with a quiet dark mode.
- Vercel Web Analytics is loaded on every page via `/_vercel/insights/script.js` (active once Web Analytics is enabled for the Vercel project).
- Deployed on Vercel; every push to `main` deploys to production, other branches get preview deployments.
- Links: <https://github.com/a2d2-dev> · X: [@a2d2dev](https://x.com/a2d2dev) · [@neolf](https://x.com/neolf)

Preview locally: `python3 -m http.server`, then open <http://localhost:8000/> (directory URLs get a trailing slash locally; Vercel serves them without).
