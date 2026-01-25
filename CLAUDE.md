# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev      # Start dev server at localhost:4321
npm run build    # Build production site to ./dist/
npm run preview  # Preview production build locally
```

## Architecture

This is a portfolio website built with Astro 5.

**Structure:**
- `src/pages/` - File-based routing (.astro files become routes)
- `src/layouts/Layout.astro` - Base HTML layout with global styles and Google Fonts
- `src/components/` - Reusable Astro components
- `src/assets/` - Static assets processed by Astro (images, SVGs)
- `public/` - Static assets served as-is

**Config:**
- Prefetching enabled for all links using viewport strategy
- Stylesheets are always inlined in production builds
- TypeScript uses Astro's strict config

## Conventions

- Components use scoped `<style>` blocks; global styles live in Layout.astro
- Props are defined using TypeScript interfaces in the frontmatter
