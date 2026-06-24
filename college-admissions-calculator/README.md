# College Admissions Calculator

A standalone, self-contained tool inspired by admissions-consulting products
like John Morganelli's "BluePrint" (Ivy Tutors Network) — a former Cornell
admissions director's intake-questionnaire-to-personalized-report product.

It has two parts:

- **Chance Calculator** — estimates admission probability across a list of
  colleges from a student's GPA, test scores, course rigor, extracurricular
  strength, and hooks (legacy, first-gen, recruited athlete), sorting schools
  into Reach / Target / Likely / Safety.
- **BluePrint-style Report Generator** — takes an intake questionnaire
  (interests, background, goals, grade level) and produces a personalized
  report: an application theme, suggested majors, recommended activities,
  independent project ideas, summer program ideas, essay brainstorm prompts,
  a financial-aid overview, and a year-by-year timeline.

## Files

- `index.html` — a single-file static web app (HTML/CSS/JS, no build step,
  no backend, no dependencies). Open it directly in a browser, or publish it
  on any static host (GitHub Pages, Netlify, Vercel).
- `CollegeAdmissions.ipynb` — the same two tools as a Python notebook, for
  use in Colab/Jupyter.

## Publishing `index.html`

- **GitHub Pages:** repo Settings → Pages → Source: this branch, folder
  `/college-admissions-calculator` (or move `index.html` to repo root on a
  dedicated repo/branch) → save.
- **Netlify/Vercel:** drag `index.html` onto netlify.com/drop for an instant
  URL, or connect this repo for auto-deploys on push.

## Disclaimer

College stats (acceptance rate, SAT/ACT/GPA ranges) in `COLLEGE_DB` are
rough, illustrative approximations of recently published Common Data Set
figures — not live data. Refresh them before relying on this for real
decisions. This tool gives a statistical estimate, not a guarantee, and does
not use race as a factor, consistent with current U.S. admissions law.
