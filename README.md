# Jekyll Blog on GitHub Pages

This repository is set up for a Jekyll blog that deploys with GitHub Pages.

## 1) Prerequisites (Windows)

- Install **Ruby** (with DevKit) from RubyInstaller.
- Install **Bundler**:

```powershell
gem install bundler
```

## 2) Install dependencies

From this folder:

```powershell
bundle install
```

## 3) Run locally

```powershell
bundle exec jekyll serve
```

Open: `http://localhost:4000`

## 4) Publish to GitHub Pages

1. Create a GitHub repo and push this code.
2. For a user site, use repo name: `<your-username>.github.io`.
3. In GitHub: **Settings > Pages**
   - Source: **Deploy from a branch**
   - Branch: `main` / `(root)`

For a project site (repo name not `<username>.github.io`), set `baseurl` in `_config.yml` to `/<repo-name>`.

## 5) Create new posts

Add markdown files in `_posts/` named like:

`YYYY-MM-DD-title.md`

Example front matter:

```yaml
---
layout: post
title: "My new post"
date: 2026-04-20 12:00:00 +0000
categories: notes
---
```
