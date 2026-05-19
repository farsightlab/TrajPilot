# TrajPilot — Project Website

**How You Move Tells What You'll Do: Trajectory-Conditioned Egocentric Prediction**
SeJoon Jun, Hai Nguyen-Truong, Luigi Seminara, Lorenzo Torresani — Northeastern University

Built in the [Nerfies](https://nerfies.github.io/) / [EgoExo-WM](https://vision.cs.utexas.edu/projects/EgoExo-WM/) academic project-page style.

## Files
```
trajpilot-website/
├── index.html                    # the whole page (HTML + CSS + JS inline)
├── assets/
│   ├── teaser.jpg                # Figure 1 — basketball shot prediction
│   ├── cem_diagnostic.jpg        # Figure 2 — CEM in V-JEPA fails
│   ├── architecture.jpg          # Figure 3 — TrajPilot model
│   ├── scorer.jpg                # Figure 4 — gate-then-rank scorer
│   ├── results_planning.jpg      # Figure 5 — planning across horizons
│   ├── qualitative.jpg           # Figure 6 — 4 qualitative examples
│   ├── results_anticipation.jpg  # Figure 7 — anticipation results
│   └── poster.jpg                # full poster
└── README.md
```

## Preview locally
```bash
cd trajpilot-website
python3 -m http.server 8000
# open http://localhost:8000
```
Or just double-click `index.html`.

## Hosting
The site is fully static — drop the folder onto any static host:
- **GitHub Pages**: push to a repo's `gh-pages` branch or `docs/` folder, then enable Pages in repo settings.
- **Netlify / Vercel**: drag-and-drop deploy.
- **Northeastern web space**: upload via SFTP.

## Things to update once arXiv is up

Search `index.html` and replace these placeholders:

1. **PDF button** — change `href="#"` to your arXiv PDF link (e.g. `https://arxiv.org/pdf/2606.XXXXX`).
2. **arXiv button** — change `href="#"` to your arXiv abstract link (e.g. `https://arxiv.org/abs/2606.XXXXX`).
3. **Code button** — when code drops, remove `class="disabled"` and replace `href="#"` with the GitHub URL, then drop the "(soon)" text.
4. **Optionally**: link each author's name in `<p class="authors">` to their personal site or Google Scholar.
5. **BibTeX** — once the arXiv ID is assigned, update the BibTeX block to include `eprint = {arXiv:XXXX.YYYYY}` and `archivePrefix = {arXiv}`.

## Design notes
- Typography: Google Sans for headings/numbers, Noto Sans for body, Castoro for italic emphasis, Roboto Mono for code/emails — all loaded from Google Fonts.
- Color: white background, dark text, blue (#1d4ed8) accent for links and highlights, soft-blue callout for the TL;DR.
- Section structure mirrors EgoExo-WM: centered title at top, single-column content, justified prose, centered section headings, dark pill buttons.
- Two-column diagnostic layout for the "Why not V-JEPA" section.
- Featured stat card (TrajPilot Scorer 81.1%) is highlighted in the basketball section.
- Poster is clickable to open full-size.
- BibTeX has a one-click copy button.

## Accessibility
- All decorative SVG icons marked `aria-label`.
- Color contrast meets WCAG AA for body text.
- Responsive: layouts collapse cleanly on mobile (single-column, smaller stat-card grid, etc.).
