# Sala Company — Start Page

The Sala Company start page lives at [https://go.sala.company](https://go.sala.company) and serves as a central hub for all of Sala's browser-based projects: a searchable, filterable directory of live data, games, AI tools and more, all running directly in your browser.

## What's New

The page has a matching **What's new** strip under the search bar; update both together, and keep it to the last month or so.

- **Sala News** — Out of beta: a new look, about 95 live sources, breaking-news alerts and videos from 29 news channels ([news.sala.company](https://news.sala.company))
- **Heat Rates** — Official government bond yield curves for 14 markets, with real yields and ten years of history ([heat.sala.company/rates/](https://heat.sala.company/rates/))
- **Rizq** — A Brogue-inspired roguelike set in modern Kuwait. Now with traders and banking, a pickup truck home for your herd, smarter animals and a daily run
- **New design** — Projects grouped by what they are, a screenshot on every card, light and dark themes, and the most active projects first

## Projects

The page shows them in this order, most active first.

### Live data

- **Sala News — The World Now** ([news.sala.company](https://news.sala.company)) — [[repo]](https://github.com/jamalxcode/the-world-now): Live world headlines from about 95 news, OSINT and disaster sources, refreshed every few minutes, with breaking-news alerts, videos from 29 news channels and search links under every headline.
- **Heat — Market Heatmaps** ([heat.sala.company](https://heat.sala.company), [forex](https://heat.sala.company/forex/), [metals](https://heat.sala.company/metals/), [energy](https://heat.sala.company/energy/), [rates](https://heat.sala.company/rates/)) — [[repo]](https://github.com/jamalxcode/heat): Top 100 coins (stablecoins excluded) colored by price move, with RSI, the 50/200-day trend, point & figure, 30-day momentum and suggested stop-losses on every tile. A daily scorecard checks the signals against the next moves, and a weekly tuner adjusts them. Prices refresh every 10 minutes. A forex page shows 48 currencies against the US dollar from official ECB rates; metals and energy pages cover gold, silver, platinum, palladium, crude, diesel, gasoline and natural gas; and a rates page shows official government bond yield curves for 14 markets (normal, flat or inverted). Beta, not financial advice.

### Games

- **Rizq — A Kuwaiti Roguelike** ([rizq.sala.company](https://rizq.sala.company)) — [[repo]](https://github.com/jamalxcode/rizq): A Brogue-inspired roguelike set in modern Kuwait. Hustle from the Friday market to the deep desert, win over camels with dates, trade and bank at diwaniyas and camps, and dodge charging bull camels and howling wolf packs. Reach 100,000 KD net worth, then make it home. Includes a daily run where everyone gets the same map. Shown as the large featured card.
- **3D Rubik's Cube** ([cube.sala.company](https://cube.sala.company)) — [[repo]](https://github.com/jamalxcode/cube): Interactive 3D puzzle built with React and Three.js.
- **Vibe Coded Breakout** ([breakout.sala.company](https://breakout.sala.company)) — [[repo]](https://github.com/jamalxcode/breakout-game-html): Classic arcade Breakout, vibe coded from the start.
- **Galactic Defender** ([galacticdefender.sala.company](https://galacticdefender.sala.company)) — [[repo]](https://github.com/jamalxcode/galactic_defender): Galaga-inspired space shooter.
- **Vibe Coded Tetris** ([tetris.sala.company](https://tetris.sala.company)) — [[repo]](https://github.com/jamalxcode/tetris3): The classic puzzle game, vibe coded from the start.

### AI

- **WebAI — Private Browser AI Chat** ([webai.sala.company](https://webai.sala.company)) — [[repo]](https://github.com/jamalxcode/webllm-onefile): Chat with open AI models (Llama, Phi, Mistral, Qwen, Gemma, TinyLlama) running entirely on your device through WebGPU. No servers, no API keys, no account. Needs a WebGPU browser such as recent Chrome or Edge.
- **Harmony** ([harmony.sala.company](https://harmony.sala.company)): A local AI co-producer for Suno: turn a rough song idea into titles, genre tags, lyric skeletons and exclude lists for Custom Mode.
- **How AI Works** ([understand.sala.company](https://understand.sala.company)): Educational presentation covering neural networks, language models, and how modern AI systems are built. Authored in [Gamma](https://gamma.app/).
- **AI Tools Collection** ([ai.sala.company](https://ai.sala.company)) — [[repo]](https://github.com/jamalxcode/ai-sala-company): A curated directory of AI websites and tools.

### More

- **Secret Emoji Messenger** ([secret.sala.company](https://secret.sala.company)) — [[repo]](https://github.com/jamalxcode/hidetext): Hide secret messages inside emojis using Unicode steganography.
- **iPod Classic Player** ([music.sala.company](https://music.sala.company)) — [[repo]](https://github.com/jamalxcode/retro-tunes-player): A browser-based retro MP3 player styled after the original iPod Classic.
- **Early Wake Up Club** ([mutawa.substack.com](https://mutawa.substack.com)): Newsletter covering technology, business, and AI — from the AI chip race to crypto trends and big tech moves. Published on Substack.
  - [The Trillion Dollar Club](https://mutawa.substack.com/p/the-trillion-dollar-club) — Jan 2026
  - [From Mining Bitcoin to Powering ChatGPT: The Great Crypto Pivot](https://mutawa.substack.com/p/from-mining-bitcoin-to-powering-chatgpt) — Dec 2025
  - [The Great AI Chip War: How China and America Are Fighting for the Future](https://mutawa.substack.com/p/the-great-ai-chip-war-how-china-and) — Nov 2025
- **Sala Company Store** ([www.sala.company](https://www.sala.company)): Ebooks — sci-fi thrillers such as *The Boy Who Defied the Machine*, AI guides, business and children's books.

## How the page works

- **Sections:** Live data, Games, AI and More, each with an `<h2>`; every card title is an `<h3>`.
- **Search and filters:** the search box matches card titles, text and `data-tags`; the filter buttons (`aria-pressed`) show one section. Empty sections hide, and the What's new strip hides while you search or filter. A link like `go.sala.company/?q=heat` opens with that search already applied.
- **Cards:** the title link covers the whole card, so one click anywhere opens the project; extra links (Heat's markets, the newsletter articles) sit above it and stay clickable. The "Play … →" button is part of that same link.
- **Badges:** **New** for about 30 days after a project launches, **Updated** for a big recent change, **Beta** while a project is still a work in progress. Take them off when they go stale.
- **Featured card:** add `feature` to an item's class to give it a 2×2 block on wider screens (Rizq today).
- **Theme:** light and dark follow the system; the ◐ button cycles Auto → Light → Dark and remembers the choice in this browser.
- **Screenshots:** `img/<project>.jpg`, 640×400 JPEGs (Rizq's is 720×720 for the featured block), taken with headless Edge at 1280×800 and cropped. Retake them when a project's look changes.
- **Font:** Inter (`fonts/inter-latin.woff2`), hosted here so the page makes no calls to Google, as on heat and news.

## Tech

- Pure HTML/CSS/JS — no build step, no dependencies.
- Hosted via GitHub Pages with a custom CNAME (`go.sala.company`).

## Search engines and link previews

- **Title and description** written for search results, within Google's display limits.
- **Canonical URL** `https://go.sala.company/`, plus Google and Bing site-verification tags.
- **Link previews** (Open Graph and X): `og-image.png`, a 1200×630 screenshot of this page.
- **Icons:** the "S" mark in `favicon.svg`, with `favicon-48.png` and `favicon.ico` for browsers and search results, and `apple-touch-icon.png` (180×180, square; phones round the corners) for home screens.
- **Structured data** (JSON-LD): the `WebSite` with its search (`?q=`, which really works), the `WebPage` (with `dateModified`), the `Organization`, and an `ItemList` of every project in page order, each typed as a free `WebApplication`, `VideoGame` or `WebSite` with its own description and screenshot. When a card is added, removed or moved, update the `ItemList` (and `numberOfItems`) too.
- **Crawlable text:** the What's new strip and an About / FAQ section give search engines plain text about each project. Cards are visible without JavaScript.
- **`robots.txt`** and **`sitemap.xml`**. Update the sitemap's `lastmod` date when the page changes.
