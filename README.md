# BlueSkyLT.github.io

Personal GitHub Pages site used as an online career profile / extended CV, based on the
[personal-homepage-template](https://github.com/Yixin0313/personal-homepage-template) by Yixin Huang
(MIT licensed, see `LICENSE`). Content is bilingual (English / 中文).

## Structure

- `index.html` — page layout/markup.
- `contents/config.yml` — site title, header text, and copyright.
- `contents/*.md` — Markdown content for each section (home, awards, experience, publications, skills).
- `static/` — CSS, JS, and image assets.
- `cv.md` — source CV used to populate the site content.

## Local preview

Serve the repository root with any static file server, e.g.:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html` in a browser.
