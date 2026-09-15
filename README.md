# BlueSkyLT.github.io

Personal GitHub Pages site used as an online career profile / extended CV, based on the
[personal-homepage-template](https://github.com/Yixin0313/personal-homepage-template) by Yixin Huang
(MIT licensed, see `LICENSE`). Content is bilingual (English / 中文).

The English and Chinese versions are served as separate static pages (not toggled on one
page), with a language switch in the top-right corner of the nav bar.

## Structure

- `index.html` — English page (`data-lang="en"`).
- `zh.html` — Chinese page (`data-lang="zh"`).
- `contents/config.en.yml` / `contents/config.zh.yml` — per-language site title, header text, and copyright.
- `contents/en/*.md` / `contents/zh/*.md` — per-language Markdown content for each section (home, education,
  experience, projects, awards, publications, skills).
- `contents/*_tag.svg` — institution logos shown next to institution names in the Education/Experience/Projects
  entries.
- `static/` — CSS, JS, and image assets.
- `cv.md` — source CV used to populate the site content.

## Local preview

Serve the repository root with any static file server, e.g.:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html` (English) or `http://localhost:8000/zh.html` (中文) in a browser.
