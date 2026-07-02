# ysb.life

Landing page + student tools for ISB Hyderabad.

## Structure
- `index.html`     — landing page with command-bar search (routes to tools, or "not built yet")
- `netlify.toml`   — publish config, clean-URL redirects, security headers
- `term2calendar/` — Term 2 calendar (index.html + data.js)
- `term3calendar/` — Term 3 calendar (placeholder until timetable data is added)

## Deploy (first time — since ysb.life is empty)
1. Go to https://app.netlify.com/drop and drag this whole `ysb-life` folder in — OR push to GitHub and "Import an existing project".
2. In the site's **Domain management**, add custom domain `ysb.life` (and `www.ysb.life`).
3. Follow Netlify's DNS instructions (point nameservers to Netlify, or add the A/CNAME records at your registrar). SSL provisions automatically.

Once live:
- ysb.life               → landing
- ysb.life/term2calendar → Term 2
- ysb.life/term3calendar → Term 3 (placeholder for now)

## Adding a new tool later
1. Create a folder like `parking/` with its own `index.html`.
2. In `index.html` (landing), add an entry to the `PAGES` array with title/desc/path/icon/keywords. Set `status:"live"`.
That's it — search will find and route to it.

## When Term 3 data is ready
Replace `term3calendar/index.html` with the real calendar (same build as Term 2) and add `term3calendar/data.js`.
