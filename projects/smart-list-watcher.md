---
layout: project
title: Smart List Watcher
---
### The Goal

Build an app that watches a website for you and tells you when something new shows up that matches what you're looking for. You pick a site — say, a used-car listing site — and describe what you want in plain English, like _"a reliable first car, nothing flashy, good value."_ Instead of refreshing the same search page over and over, you get notified only when a new listing genuinely fits.

The point is to end the summer with a real, working AI app that quietly watches for you and only speaks up when there's something worth seeing — not a throwaway demo.

### What It Should Do

- Let you describe what you're looking for in plain language, plus a few hard limits like price, year, and distance.
- Regularly check the target website and pull the current listings.
- Remember everything it has already seen, so it can tell new listings from ones you've already been shown.
- Drop anything that fails your hard limits before any AI is involved, keeping it fast and cheap.
- Match the remaining new listings against your description by _meaning_, not just keywords, and surface the closest fits.
- Notify you when something good shows up.

The interesting twist: because it matches by meaning, describing "a reliable commuter car" will surface the right listings even when they never use the word "reliable" — the app understands the idea, not just the words.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Requests + BeautifulSoup** (or **Playwright** for sites that load content with JavaScript) — the tools that fetch and read the website's pages.
- **Pandas** — for organizing listings and applying the hard filters.
- **SQLite** — a simple database to remember every listing it has already seen, so it knows what's new.
- **Embeddings + Chroma** — a vector database that stores the "meaning" of your criteria and each listing, so you can match by idea instead of exact words.
- **A notification method** — email, or a free service like a Telegram or Discord bot, to alert you when there's a match.
- **Streamlit** — turns your code into a clickable web app where you set your criteria and review matches.

### Why It's Worth Doing

You'll learn **web scraping** — reliably pulling structured data out of messy real-world web pages, a skill that applies far beyond cars to apartments, jobs, tickets, and more. You'll also practice **change detection** (telling new from old over time) and the heart of the project, **semantic matching with embeddings** — the foundation of **RAG (Retrieval-Augmented Generation)**, one of the most in-demand GenAI skills right now — all while building something you'd actually use.

### One Thing to Check Early

Websites have rules about scraping — check the site's `robots.txt` and terms of service before you start, and build in polite delays between requests so you're not overloading their servers. Picking a site that's friendly to this (or offers an API) makes the whole project smoother, so it's worth choosing your target site in week one.