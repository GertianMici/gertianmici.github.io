# gertianmici.github.io

The published build of the owner's personal site, served by GitHub Pages at gertianmici.com (`CNAME`). It holds the portfolio page, a CV PDF, a set of small browser games, and the privacy, support and terms pages for the Helkost and Osrever apps. Visitors use it in a browser.

This file is what an agent needs to work on this repo. It holds facts about this repo only; my working agreement holds the rules for every repo.

## Layout

- Everything here is output of the separate `Portofolio` repo (Vite): `index.html` and `assets/` are its build, and the other files below are copied from its `public/` folder. Edit them there, not here.
- Standalone pages at the root: `car-race.html`, `chess-3d.html`, `falling-sand.html`, `horse-race.html`, `idle-metropolis.html`, `llama-race.html`, `pac-girl.html`, `ship-it.html`, `tower-stack.html`. `three/` holds a vendored `three.module.js` and addons that five of them load.
- `helkost/` (index, privacy, support, terms) and `osrever/` (index, privacy, support) are the app pages.
- Root files: `CNAME`, `.nojekyll`, `robots.txt`, `manifest.json`, icons, `og-image.png`, `GertianMici_CV.pdf`.

## Build, test and run

No build, no tests and no manifest in this repo. To look at it, serve the folder with any static server, for example `python3 -m http.server`. The `verify` skill does not cover it.

## Deploy

GitHub Pages serves this repo. A push to main in the `Portofolio` repo runs `.github/workflows/deploy.yml` there, which builds and pushes to the `main` branch here as `deploy: GertianMici/Portofolio@<sha>` commits. Deploying is ask-first.

## Data sources

None.

## Conventions

- The `index.html` meta tags set a Content Security Policy of `default-src 'self'` with inline scripts and styles allowed, and no external hosts. Pages should stay self-contained.
- A change made directly in this repo is replaced by the next Portofolio deploy, so changes belong in `Portofolio`.

## Known traps

None recorded yet.
