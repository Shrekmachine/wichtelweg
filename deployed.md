# Deployment — Westhofener Wichtelweg

## Live targets

| Item | Value |
| --- | --- |
| GitHub | https://github.com/Shrekmachine/wichtelweg |
| Cloudflare Pages project | `wichtelweg` |
| Pages preview | https://wichtelweg.pages.dev |
| Custom domain | https://westhofenerwichtel.de (+ `www`) |

Cloudflare account: **Krav Maga Südwest** (same account as the Pages project).

**Pages:** Git-Connect on `main` → build `npm run build` → output `dist`.

## Custom domain setup (2026-09-22)

Done in Cloudflare:

- Pages custom domains: `westhofenerwichtel.de`, `www.westhofenerwichtel.de`
- DNS CNAMEs (proxied) → `wichtelweg.pages.dev`
- Mail left intact: MX + SPF TXT (Netcup)
- `autoconfig` set to DNS-only (not proxied)

### Action required at the registrar (Netcup)

Zone status is still **pending**. Cloudflare DNS is not authoritative until nameservers are switched.

Set these nameservers at Netcup (Domain → Nameserver):

1. `clyde.ns.cloudflare.com`
2. `kami.ns.cloudflare.com`

Remove the old Netcup nameservers (`netcup.firstns.cc`, etc.). Propagation can take minutes to a few hours. After that, SSL on the custom domains should finish automatically.

## Build settings (Pages)

| Setting | Value |
| --- | --- |
| Production branch | `main` |
| Build command | `npm run build` |
| Build output directory | `dist` |
| Root directory | `/` |
| Node | ≥ 22.12 |

## Local deploy fallback

```sh
npx wrangler login
npm run pages:deploy
```
