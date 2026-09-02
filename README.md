# Carla's Cleaning — landing site

Static one-page site for **Carla Gonzalez Perez** / Carla's Cleaning.

## Files

- `index.html` — page content (English default, bilingual-ready)
- `styles.css` — mobile-first styles
- `README.md` — this file

## Contact on page

- Email only: **carlashoe@icloud.com** (mailto for quote/book)
- No phone, address, licenses, reviews, prices, or cities
- Service area: **TBD — ask when you book**

## Local preview

From this folder:

```bash
# Option A — Python
python3 -m http.server 8080

# Option B — npx serve
npx --yes serve -l 8080
```

Then open http://localhost:8080

## Deploy to Render (static site)

1. Push this folder to a **public** GitHub repo (or a private repo connected to Render).
2. In [Render Dashboard → New Static Site](https://dashboard.render.com/static/new):
   - **Build Command:** `true` (no build step)
   - **Publish Directory:** `.` (or leave as `./`)
3. Or with Render MCP / API after the repo exists:
   - `create_static_site` with `buildCommand: "true"`, `publishPath: "./"`, and the Git repo URL.
4. Confirm the live `*.onrender.com` URL after the first deploy succeeds.

## Deploy to Cloudflare Pages

1. Install and log in: `npx wrangler login`
2. From this folder:

```bash
npx wrangler pages project create carlas-cleaning
npx wrangler pages deploy . --project-name=carlas-cleaning
```

3. Use the URL Wrangler prints (e.g. `*.pages.dev`).

## SEO / Search Console

- Meta title and description are set in `index.html` `<head>`.
- After deploy, add the property in Google Search Console and verify ownership.
