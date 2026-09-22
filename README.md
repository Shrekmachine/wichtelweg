# Westhofener Wichtelweg

Website für den Westhofener Wichtelweg – **Astro** (statisch) und **Cloudflare Pages**.

- Geplante Domain: [westhofenerwichtel.de](https://westhofenerwichtel.de)
- GitHub: [Shrekmachine/wichtelweg](https://github.com/Shrekmachine/wichtelweg)
- Pages: [wichtelweg.pages.dev](https://wichtelweg.pages.dev) (nach erstem Deploy)
- Deploy-Details: [`deployed.md`](./deployed.md)
- Design-Vorgabe: `design/vorgabe-homepage-landingpage.jpg`

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
```

Produktion läuft über **Cloudflare Pages** (Git-Connect auf `main`: Build `npm run build`, Output `dist`).

Manuell lokal (nach `npx wrangler login`):

```sh
npm run pages:deploy
```

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
├── deployed.md
└── wrangler.jsonc
```

## Hinweise für Mitwirkende

Ton, Farben, Schriften und Navigation richten sich nach den Team-Grafiken. Texte kindgerecht und klar halten – siehe `AGENTS.md`.
