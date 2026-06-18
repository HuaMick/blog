# Mick's Notes

A small custom Jekyll blog, published with GitHub Pages. Essays on building
software with AI agents.

- Posts live in `_posts/` as Markdown (`YYYY-MM-DD-title.md`).
- Layouts in `_layouts/`, styling in `assets/css/style.css` (minimalist cards,
  dark-mode aware, no external theme).
- The site renders at https://huamick.github.io/blog/

## Add a post

Drop a Markdown file in `_posts/` with front matter and push:

```markdown
---
layout: post
title: "Your title"
date: 2026-06-20
description: "One-line summary shown on the card."
image: /assets/img/your-cover.jpg   # optional cover image
---

Body...
```

To give a post a card/cover image, add the file under `assets/img/` and set
`image:` in the front matter.
