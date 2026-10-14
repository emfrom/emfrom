# Editing the site

This site is generated from files in `docs/` with Jekyll. Edit the source files, then push the changes to `main`; GitHub Actions builds and deploys the site.

## Change the site details and menu

- Edit `_config.yml` for the title, description, language, and post URL pattern.
- Edit `_data/profile.yml` for the name, introduction, interests, and links.
- Edit `_data/navigation.yml` to add, remove, rename, or reorder menu links. Each item has a `label` and a site-relative `url`.
- Edit `index.md`, `about.md`, and `writing.md` for page content.
- Edit `assets/css/site.css` to change the visual design.

The navigation, profile details, and post archive are rendered from those source files; there is no runtime server or client-side JavaScript.

## Publish a post

Create a Markdown file in `_posts/` using `YYYY-MM-DD-short-title.md`, for example `2026-04-16-notes-from-the-workbench.md`:

```markdown
---
title: "Notes from the workbench"
description: "A short summary shown in the post list."
---

Write the post in Markdown here.
```

Posts appear automatically on the home page, in the Writing archive, and in the Atom feed. Jekyll uses the date in the filename for the publication date and URL.

## Local preview

Install Ruby and Bundler, then install Jekyll and run:

```sh
gem install jekyll
cd docs
jekyll serve
```

Open <http://localhost:4000>. GitHub Actions performs the production build and deploys successful pushes to `main`.
