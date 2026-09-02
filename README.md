# Carla's Cleaning — landing page

Static one-page site for Carla Gonzalez Perez’s home cleaning business.

## Contact (do not invent extras)

- Phone: **786-578-7462**
- Email: **carlashoe@icloud.com**
- Instagram: **[@gpcl77](https://www.instagram.com/gpcl77)**
- Service area: **TBD — ask when you book**
- No invented prices, reviews, licenses, or addresses

## Local preview

```bash
cd /workspace/carla-cleaning-landing
python3 -m http.server 8080
```

Open http://127.0.0.1:8080

## Deploy

Prefer **Render Static Site** or **Cloudflare Pages**:

- Publish directory: site root (this folder)
- Build command: none (or `echo ready`)
- `index.html` + `styles.css` at publish root

## Repository & live preview

- GitHub: https://github.com/bshoemak2/carlas-cleaning-landing
- GitHub Pages (fallback while Render/Cloudflare auth blocked): https://bshoemak2.github.io/carlas-cleaning-landing/

### Deploy blockers noted

- **Render MCP** (`user-Render`): `list_workspaces` returns `unauthorized`; cannot select workspace or call `create_static_site` successfully. Re-authenticate the Render MCP integration in Cursor, then create a static site with build `true` and publish path `./` from this repo.
- **Cloudflare Wrangler**: not logged in (`wrangler whoami`). Node on this box is v20; latest Wrangler wants Node ≥22 — use `npx wrangler@3` after `wrangler login`, or upgrade Node.
