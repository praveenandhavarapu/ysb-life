# ysb.life

Landing page + student tools for ISB Hyderabad PGP'27.

## Structure
- index.html        — landing page with search (routes to tools)
- netlify.toml      — publish config + clean-URL redirects + security headers
- term2calendar/    — Term 2 calendar (index.html + data.js)
- term3calendar/    — Term 3 calendar (index.html + data.js)
- term4calendar/    — Term 4 calendar (index.html + data.js)

## Adding a new term/tool
1. Create a folder e.g. term5calendar/ with index.html + data.js
2. Add a redirect block in netlify.toml
3. Add an entry to the PAGES array in index.html (set status:'live')
4. Commit + push — Netlify redeploys automatically.
