# CLAUDE.md

## Project Overview

Jekyll-based static website for Hori Lab (Computational Biophysics, University of Nottingham), hosted on GitHub Pages at hori-lab.github.io. Template adapted from Allan Lab (MIT License).

## Build & Serve Commands

```bash
# Setup (first time)
rbenv local 3.1.3
gem install bundler jekyll
bundle config set --local path 'vendor/bundle'
bundle install

# Local development server (http://localhost:4000/)
bundle exec jekyll serve --watch

# Build only (outputs to _site/)
bundle exec jekyll build
```

## Architecture

- **Pure Ruby/Jekyll stack** — no Node.js or npm. Dependencies: jekyll (>=3.6.3) and webrick.
- **Content is data-driven**: most page content comes from YAML files in `_data/` (members, publications, news, alumni), not from the Markdown pages themselves.
- **Pages** in `_pages/` select a layout and iterate over data files via Liquid templates.
- **Layouts** in `_layouts/` define page structure: `default.html` is the root wrapper; `homelay.html`, `gridlay.html`, `textlay.html` etc. are content-specific.
- **Custom plugin** `_plugins/markdown.rb` provides a Liquid tag for rendering Markdown includes with Liquid preprocessing.
- **CSS**: Bootstrap via SASS (`_sass/`) compiled through `css/main.scss`.

## Content Editing Patterns

- **Add a team member**: edit `_data/members.yml`, add photo to `images/teampic/`
- **Add a publication**: edit `_data/publist.yml`, add figure to `images/pubpic/`
- **Add news**: edit `_data/news.yml`
- **Move member to alumni**: move entry from `_data/members.yml` to `_data/alumni.yml`
- **Navigation**: defined in `_includes/header.html`

## Image Directories

Images are organized by purpose: `teampic/` (team), `pubpic/` (publications), `respic/` (research), `logopic/` (logos), `newspic/` (news), `slider7001400/` (homepage carousel), `photos/` (gallery).
