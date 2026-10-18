# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Install dependencies
./bin/bootstrap
# or: bundle install

# Local development server (http://localhost:4000)
./bin/start
# or: bundle exec jekyll serve

# Build static site to _site/
bundle exec jekyll build
```

## Architecture

This is a **Jekyll static site** (GitHub Pages portfolio) using the [Moonwalk theme](https://github.com/abhinavs/moonwalk) for a minimalist dark-mode-capable layout.

### Content Structure

- **`_posts/`** — Blog posts, named `YYYY-MM-DD-title.md`. Use front matter with `layout: post`, `title`, `date`, `categories`, `description`.
- **`_projects/`** — Project write-ups. Use front matter `layout: project`, `title`, `description`. Projects are linked from `_data/home.yml`.
- **`_data/home.yml`** — Single source of truth for navigation links, featured projects list, and footer links. Edit this to add/remove items from the homepage.
- **`assets/files/`** — PDFs (resume, project reports). Referenced directly in markdown.
- **`assets/images/`** and **`assets/posts/`** — Images for the site and blog posts respectively.

### Layout Hierarchy

`_layouts/default.html` is the base layout. All other layouts (`home`, `blog`, `post`, `project`, `aboutme`, `projects`) extend it. The `_includes/` directory holds reusable partials like `head.html`, `post_list.html`, and `card_list.html`.

### Styling

- **`_sass/moonwalk.scss`** — Main theme styles (imported by `assets/css/main.scss`).
- **`assets/css/custom.scss`** — Site-specific overrides. Add custom styles here, not to the theme files.
- **`_sass/syntax.scss`** — Rouge syntax highlighting theme.

### Configuration

`_config.yml` controls the site globally. Key fields:
- `title`, `subtitle`, `author` (name + twitter) — Site identity
- `theme_config.appearance` — `auto` / `light` / `dark` (auto follows the visitor's OS setting until they use the pokeball toggle)
- `theme_config.show_*` flags — Enable/disable homepage sections
- `collections.projects.permalink` — URL pattern for project pages

### Theme and build

The Moonwalk theme (github.com/abhinavs/moonwalk) is vendored: all layouts, includes and SCSS live in this repo, and there is no `remote_theme`. Dependencies come from the `github-pages` gem so local builds match what GitHub Pages runs. Images are WebP (except favicons and the `serena_pic.jpg` social-preview image). Repo-only files are kept off the live site by the `exclude:` list in `_config.yml`.
