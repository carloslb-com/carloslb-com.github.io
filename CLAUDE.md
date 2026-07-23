# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Serve locally with live reload
bundle exec jekyll serve --host 0.0.0.0 --livereload

# Build for production
bundle exec jekyll build

# Install dependencies
bundle install
```

The site runs at `http://192.168.2.152:4000` by default.

## Architecture

This is a **Jekyll 4** static site for the personal/professional profile of Carlos León Bolaños. It uses **jekyll-polyglot** for bilingual support (Spanish `es` as default, English `en`).

### Profile structure

The site has three distinct professional profiles, each with its own layout and stylesheet:

| Profile | Page | Layout | Sass |
|---|---|---|---|
| IT / Telecom | `profiles/it.html` | `_layouts/it.html` | `_sass/_it.scss` |
| Administration / HR | `profiles/management.html` | `_layouts/management.html` | `_sass/_management.scss` |
| Teaching | `profiles/teaching.html` | `_layouts/teaching.html` | `_sass/_teaching.scss` |

All three layouts inherit from `_layouts/default.html`, which composes `_includes/head.html`, `header.html`, `nav.html`, and `footer.html`.

### Styles

`assets/css/main.scss` is the single stylesheet entry point. It imports from `_sass/`: `_base.scss` for shared styles, plus one file per profile.

### Diagrams

Mermaid.js is bundled locally at `assets/js/mermaid.esm.min.mjs`. To enable diagrams on a page, add `mermaid: true` to its front matter — the `default` layout conditionally includes `_includes/mermaid.html`.

### i18n

jekyll-polyglot handles language routing. Assets, JS, CSS, and images are excluded from localization (`exclude_from_localization` in `_config.yml`). Use `{{ site.active_lang }}` in templates and provide translated front matter per language as needed.
