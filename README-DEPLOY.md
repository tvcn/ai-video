# AI video site v6

Static build: 29 Chinese pages + 14 English pages. Six captioned official-page screenshots and two free commercial-use real reference clips on the tool hub; no decorative images.

- Build: `python generator/ai6/build_site.py --out generator/ai6/site`
- QA: `python generator/ai6/qa_site.py --site generator/ai6/site`
- Publish: `node generator/build-all.mjs`, then `generator/publish.ps1 -Site ai`.
- Templates: `/assets/templates/` (zh) and `/assets/templates/en/` (en).
- Legacy: `/legacy-map.json` maps 178 old URLs; `404.html` performs a client-side redirect. GitHub Pages cannot issue HTTP 301, so use a CDN 301 list if search equity matters.
