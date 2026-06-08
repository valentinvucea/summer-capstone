---
layout: project
title: Friend-Group Vibe Compromiser
---
### The Goal

Build an app that solves the eternal "what do we put on?" argument. A few friends each enter their favorite playlists, one of them describes what the group is doing — _"we're cooking dinner in the backyard and want something everyone likes, but keep it relaxing"_ — and the app blends everyone's tastes into one playlist that fits both the group and the moment. Nobody's music gets ignored, and it actually suits the occasion.

The point is to end the summer with a real, working AI app that takes a genuinely common social problem and solves it in a way that feels almost magical — the kind of thing friends would actually use at a get-together.

### What It Should Do

- Let two or three friends each enter their favorite playlists.
- Read each person's tracks and build a picture of their individual taste — genres, artists, styles.
- Find the common ground between them: shared genres, overlapping artists, similar styles.
- Let someone describe the situation in plain English — the activity, the mood, the vibe they want.
- Generate one blended playlist that balances everyone's taste _and_ fits the described setting.
- Show whose library inspired the result, so the compromise is transparent ("70% from Friend A, 30% from Friend B, based on your cooking prompt").

The interesting twist: the AI reads the _situation_, not just the music. The same group of friends needs something different for a backyard dinner than for a road trip or a workout — and the app uses the plain-English prompt to decide which tastes and styles should take the lead for _this_ specific moment, then picks the tracks that fit.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Spotipy** — to connect to Spotify and read each friend's playlist and track details.
- **Pandas** — to join the different friends' libraries together and find the overlap in genres, artists, and styles.
- **An LLM API (OpenAI or Claude)** — the AI that reads the situation prompt, decides which styles should take priority, and selects the best tracks from the shared pool.
- **Streamlit** — turns your code into a clickable web app with a side-by-side view of each friend's taste and the final blended playlist.

### Why It's Worth Doing

You'll practice **combining and comparing data with Pandas** — joining multiple people's libraries and finding meaningful overlap is real data-merging work. You'll use a music **API** to pull live data, and the AI gives it a strong GenAI core: using an **LLM to balance competing preferences against a described context** — a reasoning task that's genuinely hard with plain rules, since "what fits a relaxing backyard dinner for these three people" isn't something you can capture in a simple filter. It's a creative, social project that still rests on solid, transferable skills.

### How It Stays Cheap and Simple

The AI work happens once per request, not per song — you hand the LLM a summary of the shared track pool and the situation prompt in a single call, and it returns the chosen playlist. The data joining and taste-overlap work is all Pandas, which is free. That keeps both cost and complexity low.

### One Thing to Check Early

The blend is only as good as your read on each person's taste, so start there. In week one, connect to Spotify and confirm you can pull a couple of real playlists and summarize their genres and artists with Pandas, before building the blending and context logic on top. Get "describe two friends' tastes accurately" working first — everything else builds on that foundation.
