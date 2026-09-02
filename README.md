# Carla's Cleaning — landing site

Static one-page site for **Carla Gonzalez Perez** / Carla's Cleaning.

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

## Deploy

### Render (preferred)
1. Re-authenticate Render MCP in Cursor (`list_workspaces` currently returns unauthorized).
2. Create static site from https://github.com/bshoemak2/carlas-cleaning-landing branch `brief-compliant`
3. Build command: `true` · Publish directory: `.`

### Cloudflare Pages
```bash
npx wrangler@3 login
npx wrangler@3 pages deploy . --project-name=carlas-cleaning
```
(Wrangler not logged in on this box; Node 20 needs wrangler@3 or Node ≥22.)

### Note
Keep using the email-only brief. A parallel copy is at `/workspace/carla-cleaning-landing-brief-compliant/`.
