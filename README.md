# dkdan10.github.io

Personal website for Daniel Keinan. Live at https://dkdan10.github.io/.

Static HTML, CSS, and a small amount of vanilla JavaScript. No build step.

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
├── index.html
├── 404.html
├── assets/
│   ├── css/site.css
│   ├── js/site.js
│   └── img/                # headshot + project demo art (WebP)
├── resume/
│   └── Daniel_Keinan_Resume.pdf
├── og-image.png            # 1200×630 social preview
├── site.webmanifest
├── robots.txt
├── sitemap.xml
└── .nojekyll
```

## License

MIT — see [LICENSE](LICENSE).
