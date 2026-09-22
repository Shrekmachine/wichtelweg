# Deployment — Westhofener Wichtelweg

## Live targets

| Item | Value |
| --- | --- |
| GitHub | https://github.com/Shrekmachine/wichtelweg |
| Cloudflare Pages project | `wichtelweg` |
| Preview subdomain | https://wichtelweg.pages.dev |
| Custom domain (pending) | `westhofenerwichtel.de` |

Cloudflare account used for this project: the account connected via Cursor Cloudflare MCP (Workers & Pages).

## Build settings (Pages)

| Setting | Value |
| --- | --- |
| Production branch | `main` |
| Build command | `npm run build` |
| Build output directory | `dist` |
| Root directory | `/` |
| Node | ≥ 22.12 (Astro engine requirement) |

## First deploy options

### A) Dashboard + Git (recommended for ongoing work)

1. Open [Workers & Pages](https://dash.cloudflare.com/?to=/:account/workers-and-pages) → project **wichtelweg**.
2. **Settings → Builds** → connect GitHub repository `Shrekmachine/wichtelweg` (Cloudflare Workers & Pages GitHub App).
3. Confirm build settings above → save. Push to `main` triggers production deploys.

### B) Local Wrangler (direct upload)

```sh
npx wrangler login
npm run pages:deploy
```

(`pages:deploy` = `npm run build` + `wrangler pages deploy dist --project-name=wichtelweg`)

## Custom domain

When `westhofenerwichtel.de` is ready:

1. Add the domain in the Pages project (**Custom domains**).
2. Point DNS at Cloudflare (or follow the Dashboard CNAME instructions).
3. Update `site` in `astro.config.mjs` if the canonical URL changes (already set to `https://westhofenerwichtel.de`).
