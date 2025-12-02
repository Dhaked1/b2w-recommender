🚀 Features

Simple, static, client-side prototype

User enters their video requirement → app returns the top 2–3 matching videos

Uses a small local JSON dataset (VIDEO_DB)

Lightweight tag scoring + keyword matching recommendation system

Clean UI with responsive layout

Includes integration placeholder for Google AI Studio to generate real recommendations

Zero build tools — works with plain HTML/CSS/JS

🧩 How It Works

The logic lives entirely in index.html (inline JS).

1. Local Video Dataset

A small list of example videos with fields:

title

description

category

tags

url

thumb

2. Fallback Recommender

The function fallbackRecommend() calculates a score for each item using:

Tag matches

Category matches

Generic keywords (“explainer”, “brand”, “demo”, etc.)

Duration tokens (15s/30s/60s/90s)

Light fuzzy match with title words

Top-scoring items are returned to the UI.

3. Optional AI Integration

A placeholder function getRecommendationsFromAI() is included.
You can replace it with real calls to:

Google AI Studio

Gemini API (via server-side proxy)

📁 Project Structure
root/
│── index.html        # Full UI + script + dataset
│── README.md         

Live Demo: https://dhaked1.github.io/b2w-recommender/
Any LLM that maps requirements → recommended videos

🚀 The prototype currently always falls back to local logic.
