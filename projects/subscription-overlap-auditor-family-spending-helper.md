---
layout: project
title: Subscription Overlap Auditor - Family Spending Helper
---
### The Goal

Build an app that finds the subscriptions a family is paying for twice. Across a household, people sign up for things separately — two Amazon Prime accounts, three music services, a streaming plan nobody remembers — and it's all buried in different bank and card statements. You upload those scattered statements, and the app pulls the charges together, recognizes which ones are really the same service, and shows the family exactly where they're doubling up and wasting money.

The point is to end the summer with a real, working AI app that solves a concrete household problem — the kind of tool that pays for itself the first time it finds a forgotten duplicate.

### What It Should Do

- Let family members upload or paste bank and card statement lines from different accounts.
- Clean up and merge those different sources into one combined view of the household's recurring charges.
- Recognize when differently-worded charges are actually the same service, and group them together.
- Highlight duplicates — the same subscription being paid for more than once across the family.
- Total up the wasted money, so the family sees the real monthly and annual cost of the overlap.
- Present it all as a clear table the family can act on.

The interesting twist: bank statements describe the same service in wildly different ways — "AMZN*MKTP", "Amazon Prime Video", and "PRIME MEMBERSHIP" all point to the same thing. A simple text match would treat those as three different charges. The AI recognizes they're one service, which is exactly what makes the duplicate-finding actually work — and it's something rigid keyword rules can't reliably do.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Pandas** — the workhorse: cleans the messy statement lines, merges different family members' data into one view, and computes the duplicate totals and wasted spend.
- **An LLM API (OpenAI's gpt-4o-mini)** — the AI that recognizes when differently-worded charges are the same service and groups them together.
- **Streamlit** — turns your code into a clickable web app where the family pastes or uploads statements and sees the results table.

### How It Stays Cheap and Private

A couple of design choices keep this efficient and safe. To save cost, you only need to identify the _unique_ charge descriptions, not every transaction — a household might have hundreds of line items but only a few dozen distinct merchants, so send only those unique descriptions to the AI and cache the results so a known merchant is never looked up twice. To protect privacy, the AI only needs the _description text_ to recognize a service — not the amounts, balances, or account numbers — so strip those out before anything is sent and keep the financial numbers entirely on your own machine.

### Why It's Worth Doing

You'll get strong, practical experience with **Pandas** — cleaning genuinely messy real-world data and merging multiple inconsistent sources is one of the most valuable everyday data skills. You'll learn **fuzzy entity matching with an LLM** — resolving "are these two messy strings the same thing?", a problem that shows up everywhere from finance to customer databases. And you'll practice **privacy-by-design**, sending the AI only what it needs. It's a focused, achievable project that solves a real problem and shows clear judgment about where AI belongs.

### One Thing to Check Early

The accuracy of the whole tool rests on correctly grouping the same service together, so test that early. In week one, gather a realistic set of messy merchant descriptions — your own, or made-up examples of how the same service shows up differently — and confirm the AI groups them correctly before building the rest of the app around it.