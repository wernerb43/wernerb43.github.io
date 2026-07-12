# CLAUDE.md

Guidance for working in this repository.

## What this is

A personal academic website built on the **Academic Pages** template (a fork of the
Minimal Mistakes Jekyll theme). It's a **Jekyll static site** deployed via **GitHub Pages**.
The repo name `wernerb43.github.io` means it publishes to `https://wernerb43.github.io`.

Owner: Blake Werner (Caltech). Note: the template's default placeholder content is still
in place — `_config.yml` still has `title: "Your Name / Site Title"`, `url:
https://academicpages.github.io`, and `repository: academicpages/academicpages.github.io`.
These should be personalized (see "Personalizing" below).

## Local environment setup

Setup is complete and verified — `bundle install` succeeded and the site builds and serves.
Ruby 3.0.2, gcc, make, `ruby-dev` headers, and node/npm are installed.

Bundler lives in the user gem dir, so **add it to PATH in each fresh shell**:

```bash
export PATH="$(ruby -e 'puts Gem.user_dir')/bin:$PATH"
```

The bundle installs into `vendor/bundle` (local path, already configured via
`bundle config set --local path 'vendor/bundle'`).

If you ever need to reinstall gems: `bundle install` (if it errors, delete `Gemfile.lock`
and retry). The `ruby-dev` system package is required to compile native gems (`nokogiri`,
`racc`) and is already installed; `nodejs`/`npm` are only needed for the JS asset build
scripts, not for serving the site.

## Build & serve

```bash
bundle exec jekyll serve -l -H localhost   # serves at localhost:4000, live-reload
```

Jekyll auto-rebuilds on changes to `*.md` / `*.html`. Changes to `_config.yml` require
restarting the server. Docker alternative: `docker compose up` (also serves on :4000).

## How the site is structured

Jekyll **collections** drive most content (see `collections:` in `_config.yml`). Each is a
folder of Markdown files with YAML front matter; the listing pages in `_pages/` render them:

| Collection      | Folder           | Listing page             | URL             |
|-----------------|------------------|--------------------------|-----------------|
| Publications    | `_publications/` | `_pages/publications.html` | `/publications/` |
| Talks           | `_talks/`        | `_pages/talks.html`        | `/talks/`        |
| Teaching        | `_teaching/`     | `_pages/teaching.html`     | `/teaching/`     |
| Portfolio       | `_portfolio/`    | `_pages/portfolio.html`    | `/portfolio/`    |
| Blog posts      | `_posts/`        | archive pages              | `/year-archive/` |

Other key directories:

- `_pages/` — standalone pages (`about.md` is the homepage, `cv.md`, `404.md`, archives).
- `_data/` — site data: `navigation.yml` (top menu), `authors.yml`, `ui-text.yml`
  (i18n strings), `cv.json` (JSON Resume data for the CV page), `comments/`.
- `_layouts/` — page templates (`single.html`, `default.html`, `talk.html`, `cv-layout.html`, …).
- `_includes/` — reusable Liquid partials (sidebar, author profile, head, footer, SEO, etc.).
- `_sass/` + `assets/` — styles and compiled assets. Theme colors set via `site_theme` in
  `_config.yml` (options: default, air, sunrise, mint, dirt, contrast).
- `files/` — static downloads (PDFs, etc.), served at `/files/...`.
- `images/` — images including author `avatar` (`profile.png`).

## Adding content

Create a Markdown file in the relevant collection folder with the required front matter
(copy the shape of an existing file in that folder). Front-matter fields differ per
collection — always model a new entry on an existing sibling.

## Helper scripts (optional, not needed for normal editing)

- `markdown_generator/` — Python/Jupyter scripts to generate publication and talk `.md`
  files from `.tsv`/`.csv`/BibTeX (`publications.py`, `talks.py`, `PubsFromBib.ipynb`, …).
- `scripts/update_cv_json.sh` + `scripts/cv_markdown_to_json.py` — regenerate
  `_data/cv.json` from `_pages/cv.md`.
- `talkmap.py` / `talkmap.ipynb` — geolocate talk locations and build a Leaflet cluster
  map (output in `talkmap/`). Uses `geopy`/`getorg`.

## CI / GitHub Actions (`.github/workflows/`)

- `scrape_talks.yml` — on push touching `_talks/**` or `talkmap.ipynb`, runs the talkmap
  notebook and commits the updated talk-location map back to the repo.
- `bad-pr.yml` — template-maintenance workflow that auto-closes template PRs (inherited from
  upstream; not relevant to this personal site).

Actual site deployment is GitHub Pages' built-in Jekyll build (no explicit deploy workflow).

## Personalizing (template still has placeholder values)

When customizing for Blake's site, update in `_config.yml`: `title`, `name`,
`description`, `url` → `https://wernerb43.github.io`, `repository` →
`wernerb43/wernerb43.github.io`, and the `author:` block (bio, email, social links).
Then replace placeholder content in `_pages/about.md`, `_pages/cv.md`, and the collection
folders. Edit `_data/navigation.yml` to control the top menu.
