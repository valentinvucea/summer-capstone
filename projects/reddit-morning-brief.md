---
layout: project
title: Reddit Morning Brief
---
### The Goal

Build an app that reads Reddit for you. You pick the subreddits you care about, and instead of scrolling endlessly to find the few posts that matter, you get a clean daily summary — plus the ability to ask questions about what's been happening, like _"what's the mood in r/programming this week?"_

The point is to end the summer with a real, working AI app that's genuinely useful to you — not a throwaway demo.

### What It Should Do

- Let you choose a list of subreddits to follow.
- Collect the top posts and discussions from those subreddits and save them.
- Show you a short summary of what the important threads are actually about.
- Let you ask questions in plain English and get answers based on the real posts it saved — with those posts shown as sources, so it's grounded in actual Reddit content rather than made up.

The interesting twist: because it can search by _meaning_ and not just keywords, asking "what's everyone frustrated about?" will surface a post that says "this update is infuriating" — even though it never uses the word "frustrated."

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **PRAW** — the tool that pulls posts and comments from Reddit.
- **Pandas** — for organizing and ranking the posts.
- **SQLite** — a simple database to store the real post content.
- **Chroma** — a vector database that stores the "meaning" of each post so you can search by idea, not just words.
- **An LLM API (OpenAI or Claude)** — the AI that writes the summaries and answers your questions.
- **Streamlit** — turns your code into a clickable web app you can share with a link.

### Why It's Worth Doing

You'll learn **RAG (Retrieval-Augmented Generation)** — the pattern of answering questions using your own saved data — which is one of the most in-demand GenAI skills right now. And you'll get real, hands-on practice with databases, embeddings, and AI APIs, all while building something you'd actually use.