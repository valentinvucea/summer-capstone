---
layout: project
title: Resume Match - Job Fit Analyzer
---
### The Goal

Build an app that works from the applicant's side of the job hunt. You load your resume once, then feed the app a job you're interested in — a link, a pasted page source, or just the description text — and it tells you how well you fit, where the gaps are, and how your resume should be adjusted to match. It even tells you whether the job is worth tailoring for in the first place, so you spend your effort where it actually pays off.

The point is to end the summer with a real, working AI app that acts like a personal job-application coach — the kind of tool someone would genuinely use throughout a stressful job search.

### What It Should Do

- Let you load your resume once and keep it as the fixed reference.
- Let you add a job description any way that's convenient — a URL, raw HTML or page source, or plain pasted text.
- Pull the real job requirements out of whatever you give it, ignoring the surrounding web-page clutter.
- Compare your resume against the job by meaning, and produce a clear fit assessment.
- Show the specific gaps — required skills or experience the job wants that your resume doesn't currently show.
- Recommend concrete resume adjustments: what to emphasize, rephrase, or add to better match this role.
- Give an honest verdict on whether the job is worth tailoring for, so you can prioritize the roles where you're a realistic fit.

The interesting twist: it matches by _meaning_, not keywords. If a posting wants "CI/CD experience" and your resume says "set up automated build and deployment pipelines," the app recognizes those as the same thing — so it credits what you've actually done and only flags gaps that are real.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **PyPDF2** (or **pdfplumber**) — to pull the text out of your resume PDF.
- **Requests + BeautifulSoup** — to fetch a job posting from a link or strip the requirements out of pasted HTML or page source.
- **Pandas** — to organize the comparison: which requirements are met, which are missing, laid out clearly.
- **An LLM API (OpenAI or Claude)** — the AI that reads the job, compares it to your resume by meaning, identifies the real gaps, and writes the tailoring advice and the worth-it verdict.
- **Streamlit** — turns your code into a clickable web app where your resume stays loaded and you drop in jobs to analyze.

### Why It's Worth Doing

You'll learn **semantic matching** — comparing two documents by meaning rather than exact words, the foundation of how modern search and **RAG** systems work. You'll practice **text extraction** from both messy PDFs and messy web pages (two constant real-world data tasks), **structured analysis with Pandas**, and using an **LLM to generate genuinely useful, specific critique** rather than generic advice. It solves a problem almost everyone faces, and it's a tool you'd actually keep using.

### One Thing to Check Early

Job postings come in wildly different shapes — a clean URL, a JavaScript-heavy page that hides the text, or a messy copy-paste. Decide early how much you'll support: getting clean text from a pasted description is easy and reliable, while scraping arbitrary live URLs is harder. Start in week one by supporting pasted text and one or two real job-site formats, get the full analysis working on those, then expand to trickier sources once the core is solid.