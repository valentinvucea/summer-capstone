---
layout: project
title: Ledger Lens - Private Transaction Categorizer & Reporter
---
### The Goal

Build an app that takes bank and card statements from different sources — each with its own messy format — and turns them into one clean, unified ledger. You upload your statements, and instead of manually sorting transactions into a spreadsheet, the app logs them, categorizes each one, and lets you generate a clear financial report showing where your money actually goes.

The point is to end the summer with a real, working AI app that does the tedious part of personal or small-business finance for you — built carefully, so your private financial details stay private.

### What It Should Do

- Let you upload transaction statements (CSV or similar) from different banks or cards, each with its own column layout.
- Normalize those different formats into one consistent structure.
- Remember transactions it has already logged, so re-uploading a statement doesn't create duplicates.
- Categorize each transaction in plain terms — groceries, transport, utilities, dining, income — even when the raw description is cryptic.
- Compute running balances, monthly totals, and spending by category.
- Generate a financial report you can read and download, with the breakdowns that matter.

The interesting twist: bank descriptions are cryptic ("SQ *COFFEE 0123", "AMZN MKTP US"). The AI reads these and understands what they actually are, so it can categorize them sensibly even when the text gives little away — something rigid keyword rules struggle with.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Pandas** — the core workhorse: normalizes the different statement formats, flags duplicates, and computes balances, totals, and monthly groupings.
- **SQLite** — a simple database to store every logged transaction, so the ledger persists and duplicates are caught.
- **An LLM API (OpenAI or Gemini)** — the AI that reads cryptic transaction descriptions and assigns each a sensible category.
- **Streamlit** — turns your code into a clickable web app where you upload statements, review the ledger, and view the report.
- _(Optional)_ a charting library like **Plotly** for visual spending breakdowns in the report.

### Keeping Your Financial Data Private

This is part of the project, not an afterthought — and it's a genuinely valuable thing to learn. Before building, spend time researching how to use an AI on sensitive data _without_ exposing the sensitive parts. The core principle to investigate and apply:

- **Send only what's needed.** To categorize a transaction, the AI needs the _description_ ("AMZN MKTP US") — it does **not** need the amount, your balance, or your account number. Strip those out before anything goes to the API, and join the category back to the full record locally afterward. The numbers never leave your machine.
- **Research the trade-offs** between sending data to a cloud API versus running a small local model (for example, via Ollama) so that _nothing_ leaves your computer at all. Understanding when each approach makes sense is a real engineering judgment worth forming.
- **Look into how API providers handle the data you send** — their data-retention and training policies — so you can make an informed choice and explain it.
- **Keep the local data secure:** the SQLite ledger holds real financial history, so research safe handling — keeping it off any shared repo, and treating the file as private.

The takeaway you'll be able to articulate: _"I designed it so amounts and account details are never transmitted — only the merchant text needed for categorization."_ That's exactly the kind of privacy-by-design thinking employers value.

### How It Stays Cheap and Simple

Categorizing every transaction one-by-one through the AI would get expensive and slow. Keep it efficient: categorize in **batches** (send many descriptions in a single request), and **cache results** — once "AMZN MKTP US" is known to be "Shopping," store that mapping so it's never sent to the AI again. Most months, only a handful of genuinely new descriptions ever need the AI at all. (This also _improves_ privacy — the less you send, the less is ever exposed.)

### Why It's Worth Doing

You'll get deep, practical experience with **Pandas** — cleaning and unifying messy real-world data from inconsistent sources is one of the most valuable day-to-day data skills there is. You'll practice **deduplication and change detection** (logging only what's new), use an **LLM for smart categorization** (turning vague text into meaningful labels), and learn **privacy-by-design** — how to get AI's benefits without handing over sensitive data. The result is a finance tool that's both technically real and genuinely trustworthy.

### One Thing to Check Early

Bank statements are sensitive data, so plan to work with your own real statements or realistic sample data — never anyone else's. Decide early how you'll handle different bank formats, since each export looks different; start with one bank's CSV in week one, get the full pipeline working end to end, then add a second format to prove the normalization holds up.