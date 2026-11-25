# AI video site v6

Static build: 29 Chinese pages + 11 English pages. Zero decorative images.

- Build: `python build/ai6/build_site.py --out build/ai6/site`
- QA: `python build/ai6/qa_site.py --site build/ai6/site`
- Responsive/interaction QA: `$env:AI_QA_BASE='http://127.0.0.1:8766'; python build/ai6/qa_responsive.py`
- Publish: copy this directory into `build/pages-sites/ai` (keep `.git`), then `build/push-site-fast.ps1 -Site ai`.
- Lab: `/lab/` (zh) and `/en/lab/` (en): 3 demo timelines + a 4-question tool picker. It is a recipe/timeline demo, not fake model footage.
- Templates: `/assets/templates/` (zh) and `/assets/templates/en/` (en), including `lab-demo-pack.md`.
- Legacy: `/legacy-map.json` maps 178 old URLs; `404.html` performs a client-side redirect. GitHub Pages cannot issue HTTP 301, so use a CDN 301 list if search equity matters.
