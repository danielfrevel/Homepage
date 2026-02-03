# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Personal portfolio website built with Astro 5 + Tailwind CSS. Static site deployed via Docker/Nginx.

## Commands

```bash
npm run dev      # Dev server
npm run build    # Production build → dist/
npm run preview  # Preview production build
```

## Architecture

- `src/pages/` - Astro pages (index.astro is main portfolio)
- `src/layouts/Layout.astro` - Base HTML template
- `public/` - Static assets
- Path alias: `@/*` → `src/*`

## Deployment

GitHub Actions builds Docker image on push to main → ghcr.io. Multi-stage build: Node 20 builds site, Nginx serves static files.

## Dev Environment

Nix flake provides Node 20. Run `nix develop` or use Node 20 directly.
