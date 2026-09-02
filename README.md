# Carla's Cleaning — landing site

Static one-page site for **Carla Gonzalez Perez** / Carla's Cleaning.

## Files

- `index.html` — page content (English default, bilingual-ready)
- `styles.css` — mobile-first styles
- `README.md` — this file

## Contact on page (do not invent extras)

- Email only: **carlashoe@icloud.com** (mailto for quote/book)
- No phone, address, licenses, reviews, prices, cities, or social links
- Service area: **TBD — ask when you book**

## Local preview

```bash
cd /workspace/carla-cleaning-landing
python3 -m http.server 8080
# or: npx --yes serve -l 8080
```

Open http://localhost:8080

## Deploy to Render (preferred)

1. Repo / branch for brief-compliant files: use branch `brief-compliant` on https://github.com/bshoemak2/carlas-cleaning-landing
2. [New Static Site](https://dashboard.render.com/static/new):
   - **Build Command:** `true`
   - **Publish Directory:** `.`
   - **Branch:** `brief-compliant`

**Blocker:** Render MCP `list_workspaces` returns `unauthorized`. Re-auth Render in Cursor, then deploy.

## Deploy to Cloudflare Pages

```bash
npx wrangler@3 login
npx wrangler@3 pages deploy . --project-name=carlas-cleaning
```

**Blocker:** Wrangler not logged in. Node on box is v20; use `wrangler@3` or upgrade to Node ≥22.

## Note on `main`

Other agents have been pushing phone / Instagram / Facebook / invented bio onto `main`. This folder and the `brief-compliant` branch follow the brief: email only.
