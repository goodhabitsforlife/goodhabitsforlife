# Good Habits for Life — Hugo Revamp

This repository contains the full Hugo source for https://goodhabitsforlife.com, designed for speed, accessibility, SEO, and an easy GitOps workflow.

## Deploy
On every push to `main`, GitHub Actions builds and deploys to cPanel via FTP (see `.github/workflows/deploy.yml`). Set repository secrets:
- `FTP_HOST` = your FTP host (e.g., `162.241.116.114`)
- `FTP_USERNAME` = FTP user restricted to `public_html`
- `FTP_PASSWORD` = FTP password
- `FTP_PATH` = `/home1/goodhcnm/public_html`

## Structure
- `content/` — Markdown content (articles, habits, guides, pages)
- `layouts/` — Hugo templates/partials
- `assets/css/` — Source CSS (piped via Hugo pipelines)
- `static/` — Public static files (`.htaccess`, `robots.txt`, images)
- `.github/workflows/` — CI/CD workflows

## Authoring
Create posts under `content/articles/`, `content/habits/`, `content/guides/` with YAML front matter:
```yaml
---
title: "Title"
slug: "slug"
date: 2025-08-31
author: "Dheeraj Issar"
topics: ["topic1", "topic2"]
tags: ["tag1"]
difficulty: "starter"
summary: "1–2 sentence summary."
cover: "/images/cover.jpg"
---
```

## Next Up
- [ ] Add favicon set under `static/`
- [ ] Hook Plausible or GA4 in `layouts/partials/analytics.html`
- [ ] Publish 10–20 cornerstone articles
