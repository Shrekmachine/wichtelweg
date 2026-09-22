# Westhofener Wichtelweg

Website für den Westhofener Wichtelweg – **Astro** (statisch) und **Cloudflare** (Workers Static Assets).

- Geplante Domain: [westhofenerwichtel.de](https://westhofenerwichtel.de)
- Design-Vorgabe: `design/vorgabe-homepage-landingpage.jpg`
- Bildmaterial: `src/assets/`

## Voraussetzungen

- Node.js ≥ 22.12
- npm

## Lokal starten

```sh
npm install
npm run dev
```

Dev-Server: [http://localhost:4321](http://localhost:4321)

## Build & Deploy

```sh
npm run build
npm run preview
npm run deploy
```

Vor dem ersten Deploy: `npx wrangler login`.

Git-Connect in Cloudflare: Build `npm run build`, Assets aus `dist/` (siehe `wrangler.jsonc`). Domain `westhofenerwichtel.de` später als Custom Domain hinterlegen.

## Struktur

```text
/
├── design/                 # Team-Vorgaben (nicht für die Live-Seite gerendert)
├── public/
├── src/
│   ├── assets/             # Produktionsbilder
│   │   └── site/           # Hero- / Galerie-Zuschnitte
│   ├── components/         # Abschnitte der Startseite
│   ├── layouts/
│   └── pages/
├── astro.config.mjs
└── wrangler.jsonc
```

## Hinweise für Mitwirkende

Ton, Farben, Schriften und Navigation richten sich nach den Team-Grafiken. Texte kindgerecht und klar halten – siehe `AGENTS.md`.
