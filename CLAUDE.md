# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Site Overview

Personal website and blog at **hypothetical.ink** (custom domain via CNAME). Built with Jekyll using a customized [just-the-docs](https://just-the-docs.com/) theme (v0.10.1). Deployed to GitHub Pages via GitHub Actions on push to `main`.

## Common Commands

```bash
# Install dependencies
bundle install

# Local development server (auto-reloads on changes, but NOT for _config.yml edits)
bundle exec jekyll serve

# Build the site (outputs to _site/)
bundle exec jekyll build

# Lint CSS and formatting
npm run lint

# Auto-format SCSS/JS/JSON
npm run format
```

## Architecture

### Content Structure

- **`_posts/`** — Blog posts. Filename format: `YYYY-MM-DD-slug.md`. Permalink pattern: `/blog/:slug` (set in `_config.yml`).
- **`_drafts/`** — Unpublished posts. Preview with `bundle exec jekyll serve --drafts`.
- **`apps/`** — App pages (e.g., NiftyScan with privacy/terms/support subpages).
- **`category/`** — Category pages for blog post filtering (product, payments, design).
- **`blog/index.md`** — Blog listing page, iterates over `site.posts`.

### Theme Customization

The site uses just-the-docs as a gem dependency (via `just-the-docs.gemspec`) with local overrides:

- **`_layouts/`** — Custom layouts: `post.html` (blog posts), `home.html`, `about.html`, `minimal.html` (used for apps). All extend `default.html`.
- **`_includes/components/sidebar.html`** — Customized sidebar navigation.
- **`_sass/custom/`** — Custom SCSS overrides on top of the theme.
- **`_data/links.yml`** — Data file for navigation links.

### Configuration

- **`_config.yml`** — Jekyll config. Dark color scheme. Lunr search enabled. Mermaid diagrams enabled. Liquid strict mode.
- **`_config.yml` changes require server restart** — Jekyll does not hot-reload this file.
- **`.markdownlint.json`** — Allows multiple H1s, long lines, and inline HTML in markdown.

### Deployment

GitHub Actions workflow (`.github/workflows/deploy.yml`) builds with Ruby 3.4 and deploys to GitHub Pages on push to `main`. No manual deploy steps needed.

## Blog Post Deployment from Obsidian Vault

Blog posts are authored in an Obsidian vault and deployed to this repo by Claude Code.

### Vault Location

The Obsidian vault is at: /Users/suman/Documents/Obsidian/smnd/

Posts ready for deployment are in: {vault-path}/blog/
The pipeline tracker is at: {vault-path}/blog/_pipeline.md

### Source

Posts ready for deployment live in the vault's `blog/` folder. Only posts with `blog/published` in their tags are eligible.

### Frontmatter

Blog post files carry two sets of frontmatter fields. When copying to the repo, keep the Jekyll fields and strip the vault fields.

**Keep (Jekyll):**

- `layout` (always `post`)
- `title`
- `date`
- `categories`
- `summary`

**Strip (vault-only):**

- `tags`
- `References`
- `Created`
- `Updated`
- `Status`
- `slug`
- `type`
- `source`

### Duplicate Prevention

The `slug` field in the post's frontmatter is the unique identifier.

- Before copying a post, check whether a file with that slug already exists in the content folder.
- No match: new post. Create the file.
- Slug exists: update. Replace the existing file.
- No slug in frontmatter: reject. Do not deploy. Ask for a slug to be set first.

### Deployment Checklist

Before deploying a post, verify all of these:

1. Post has a `slug` field in frontmatter.
2. Post has `blog/published` in tags.
3. Post has `layout`, `title`, `date`, and `categories` set.

### Rules

- Never deploy a post without checking the slug first.
- Never change a slug. If a slug needs changing, that decision happens in the vault, not the repo.
- Commit each post as a separate commit with message format: `publish: {slug}` (new) or `update: {slug}` (existing).
- Do not add co-authored by Claude when committing blog posts and content pages.
- Do not modify or delete other posts in the same commit.
- When committing and pushing any file in `_posts/`, update the `date` frontmatter field to the current date and time (in `DD-MM-YYYY HH:MM:SS +0800` format) before committing. This only applies to post files that are part of the commit — do not touch posts that are not being changed.
