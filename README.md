# Social Media & Attention: An Observation Tool

**DIFH3017 Digital Humanities and Health · Spring 2026 · Website Project**

---

## What This Is

A public health communication website targeting Hong Kong university students. The topic is the relationship between social media use and attention difficulties.

It does **not**:
- Diagnose
- Provide treatment advice
- Suggest that "quitting your phone will cure attention problems"

It **does**:
- Let readers record their usage and focus patterns in one minute, with no score
- Present three verifiable local numbers, each with its limits
- Provide verified support channels in Hong Kong

**This website is not a medical tool.** If you or someone around you is in immediate danger, call 999 or go to the nearest emergency department.

---

## Website Structure

| Page | File | Purpose |
|---|---|---|
| Observation Tool | `index.html` | Landing page, one-minute observation form, no data stored |
| What We Know | `evidence.html` | Three claims + one chart, each with denominator, source, and limits |
| One Person's Day | `story.html` | Five-scene fictional story, explicitly labelled as fiction, no promise of recovery |
| Find Help | `support.html` | Hong Kong support channels, urgent vs non-urgent |
| Method & AI | `method.html` | Source table, AI use log, known limitations |

---

## Five-Line Brief

| Element | Content |
|---|---|
| **Audience** | Hong Kong university students (18–22), who feel their attention has worsened but are unsure if social media is related |
| **Objective** | Help readers understand that usage time and attention difficulties are **correlated**, but correlation is not causation; provide one actionable next step |
| **Core Message** | 93.4% of Hong Kong youth use social media, averaging 4.1 hours/day; attention difficulties are real, but "scrolling causes ADHD" is an oversimplification |
| **Boundary** | No diagnosis, no treatment advice, no implied causation |
| **Next Step** | Provide verified Hong Kong support resources and a self-observation tool |

---

## Tech Stack

| Layer | Technology | Notes |
|---|---|---|
| Frontend | Plain HTML + Bootstrap 5 | No build step; open directly in browser |
| Charts | ApexCharts 3.54 (CDN) | One chart, with `aria-label` and text summary |
| Interaction | Vanilla JavaScript | Observation form, story scene navigation; no external dependencies |
| Deployment | GitHub Pages (static) | No backend, no database, no environment variables |

**Why no backend:** The site only presents verified public data; it does not need to store reader input. The observation form's answers never leave the browser.

---

## Run Locally

No installation needed. Open `index.html` directly in a browser.

If you prefer a local server (e.g. to test relative paths):

```bash
# Python 3
python -m http.server 8000

# Or Node.js
npx serve .