---
title: SQL-Insight - Natural Language Data Explorer
---
### The Goal

Build an app that lets anyone ask a database questions in plain English. You connect it to a database — a store's inventory, a college course catalog, anything with tables — and instead of needing to know SQL, a user just types _"show me the top 5 most expensive items in stock"_ and gets back a live data table and a chart. The app shows the SQL it generated too, so the user can see exactly how their question became a query.

The point is to end the summer with a real, working AI app that turns plain questions into real answers from real data — the kind of tool a non-technical manager would actually want on their desk.

### What It Should Do

- Let you point it at a database and read its structure (which tables and columns exist).
- Let a user type a question in plain English, no SQL knowledge needed.
- Translate that question into a valid SQL query behind the scenes.
- Run the query safely and return the results as a clean data table.
- Show a matching chart when the data suits one (a ranking, a trend, a breakdown).
- Display the generated SQL alongside the results, so the user can see and trust how the answer was produced.

The interesting twist: the app reads the database's structure and hands it to the AI as context, so the questions and answers are grounded in _your_ actual tables and columns — it generates queries that really run, instead of guessing at field names.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **sqlite3** — a simple, built-in database to hold your data and run the queries against.
- **Pandas** — for cleaning up the raw records, fixing data types, and shaping the results for display and charting.
- **An LLM API (OpenAI's gpt-4o-mini)** — the AI that translates a plain-English question into a SQL query, using the database's structure as context.
- **Streamlit** — turns your code into a clickable web app with a split-screen view: the generated SQL on one side, the table and chart on the other.

### Why It's Worth Doing

You'll learn **text-to-SQL** — having an AI translate human questions into real database queries, one of the most practical and sought-after GenAI applications in business right now. You'll also get hands-on practice with **SQL and databases**, **data cleaning and shaping with Pandas**, and building a polished, interactive interface — all in a tool that makes data accessible to people who'd never write a query themselves.

### One Thing to Check Early

Letting an AI generate queries that run against your database means you need a few guardrails — only allow read-only queries, so a generated command can never change or delete data, and test early with messy questions to see how it behaves. Start with a small, clean sample database in week one so you can focus on getting the question-to-query step right before scaling up.