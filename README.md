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

1. Repo: https://github.com/bshoemak2/carlas-cleaning-landing
2. [New Static Site](https://dashboard.render.com/static/new):
   - **Build Command:** `true`
   - **Publish Directory:** `.`
3. After Render MCP is re-authenticated: `create_static_site` with those settings + the GitHub repo URL.

**Blocker:** Render MCP `list_workspaces` returns `unauthorized`. Re-auth the Render integration in Cursor, then deploy.

## Deploy to Cloudflare Pages

```bash
npx wrangler@3 login
npx wrangler@3 pages project create carlas-cleaning
npx wrangler@3 pages deploy . --project-name=carlas-cleaning
```

**Blocker:** Wrangler not logged in on this box. Latest Wrangler wants Node ≥22; use `wrangler@3` on Node 20 or upgrade Node.

## Live URL (GitHub Pages fallback)

https://bshoemak2.github.io/carlas-cleaning-landing/

## SEO / Search Console

Meta title and description are in `index.html` `<head>`. After deploy, add the property in Google Search Console.
