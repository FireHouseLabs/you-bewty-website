# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an Astro-based website project using the basics starter template. It's a simple static site generator project with TypeScript support.

## Development Commands

| Command | Description |
|---------|-------------|
| `npm install` | Install dependencies |
| `npm run dev` | Start development server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview production build locally |
| `npm run astro` | Run Astro CLI commands |
| `npm run astro -- --help` | Get help with Astro CLI |

## Project Architecture

### Core Structure
- **`src/pages/`** - File-based routing; each `.astro` file becomes a page
- **`src/layouts/`** - Reusable layout components (currently `Layout.astro` with basic HTML structure)
- **`src/components/`** - Astro components (currently `Welcome.astro` with hero section)
- **`src/assets/`** - Static assets imported in components (SVGs, images)
- **`public/`** - Static files served directly (favicon, etc.)

### Key Files
- **`astro.config.mjs`** - Minimal Astro configuration (currently default)
- **`tsconfig.json`** - TypeScript config extending Astro's strict preset
- **`package.json`** - Project dependencies (only Astro framework)

### Astro Component Structure
Astro components use a frontmatter section (between `---`) for:
- Imports of other components, layouts, and assets
- Server-side JavaScript/TypeScript code
- Component logic and data fetching

The component template follows standard HTML with:
- Astro-specific syntax like `{variable}` interpolation
- Component imports used as JSX-like tags
- Scoped `<style>` blocks for component-specific CSS

### Current Implementation
The site currently displays a welcome page with:
- Background SVG with blur filter effect
- Hero section with Astro branding and documentation links
- Responsive design with mobile-specific layouts
- Gradient styling and modern CSS properties