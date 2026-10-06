# Sala Company — Start Page

The Sala Company start page lives at [https://go.sala.company](https://go.sala.company) and serves as a central hub for all of Sala's browser-based projects. It features a searchable, filterable directory of games, tools, learning resources, and the online store — all running directly in your browser.

## What's New

- **Rizq** — A Brogue-inspired roguelike set in modern Kuwait (new game). Now with traders and banking, a ride home for your herd, smarter animals and a daily run
- **Heat** — Crypto heatmap with self-checking 🚀/😢 signals (new tool, beta)
- **Harmony** — AI-powered Suno prompt builder (new tool)
- **WebAI** — Private, in-browser AI (featured project)
- **3D Rubik's Cube** — Interactive 3D puzzle built with React and Three.js
- **iPod Classic Player** — Retro browser-based MP3 player
- **Learn category** — Educational content on how AI works
- **Search & category filtering** — Quickly find projects by name or category
- **Sala News** — Live news aggregator and topic heatmap ([news.sala.company](https://news.sala.company))

## Projects

### Featured

- **WebAI — Private Browser AI** ([webai.sala.company](https://webai.sala.company)) — [[repo]](https://github.com/jamalxcode/webllm-onefile): Run AI directly in your browser with complete privacy. No servers, no APIs, no outside connections.

### Games

- **AI Coded Breakout** ([breakout.sala.company](https://breakout.sala.company)) — [[repo]](https://github.com/jamalxcode/breakout-game-html): Classic arcade Breakout recreated with AI-generated code.
- **Galactic Defender** ([galacticdefender.sala.company](https://galacticdefender.sala.company)) — [[repo]](https://github.com/jamalxcode/galactic_defender): Galaga-inspired space shooter.
- **AI Coded Tetris** ([tetris.sala.company](https://tetris.sala.company)) — [[repo]](https://github.com/jamalxcode/tetris3): The classic puzzle game, reprogrammed using AI.
- **3D Rubik's Cube** ([cube.sala.company](https://cube.sala.company)) — [[repo]](https://github.com/jamalxcode/cube): Interactive 3D puzzle built with React and Three.js.
- **Rizq — A Kuwaiti Roguelike** ([rizq.sala.company](https://rizq.sala.company)) — [[repo]](https://github.com/jamalxcode/rizq): A Brogue-inspired roguelike set in modern Kuwait. Hustle from the Friday market to the deep desert, win over camels with dates, trade and bank at diwaniyas and camps, and dodge charging bull camels and howling wolf packs. Reach 100,000 KD net worth, then make it home. Includes a daily run where everyone gets the same map.

### Tools

- **Heat — Crypto & Forex Heatmaps** ([heat.sala.company](https://heat.sala.company), [forex](https://heat.sala.company/forex/)) — [[repo]](https://github.com/jamalxcode/heat): Top 100 coins (stablecoins excluded) colored by price move, with RSI, the 50/200-day trend, point & figure, 30-day momentum and suggested stop-losses on every tile. A daily scorecard checks the signals against the next moves, and a weekly tuner adjusts them. Prices refresh every 10 minutes. A forex page shows 48 currencies against the US dollar from official ECB rates. Beta, not financial advice.
- **Harmony** ([harmony.sala.company](https://harmony.sala.company)): Harmony is your local AI co-producer: feed it a rough concept and it runs a rapid draft-then-refine loop—spitting out tuned titles, genre tags, lyric skeletons, and clean exclude lists—so you hit Suno's Custom Mode with production-grade prompts in seconds. Zero accounts, zero cloud, pure creative momentum.
- **AI Tools Collection** ([ai.sala.company](https://ai.sala.company)) — [[repo]](https://github.com/jamalxcode/ai-sala-company): A curated collection of AI websites and browser experiments.
- **Sala News** ([news.sala.company](https://news.sala.company)) — Live news aggregator and topic heatmap. Track trending headlines and visualize what the world is talking about — all in your browser.
- **Secret Emoji Messenger** ([secret.sala.company](https://secret.sala.company)) — [[repo]](https://github.com/jamalxcode/hidetext): Hide secret messages inside emojis using Unicode steganography. Encode a message into any emoji and share it anywhere — only those who know the trick can decode it.
- **iPod Classic Player** ([music.sala.company](https://music.sala.company)) — [[repo]](https://github.com/jamalxcode/retro-tunes-player): A browser-based retro MP3 player styled after the original iPod Classic.

### Learn

- **How AI Works** ([understand.sala.company](https://understand.sala.company)): Educational presentation covering neural networks, language models, and how modern AI systems are built. Authored in [Gamma](https://gamma.app/).
- **Early Wake Up Club** ([mutawa.substack.com](https://mutawa.substack.com)): Newsletter covering technology, business, and AI — from the AI chip race to crypto trends and big tech moves. Published on Substack.
  - [The Trillion Dollar Club](https://mutawa.substack.com/p/the-trillion-dollar-club) — Jan 2026
  - [From Mining Bitcoin to Powering ChatGPT: The Great Crypto Pivot](https://mutawa.substack.com/p/from-mining-bitcoin-to-powering-chatgpt) — Dec 2025
  - [The Great AI Chip War: How China and America Are Fighting for the Future](https://mutawa.substack.com/p/the-great-ai-chip-war-how-china-and) — Nov 2025

### Shop

- **Online Store** ([www.sala.company](https://www.sala.company)): Official Sala Company merchandise and digital products with secure checkout.

## Features

- **In-browser search** — Filter the project directory by name in real time. A link like `go.sala.company/?q=heat` opens with that search already applied.
- **Category tabs** — Browse by All, Games, Tools, Learn, or Shop.
- **No installs required** — Every project runs entirely in the browser.

## Writing

**[Early Wake Up Club](https://mutawa.substack.com/)** — Newsletter covering technology, business, and AI. Topics include crypto, the AI chip race, and big tech.

## Tech

- Pure HTML/CSS/JS — no build step, no dependencies.
- Hosted via GitHub Pages with a custom CNAME (`go.sala.company`).

## Search engines and link previews

- **Title and description** written for search results, within Google's display limits.
- **Canonical URL** `https://go.sala.company/`, plus Google and Bing site-verification tags.
- **Link previews** (Open Graph and X): `og-image.png`, a 1200×630 screenshot of this page.
- **Icons:** `favicon.svg`, `favicon-48.png` and `favicon.ico` for browsers and search results, and `apple-touch-icon.png` (180×180) for phone home screens.
- **Structured data** (JSON-LD): the `WebSite` with its search (`?q=`, which really works), the `Organization`, and an `ItemList` of every project on the page. When a card is added or removed, update the `ItemList` too.
- **`robots.txt`** and **`sitemap.xml`**. Update the sitemap's `lastmod` date when the page changes.
