---
title: Dynamic Vibe-Matcher
---
### The Goal

Build an app that filters your own playlists down to match exactly how you feel right now. You pick a few of your existing Spotify playlists as a starting pool — say "Chill Acoustic" and "Gym Hype" — then describe your moment in plain English, like _"I'm stuck in traffic, it's raining, and I need something moody but with a steady driving beat."_ The app reads that and pulls together a fresh mix from your own music that fits the mood precisely.

The point is to end the summer with a real, working AI app that understands a vibe in plain words and turns it into the right music — the kind of tool you'd reach for whenever a generic playlist doesn't quite fit the moment.

### What It Should Do

- Let you select a few of your existing Spotify playlists as the source pool.
- Pull the tracks from those playlists along with their musical characteristics — tempo, energy, mood.
- Let you describe your current situation or mood in plain English.
- Translate that description into the kind of music it calls for — energy level, tempo range, overall feel.
- Filter your song pool down to the tracks that genuinely match.
- Present the fresh mix, with a simple chart showing the energy of the chosen songs so you can see the vibe at a glance.

The interesting twist: the AI is the bridge between feeling and numbers. "Moody but with a steady driving beat" isn't something you can type into a search box — the app reads that human description and turns it into concrete targets the code can actually filter on, so a loose mood becomes a precise, matching tracklist.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Spotipy** — to connect to Spotify, read your selected playlists, and pull each track's musical data.
- **Pandas** — to store the tracks and their characteristics in a table and filter them down to the matches.
- **An LLM API (OpenAI's gpt-4o-mini)** — the AI that reads your plain-English mood and turns it into target ranges for energy, tempo, and feel.
- **Streamlit** — turns your code into a clickable web app with playlist checkboxes, a mood box, the resulting tracklist, and an energy chart.

### Why It's Worth Doing

You'll get solid practice with **Pandas** — pulling live data into a table and filtering it on multiple conditions is core data work. You'll use a music **API** for real data, and the AI plays a clean, well-scoped role: using an **LLM to translate human language into structured filters** — taking a vague mood and turning it into precise values your code can act on. That "natural language in, structured data out" pattern is one of the most practical uses of GenAI, and building it here keeps the AI focused and the rest of the app simple. You'll also practice **data visualization** to make the result clear.

### How It Stays Cheap and Simple

The AI does one small, cheap job per request: it reads your mood text and returns target ranges, in a single short call. All the actual filtering and matching is done by plain Pandas on data you already pulled — no AI involved in the heavy lifting. That keeps both cost and complexity very low.

### One Thing to Check Early

The whole app depends on getting each song's musical data — tempo, energy, mood — so confirm early what your music source actually provides per track and how you'll access it, since this kind of audio data isn't always available to new apps. In week one, connect to Spotify, pull a real playlist, and verify exactly what per-track data you can retrieve before building the mood-matching logic on top of it. If that data isn't available, decide early on an alternative source so it doesn't block you later.