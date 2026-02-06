# Custo Yang — Personal Site

Retro arcade-themed personal website built with [Astro](https://astro.build). Deployed to GitHub Pages.

## Quick Start

```bash
# Install dependencies
npm install

# Start dev server (localhost:4321)
npm run dev

# Build for production
npm run build
```

## Adding a New Diary Entry

Just create a new `.md` file in `src/content/diary/`:

```
src/content/diary/2026-02-10-my-new-post.md
```

With this frontmatter at the top:

```markdown
---
title: "YOUR TITLE HERE"
date: "FEB 10, 2026"
tags: ["TAG1", "TAG2", "TAG3"]
preview: "First line or two that shows on the main page..."
---

Your full diary entry goes here. Just write in plain markdown.

New paragraphs are separated by blank lines. That's it.
```

Save the file, and it automatically appears on the homepage and gets its own page. No other code changes needed.

## Project Structure

```
src/
├── content/
│   └── diary/           ← Drop new .md files here
│       ├── 2026-02-04-best-ramen.md
│       ├── 2026-01-28-deadlift-pr.md
│       └── ...
├── components/          ← Reusable UI pieces
│   ├── TopBar.astro
│   ├── Ladder.astro
│   └── DiaryCard.astro
├── layouts/
│   └── BaseLayout.astro ← Shared page shell
├── pages/
│   ├── index.astro      ← Homepage (single scroll)
│   └── diary/
│       └── [...slug].astro  ← Auto-generated diary pages
└── styles/
    └── global.css       ← All retro theme styles
```

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages → Source** → select **GitHub Actions**
3. Edit `astro.config.mjs`:
   - Set `site` to `https://YOUR_USERNAME.github.io`
   - Set `base` to `/YOUR_REPO_NAME`
   - If using `username.github.io` as the repo name, remove `base` entirely
4. Push to `main` — the GitHub Action will build and deploy automatically

## Customization

- **Colors**: Edit CSS variables in `src/styles/global.css`
- **Social links**: Update the `href` values in `src/pages/index.astro`
- **Interests**: Edit the interests grid in `src/pages/index.astro`
- **Power-ups/Skills**: Edit the powerups section in `src/pages/index.astro`
