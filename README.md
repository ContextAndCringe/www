# Context & Cringe — Website

Jekyll site for [Context & Cringe](https://cybersecgames.com/collections/privacy/products/context-cringe), a card game about privacy, apps, and uncomfortable design choices.

---

## Structure

```
context-cringe-site/
├── _config.yml          # Site settings (title, buy URL, etc.)
├── _layouts/
│   └── default.html     # Shared HTML wrapper (header + footer)
├── _includes/
│   ├── header.html      # Sticky nav
│   ├── footer.html      # Footer
│   └── hazard.html      # Orange stripe divider
├── _posts/              # Blog posts (Markdown)
├── assets/
│   ├── css/main.css     # All shared styles
│   └── images/          # Logo, photos, tokens
├── index.html           # Homepage
├── how-it-works.html    # Game rules page
├── facilitators.html    # Facilitator guide
├── about.html           # About page
└── blog.html            # Blog index
```

---

## Local Development

**Requirements:** Ruby 3+, Bundler

```bash
# Install dependencies
bundle install

# Run local server (http://localhost:4000)
bundle exec jekyll serve

# Build static site to ./_site/
bundle exec jekyll build
```

---

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository
2. Go to **Settings → Pages**
3. Set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`
4. GitHub will build and deploy automatically

> If you use a custom domain, add a `CNAME` file to the root with your domain name (e.g. `contextandcringe.com`).

---

## Adding Blog Posts

Create a new file in `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
layout: default
title: Your Post Title
date: 2025-06-01
excerpt: "A short description shown in the blog index."
---

Your post content here, written in Markdown.
```

---

## Updating the Buy Link

Edit `_config.yml`:

```yaml
buy_url: "https://cybersecgames.com/collections/privacy/products/context-cringe"
```

This URL is used site-wide via `{{ site.buy_url }}` — change it in one place and it updates everywhere.

---

## Images

All images live in `assets/images/`. To update a creator photo or the logo, replace the file with the same filename.

| File | Used for |
|---|---|
| `logo.svg` | Header + footer |
| `box.png` | Homepage (game photo placeholder) |
| `tokens.png` | Comfy/Cringe vote indicators |
| `kim.png` | About page — Kim's photo |
| `avi.png` | About page — Avi's photo |
| `professorprivacy.png` | About page — Kim's alter ego (hover easter egg) |
| `captainsecurity.png` | About page — Avi's alter ego (hover easter egg) |
