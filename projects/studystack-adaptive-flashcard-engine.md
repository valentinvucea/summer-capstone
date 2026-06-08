---
layout: project
title: StudyStack - Adaptive Flashcard Engine
---
### The Goal

Build a study app that turns your own notes into a smart testing tool that learns where you're weak. You upload your Markdown notes or lecture slides, and the app generates quiz questions from them — then it pays attention to how you do, bringing back the things you struggle with more often and easing off the ones you've mastered. Over time it focuses your studying exactly where it'll help most.

The point is to end the summer with a real, working AI app that makes studying genuinely more efficient — the kind of tool you and your classmates would actually use before an exam.

### What It Should Do

- Let you upload your own study material — Markdown notes or copied lecture slides.
- Generate quiz questions from that material, grounded in what you actually uploaded.
- Quiz you with clickable multiple-choice questions and check your answers.
- When you get something wrong, explain _why_ the right answer is right, so each miss is a learning moment.
- Track how you're doing on each topic — both accuracy and how confidently (and quickly) you answer.
- Use that performance to decide what to ask next, showing weak areas more often and mastered ones less.
- Show your progress, so you can see your mastery improving over time.

The interesting twist: the app doesn't just shuffle questions randomly — it keeps a running score for each piece of material and uses simple math to decide when something should reappear. Things you keep missing come back soon; things you've nailed fade out. That's the same "spaced repetition" idea behind serious study tools, built by you.

### What You'll Work With

- **Python** — the language you already know; everything is built in it.
- **NumPy** — the scoring engine: it keeps a performance score for each question and calculates which ones are due to reappear based on your accuracy and speed.
- **Pandas** — to organize the questions, your answer history, and the mastery analytics.
- **An LLM API (OpenAI or Claude)** — the AI that reads your notes and writes the multiple-choice questions and the explanations for wrong answers.
- **Gradio** — turns your code into a clickable web app with answer buttons and live progress display.

### Why It's Worth Doing

You'll get hands-on practice with **NumPy** for real numerical work — building an actual adaptive scoring system, not just toy array math. You'll use **Pandas** to track and analyze performance over time, and an **LLM for grounded content generation** — turning raw notes into good questions with helpful explanations. It blends a genuine algorithm (the adaptive scheduling) with GenAI, which makes it more substantial than a typical quiz app and gives you a real design decision to talk about: _how_ you decide when a question should come back.

### One Thing to Check Early

The heart of this project is the adaptive scoring logic, so think it through early — decide how a question's score goes up when answered correctly and down when missed, and how that translates into "show this again soon" versus "later." Sketch this rule on paper in week one with a few example scenarios before coding it, so the math is clear before you build the app around it.