# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Agencja Artystyczna Pro Arte** — a Polish-language marketing website for an artistic agency organizing educational concerts in schools. Single-page site deployed to GitHub Pages.

## Commands

```bash
npm run dev      # Start dev server (localhost:4321)
npm run build    # Build for production (outputs to dist/)
npm run preview  # Preview the production build locally
```

## Architecture

**Framework:** Astro 5 (static site generator, no JS framework). Only one dependency: `astro`.

**Deployment:** GitHub Pages at `https://szprx.github.io/pro-arte`. The `base: '/pro-arte'` in `astro.config.mjs` means all asset paths must use Astro's built-in helpers (`<Image>`, `import.meta.env.BASE_URL`) to resolve correctly. Deployment is automatic via `.github/workflows/deploy.yml` on any push.

**Structure:**
- `src/layouts/Layout.astro` — root HTML shell; loads Google Fonts (Playfair Display + Inter) and Font Awesome 6.4.0 via CDN; accepts `title` and optional `description` props
- `src/components/Header.astro` — sticky nav with mobile hamburger menu (vanilla JS toggle)
- `src/components/Footer.astro` — 4-column footer with dynamic copyright year
- `src/pages/index.astro` — entire single-page site (~1095 lines); all sections are inline in this file: Hero, Offer, Artists, Gallery, Pricing, Contact
- `src/styles/global.css` — design system with CSS custom properties (colors, spacing, shadows, radii, typography)

**Design system (CSS variables in `global.css`):**
- Primary: `--color-primary: #75b89f` (pastel green), Secondary: `--color-secondary: #e8a484` (apricot)
- Fonts: `--font-heading` (Playfair Display, serif), `--font-body` (Inter, sans-serif)
- Breakpoint: 768px (mobile)
- Container max-width: 1200px

**Contact form:** Integrated with Formspree (`https://formspree.io/f/xrekzrnq`). No backend needed.

**Images:** Stored in `public/images/`. Use Astro's `<Image>` component (imported from `astro:assets`) for optimized output — not plain `<img>` tags.

**Language:** All user-facing content is in Polish.
