---
layout: project
title: Smart Playlist Shifter - Activity Pacer
---
### The Goal

Build an app that reorders a playlist to match the shape of whatever you're doing. You describe your activity and how you want the energy to flow — _"I'm going on a 30-minute run: a slow 5-minute warmup, a high-energy peak in the middle, and a chill 5-minute cool-down"_ — and the app arranges your songs to follow that exact arc, so the music rises and falls with your effort.

The point is to end the summer with a real, working AI app that turns a flat list of songs into a soundtrack with intention — the kind of thing you'd genuinely use for a workout, a study session, or a focused stretch of work.

### What It Should Do

- Take a playlist and read each track's details — title, artist, and energy-related info from the music service.
- Let you describe your activity and its timeline in plain English, including how long it should run and where the high and low points should be.
- Work out how many songs each phase needs to fill its time slot.
- Sort and assign your tracks into phases — warmup, peak, cool-down, or whatever your description implies.
- Arrange the songs in order so the playlist follows the energy arc you asked for.
- Show the result visually, with a graph of the playlist's energy over time so you can see the peak and the wind-down.

The interesting twist: the AI acts as the scheduler. It reads your plain-English description, translates "high-energy peak in the middle" into an actual structure, and decides which of your songs belong in each phase — turning a vague human request into a precisely timed playlist.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **Spotipy** — to connect to Spotify and read the playlist and each track's energy details.
- **Pandas** — to index and organize the playlist data.
- **NumPy** — to handle the timing math: arranging tracks chronologically so each phase fills its requested number of minutes.
- **An LLM API (Gemini or OpenAI)** — the AI that reads your description, plans the phases, and tags each track as warmup, peak, or cool-down.
- **Gradio** — turns your code into a clickable web app where you type your timeline and see the new playlist and its energy graph.

### Why It's Worth Doing

You'll get real practice with **Pandas and NumPy together** — organizing data and doing genuine numerical work to fit songs to a timeline, which is more substantial than typical playlist apps. You'll use a music **API** for live data, and the AI provides a strong GenAI core: using an **LLM as a planner** that turns a loose human description into a concrete, structured schedule — a reasoning task plain rules handle poorly. You'll also practice **data visualization**, making the energy arc clear at a glance. It blends a real algorithm with AI, which gives you a meaty design decision to talk about.

### How It Stays Cheap and Simple

The AI is used once per request — you hand it the activity description and the list of tracks in a single call, and it returns the phase plan and tags. All the timing and arranging math is done with Pandas and NumPy, which is free. That keeps both cost and complexity low.

### One Thing to Check Early

The whole app depends on knowing each song's energy level, so confirm early what information the music service actually gives you for a track and how reliable it is. In week one, connect to Spotify, pull a real playlist, and check what energy or tempo data you can get per song — then build the phase-planning and arranging logic on top of what's genuinely available.