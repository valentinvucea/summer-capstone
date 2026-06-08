---
layout: project
title: Spotify-to-YouTube Bridge with AI Playlist Builder
---
### The Goal

Build an app that takes a Spotify playlist, finds the matching videos for every song on YouTube, and then goes a step further — using AI to understand the _mood_ of your playlist and suggest a fresh set of similar songs to extend it. You hand it a playlist, and you get back both a clickable YouTube version of every track and a smart "you might also like" list that fits the vibe, ready to play on YouTube.

The point is to end the summer with a real, working AI app that doesn't just move a playlist between services, but understands it well enough to grow it.

### What It Should Do

- Take a standard Spotify playlist as the starting point.
- Read each track — title, artist, and album.
- Search YouTube for the best matching video for each song and pick the most likely correct match.
- Present the results as a clean list of clickable YouTube links paired with the original songs.
- Analyze the playlist's overall mood and style, then generate a list of similar songs that fit it.
- Find those suggested songs on YouTube too, so the extended playlist is ready to play.
- Remember playlists it has already processed, so re-running one doesn't repeat the work.

The interesting twist: the AI reads the _character_ of your playlist — not just genres, but the mood and feel running through it — and suggests songs that genuinely belong, the way a thoughtful friend making you a mixtape would. It's the difference between "more songs in this genre" and "more songs that feel like this."

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Spotipy** — to connect to Spotify and read the playlist and each track's details.
- **google-api-python-client** — to search YouTube for matching and suggested songs.
- **Pandas** — to organize the tracks, search results, and chosen matches.
- **SQLite** — a simple database to store processed playlists so the work isn't repeated.
- **An LLM API (OpenAI or Gemini)** — the AI that analyzes the playlist's mood and generates the list of similar, fitting songs.
- **Streamlit** — turns your code into a clickable web app where you paste a playlist and get back both the YouTube links and the AI-suggested additions.

### Why It's Worth Doing

You'll learn to **work with real-world APIs** — connecting Spotify and YouTube and making two separate services work together, one of the most common and transferable skills in real software. You'll practice **matching messy data** (picking the right YouTube result), **organizing data with Pandas**, and **storing results in a database**. And the AI gives it a real GenAI core: using an **LLM to understand the feel of a collection and generate fitting recommendations** — a creative, reasoning-based task that plain logic genuinely can't do well, which is exactly where AI earns its place.

### How It Stays Cheap and Simple

The AI work happens once per playlist, not per song — you send the list of tracks in a single request to get the mood read and the suggestions back together, rather than calling the AI repeatedly. The heavier work of finding videos on YouTube stays plain and free of AI. This keeps both the cost and the complexity low.

### One Thing to Check Early

This app depends on two outside services, and YouTube's search API has a limited daily quota — so each song you look up costs against it, and the AI suggestions add more lookups. Check both services' API rules and quotas in week one, and confirm you can read a Spotify playlist, find a matching video for one song, and get a small AI suggestion list working before building everything else around that proven core.