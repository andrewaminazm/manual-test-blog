# manual-test-blog

A modern blog about **manual testing** — clear guides for anyone who wants to become a software tester. Built with Astro and Tailwind CSS.

## Tech stack

- **Astro** — Static site generator
- **Tailwind CSS** — Styling
- **Content Collections** — Blog posts as Markdown in `src/content/blog/`

## Commands

| Command           | Action                          |
| ----------------- | ------------------------------- |
| `npm install`     | Install dependencies            |
| `npm run dev`     | Start dev server (localhost:4321) |
| `npm run build`   | Build for production to `./dist/` |
| `npm run preview` | Preview the production build    |

## Project structure

```
src/
├── content/
│   ├── config.ts       # Content collection schema
│   └── blog/           # Markdown blog posts
├── layouts/
│   ├── BaseLayout.astro
│   └── BlogLayout.astro
└── pages/
    ├── index.astro     # Homepage
    └── blog/
        ├── index.astro # Blog listing
        └── [slug].astro # Single post
```

## Adding a new post

Create a new `.md` file in `src/content/blog/` with frontmatter:

```yaml
---
title: Your Post Title
description: Short description for listings and SEO.
pubDate: 2025-02-22
tags: [basics, test design]
---

Your content in **Markdown**...
```

## Deploy

Build the site with `npm run build`, then deploy the `dist/` folder to Vercel, Netlify, or GitHub Pages.
