# CLAUDE.md

This file guides Claude Code when working in this repository.

## Overview

The Sala Company start page, live at https://go.sala.company. It is the portal that links every `*.sala.company` project (news, heat, flattery, games, AI tools, radio, video, etc.) as cards grouped into sections. It is a single static `index.html` with inline CSS and vanilla JavaScript. There are no dependencies, no build step, no package.json and no tests.

## Commands

There are no build, test or lint scripts. To preview locally, serve the directory with any static server, for example:

```
python3 -m http.server 8000
```

## Architecture

- `index.html`: the whole page: meta/SEO tags, JSON-LD structured data, styles, markup and script.
  - Cards are `<li class="item" data-added="YYYY-MM-DD" data-tags="...">` inside per-section lists (Live, Games, AI, Watch & listen, Create). Newsletter, store and About sit in footer cards outside the grid.
  - `data-added` drives behavior automatically: the **New** badge (30 days after the date) and the **Just added** row (cards added in the last 45 days). **Beta** badges are written by hand.
  - Search matches card titles, text and `data-tags`; `?q=<term>` in the URL pre-applies a search (also declared as the `WebSite` SearchAction in JSON-LD).
  - Counts (the "N free apps" pill, search placeholder, filter counts) are computed from the cards at runtime, so don't hard-code them.
  - The Sala News card fetches the top headline from `https://news.sala.company/breaking.json` and falls back to its static text if that fails.
  - Featured hero carousel: `.slide` links that work without JS; JS auto-advances every 6s, pausing on hover/focus/reduced motion.
  - Theme: follows the system; the theme button cycles Auto/Light/Dark and stores the choice in `localStorage` key `theme` (read early in `<head>` to avoid flashes).
- `img/<project>.jpg`: 640x400 card screenshots (`rates.jpg` is used only in structured data). `img/radio-icon.svg` and `img/video-icon.svg` are small inline title icons.
- `fonts/inter-latin.woff2`: self-hosted Inter (no Google Fonts calls).
- `favicon.svg`, `favicon-48.png`, `favicon.ico`, `apple-touch-icon.png`, `og-image.png` (1200x630 link preview).
- `robots.txt`, `sitemap.xml`.

## Adding or changing a project

The README's "Adding or changing a project" section is the checklist. In short:

1. Copy an existing `<li class="item">` into the right section; update link, title, one-line text, tags (max two visible), `data-tags`, screenshot and `data-added`.
2. Add `img/<project>.jpg` (640x400 JPEG).
3. Add the project to the JSON-LD `ItemList` in page order and update `numberOfItems`.
4. Update `dateModified` in the JSON-LD and `<lastmod>` in `sitemap.xml` to today.
5. Add a line to the README's "What's new" list (and the Projects table) if relevant.

## Deployment

- No GitHub Actions workflow: GitHub Pages serves the `main` branch directly. Pushing to `main` deploys live (about a minute).
- Custom domain `go.sala.company` via `CNAME`. There is no `.nojekyll` file.

## Conventions and gotchas

- Keep it a single file with no dependencies and no build step.
- The GoatCounter snippet at the end of `<body>` (endpoint `https://salacompany.goatcounter.com/count`, skipped on localhost, paths prefixed with `location.host` so all `*.sala.company` sites share one dashboard) must stay intact.
- Cards must stay crawlable and visible without JavaScript (carousel slides, card text, About/FAQ).
- One card size for everything: 16:10 screenshot, title, one line of text. The title link covers the whole card; extra links (e.g. Heat's market links) sit above it.
- Page is English (`lang="en"`), with light and dark themes; check both and narrow phone widths when changing styles.
