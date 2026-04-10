# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Academic homepage for Haoxiang Wang (Peking University), built on the **Academic Pages** template (fork of Minimal Mistakes Jekyll theme). Deployed to GitHub Pages at https://markgodrick.github.io.

## Build & Development Commands

```bash
# Install Ruby dependencies
bundle install

# Local development server (auto-reloads on changes, EXCEPT _config.yml)
bundle exec jekyll serve -l -H localhost

# Production build (outputs to _site/)
bundle exec jekyll build
JEKYLL_ENV=production bundle exec jekyll build

# JavaScript assets (only needed if editing JS in assets/js/)
npm install
npm run build:js        # Minify JS bundle
npm run watch:js        # Watch and rebuild on changes
```

**Important:** Changes to `_config.yml` require restarting `jekyll serve`.

## Deployment

Pushes to `master` trigger the GitHub Actions workflow (`.github/workflows/jekyll.yml`) which builds with Ruby 3.1 and deploys to GitHub Pages. There is no separate staging environment.

## Architecture

### Content Collections

The site uses four Jekyll collections (configured in `_config.yml`), each with its own directory, layout defaults, and archive page:

| Collection | Directory | Layout | Archive Page |
|---|---|---|---|
| Publications | `_publications/` | `single` | `_pages/publications.html` |
| Talks | `_talks/` | `talk` | `_pages/talks.html` |
| Teaching | `_teaching/` | `single` | `_pages/teaching.html` |
| Portfolio | `_portfolio/` | `single` | `_pages/portfolio.html` |

Blog posts live in `_posts/` with standard Jekyll conventions.

### Content File Naming

All content files follow `YYYY-MM-DD-title.md`. Front matter varies by collection but commonly includes: `title`, `date`, `permalink`, `venue`, `excerpt`, `paperurl`, `citation`.

Publications use a `category` field (`books`, `manuscripts`, `conferences`) that controls grouping on the publications archive page.

### Navigation

Site navigation is defined in `_data/navigation.yml`. Currently active: Publications, Blog Posts, CV. Other sections (Talks, Teaching, Portfolio) are commented out.

### Template Hierarchy

- `_layouts/default.html` - base layout (masthead + footer + scripts)
- `_layouts/single.html` - pages/posts with metadata and sharing
- `_layouts/talk.html` - talks with venue/date formatting
- `_layouts/archive.html` - archive listing pages
- `_includes/` - reusable components (author-profile, masthead, footer, etc.)

### Styling

SCSS lives in `_sass/`, compiled via `assets/css/main.scss`. The site uses Susy grid system and Breakpoint for responsive layout. Variables are in `_sass/_variables.scss`.

### Markdown Generators

`markdown_generator/` contains Python scripts and Jupyter notebooks that convert TSV data files into collection markdown files. Useful for bulk-creating publication or talk entries from spreadsheet data.

### Key Configuration

`_config.yml` controls: site metadata, author profile/social links, collection definitions, default front matter, plugin list, and publication categories. Author sidebar links (Google Scholar, GitHub, email) are configured in the `author:` section.
