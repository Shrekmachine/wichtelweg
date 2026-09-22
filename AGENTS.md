# AGENTS.md

Shared instructions for AI coding tools working on this repo.

## Project

Public website for **Westhofener Wichtelweg** — a family- and child-friendly seasonal trail with fairy-tale “Wichtel” imagery.

- Domain (in progress): `westhofenerwichtel.de`
- Stack: Astro (`output: 'static'`), Cloudflare Pages (`wrangler.jsonc` / Pages Git builds → `dist/`)
- Standalone project. Design and wording come from the **Wichtelweg team**, not from other brands or sites.

## Design authority (binding)

1. **Primary visual brief:** `design/vorgabe-homepage-landingpage.jpg` — layout, navigation, section order, textures (parchment / wood), and overall tone.
2. **Supporting art:** files under `src/assets/` (hero, flyer, Gewinnspiel, gallery crops in `src/assets/site/`).
3. Match **tonality, type feel, formats, and colors** from those graphics: warm storybook / Märchen, forest greens, wood browns, parchment cream, lantern gold, gnome-hat red, soft sunset light.
4. Display type ≈ elegant handwritten script (site uses *Grand Hotel*); body / nav ≈ friendly rounded sans (*Nunito*).
5. Do **not** invent a competing visual system (no generic purple SaaS look, no harsh corporate marketing chrome).

## Language & audience (binding)

- Site language: **German** (`lang="de"`).
- Audience: families and children. Keep wording warm, clear, and märchenhaft.
- **No** ambiguous advertising slogans, suggestive wordplay, scare tactics, or language unsuitable for children.
- Prefer team copy from the graphics (dates, parking note, section titles). Mark unknowns as TBD rather than inventing legal text.

## Contact (from team)

- Email: `westhofenerwichtel@gmx.de`
- Instagram: `@westhofenerwichtel`
- Facebook: `https://www.facebook.com/profile.php?id=61580363623028`

## Commands

- Install: `npm install`
- Dev: `npm run dev`
- Build: `npm run build`
- Deploy: push to `main` (Pages Git) or `npm run pages:deploy` after `wrangler login`

## Conventions

- Keep the site static unless SSR is explicitly requested.
- No secrets in the repo.
- Prefer small Astro components per section (`Hero`, `SiteNav`, `Announcement`, …).
- New photos for the live site go in `src/assets/` (use `astro:assets`); design-only references stay in `design/`.
- Deployment notes live in `deployed.md`.
