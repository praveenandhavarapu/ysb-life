# ISB Hyd Term 2 — my calendar

A focused, single-screen view of your ISB Hyderabad Term 2 schedule. Pick your section (A–F) and, optionally, a subject. Your classes are highlighted in amber; general sessions (workshops, CAS, ELP, makeup, exams) stay visible always. Hover any class to see venue and faculty.

Term 2 dates: 1 June 2026 → 12 July 2026.

## What's inside

- `index.html` — the whole app (HTML + CSS + JS, single file)
- `data.js` — the parsed schedule (6 weeks × 7 days × 5 slots, plus subject metadata)
- `netlify.toml` — minimal Netlify config
- `README.md` — this file

No build step. No dependencies. Pure static site.

## Deploy to Netlify

**Option 1 — Drag & drop (fastest)**
1. Go to https://app.netlify.com/drop
2. Drag the `isb-calendar` folder onto the page
3. You'll get a live URL in ~10 seconds (e.g. `https://wonderful-name-123.netlify.app`)
4. (Optional) Claim the site to a Netlify account to rename it

**Option 2 — Netlify CLI**
```bash
npm install -g netlify-cli
cd isb-calendar
netlify deploy --prod --dir .
```

**Option 3 — Git + Netlify**
1. Push the folder to a GitHub repo
2. In Netlify: "Add new site → Import an existing project" → pick the repo
3. Publish directory: `.` (already set in `netlify.toml`)

## Run locally

Just open `index.html` in a browser. Or:
```bash
cd isb-calendar
python3 -m http.server 8000
# then open http://localhost:8000
```

## How to read it

- **Amber cells** = your section's class in that slot. Subject code + name shown; hover for venue & faculty.
- **Green cells** = general sessions for everyone (CAS, Tutorial/Makeup, Student Workshops, ELP Prep, Area Elective Presentations).
- **Red cells** = exams (Mid Term, End Term).
- **Hatched cells** = nothing scheduled.

Slots stack inside one cell so each week fits on a single row. The whole term fits on one screen — no scrolling, no clutter.
