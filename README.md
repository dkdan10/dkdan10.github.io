# dkdan10.github.io

Personal website for Daniel Keinan. Live at https://dkdan10.github.io/.

Static HTML, CSS, and a small amount of vanilla JavaScript. No build step, no framework,
no analytics, no external fonts or scripts. Dark by default; follows the OS with
`prefers-color-scheme: light`.

## Local development

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000/.

## Deployment

Pushes to `master` deploy automatically via GitHub Pages.

## Layout

```
.
├── index.html                      # home: hero, selected work, about, contact
├── 404.html
├── work/
│   ├── ailibi/index.html           # AiLibi project page
│   └── fadeaway/index.html         # FADEAWAY project page + the paper
├── papers/
│   ├── index.html                  # papers index
│   └── CONTESTED_Daniel_Keinan.pdf # the submitted paper; this path is linked from
│                                   #   the analytics_resolution README and the paper's
│                                   #   own bibliography, so it must not move
├── resume/
│   └── Daniel_Keinan_Resume.pdf    # keep the filename; old links point here
├── assets/
│   ├── css/site.css                # tokens on :root, light overrides in one media query
│   ├── js/site.js
│   └── img/
│       ├── headshot.webp
│       ├── ailibi-spectator.png    # AiLibi card + page image, also its OG image
│       ├── fadeaway-og.png         # FADEAWAY OG image (1200×630)
│       ├── fadeaway-card.webp      # lighter copy of the same frame for the card and page
│       ├── nbajam.webp             # earlier work, not displayed on the current site
│       └── squadup.webp            # earlier work, not displayed on the current site
├── og-image.png                    # 1200×630 social preview for the home page
├── site.webmanifest
├── robots.txt
├── sitemap.xml                     # lists every HTML page
└── .nojekyll
```

## Content rules

The project pages describe FADEAWAY and AiLibi in the terms their own hand-off notes allow.
The author will be asked about these in interviews, so the site must not oversell. Keep
every edit inside these lines:

- Do not say "every visual property is measured" (143 of 148 scalars are authored constants).
- Do not say "validated against the NBA" (the acceptance table is a self-measured regression fixture).
- Do not call the seeded-defect catalogue "mutation testing" (the defects corrupt data and documents, not code). Say "seeded defects" or "acceptance gate".
- Do not say "25 Hz across 30 seasons" (tracking exists for one 89-day window only).
- Do not say "all publicly available NBA data" (regular-season shot charts plus one tracking window).
- Do not describe FADEAWAY as "AI art", "generative", or "ML" (no model runs anywhere in the tree).
- Say "calibrated" the misalignment, never "corrected".
- Do not say "spatial precision changed" (precision is a constant 0.1 ft; what changes is whether a shot is placed at all).
- For AiLibi, do not imply the production code was hand-written, and do not call the AI-reviewer audits "independent human review".

Quick check before committing:

```sh
grep -ril "mutation testing\|generative\|validated against the NBA\|all publicly available" --include=*.html .
```

## License

MIT — see [LICENSE](LICENSE).
