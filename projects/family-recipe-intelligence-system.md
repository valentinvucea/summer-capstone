---
layout: project
title: Family Recipe Intelligence System
---
### The Goal

Build an app that turns a family's scattered recipes into one smart, searchable cookbook. You digitize the recipes — the handwritten cards, the ones in your head, the ones copied from relatives — and then instead of flipping through a box or texting your mom, you just ask the app: _"What can I cook with chicken, potatoes, and spinach?"_ It finds what fits, suggests swaps when you're missing something, and can even plan a week of meals.

The point is to end the summer with a real, working AI app that preserves something personal and makes it genuinely useful — the kind of tool a family would actually keep using at dinnertime.

### What It Should Do

- Let you add and store family recipes — ingredients, steps, and notes — in one place.
- Let you ask in plain English what you can make, based on the ingredients you have on hand.
- Suggest recipes that match, even when you don't have every ingredient.
- Offer sensible ingredient substitutions when something's missing or someone has a dietary restriction.
- Summarize a recipe's nutrition in plain terms, so the family knows roughly what they're eating.
- Help plan meals across a week, pulling from the family's own collection.

The interesting twist: it matches by _meaning_, not exact wording. Ask for "something light with chicken" and it understands the intent — it doesn't just look for the word "light," it reasons about which recipes actually fit, and works around what you do and don't have in the kitchen.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **SQLite** — a simple database to store the family's recipes, ingredients, and notes so the collection persists.
- **An LLM API (OpenAI or Gemini)** — the AI that understands plain-English requests, matches recipes to what you have, suggests substitutions, and writes the nutrition summaries.
- **Streamlit** — turns your code into a clickable web app where the family adds recipes and asks what to cook.

### Why It's Worth Doing

You'll get hands-on practice with **database design** — structuring recipes and ingredients so they're easy to store and query — and **data handling with Pandas** for organizing and filtering the collection. The heart of it is using an **LLM to reason over your own data**: understanding a casual request, matching it against the family's recipes, and giving practical, grounded answers. It's a warm, relatable project that still demonstrates real skills — turning a personal collection into an intelligent, interactive tool.

### One Thing to Check Early

The app is only as good as the recipes inside it, so decide early how recipes get entered and stored — what fields a recipe needs (ingredients, quantities, steps) and how you'll keep that consistent. In week one, add a handful of real recipes by hand and get the "what can I cook with…" question working on that small set before building out substitutions, nutrition, and meal planning.

