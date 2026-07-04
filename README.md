# PortfolioAI

A high-fidelity UI prototype for **PortfolioAI** — a SaaS concept that helps people build beautiful portfolio websites with AI. The design language draws on Apple's Human Interface Guidelines, Linear, Notion, Framer, and Arc Browser: premium, minimal, and fast, with soft shadows, glassmorphism, and purposeful motion throughout.

> This repo contains a single self-contained HTML prototype (`portfolioai.html`) covering the Landing page, Dashboard, and Portfolio Builder. It's a design/interaction prototype, not a production app — see [Roadmap](#roadmap) for what a real build would need.

## Preview

Open `portfolioai.html` in any modern browser. No build step, no dependencies, no server required.

A pill switcher fixed to the top of the page (labeled **Landing / Dashboard / Builder**) lets you jump between the three screens — that switcher is prototype-only scaffolding and isn't part of the product itself.

## Features

**Landing page**
- Sticky glass navigation with backdrop blur
- Gradient-blob hero with an animated floating preview mockup
- Stats strip, 6-card feature grid, testimonials, 3-tier pricing, accordion FAQ, CTA banner
- Scroll-triggered fade/slide-in animations throughout

**Dashboard**
- Personalized greeting header
- Stat cards (portfolios, templates, views, published, drafts)
- Recent portfolios list with status badges
- Quick action shortcuts into the builder

**Portfolio Builder**
- Three-panel layout (sections sidebar / editor / live preview), inspired by Figma and Notion
- 9-step progress flow with an autosave indicator
- Floating-label inputs, skill tag input, duplicate/remove project cards, experience timeline
- Live preview with a working Desktop / Tablet / Mobile device switcher
- Floating AI Assistant panel with suggestion chips and a simulated typing indicator
- Confetti + toast on Publish

**Design system**
- Light and dark themes, toggleable, using the full color and shadow tokens from the spec
- 8-point spacing grid, consistent border radii (buttons 14px, cards 24px, inputs 16px, modals 28px)
- Inter typeface, reusable button/card/input/chip/badge/toast/accordion/progress components
- Motion in the 200–300ms range: hover elevation, skeleton loading, typing animation, page transitions

## Tech

Built as plain HTML, CSS, and vanilla JavaScript — no framework or build tooling required to view it.

The original spec targets a production stack of:

- Next.js + React
- Tailwind CSS
- shadcn/ui
- Framer Motion
- Lucide Icons

Porting this prototype into that stack is the natural next step (see below).

## Getting started

```bash
git clone <your-repo-url>
cd portfolioai
open portfolioai.html   # or just double-click the file / drag it into a browser
```

No install, no server, no environment variables.

## Project structure

```
portfolioai/
├── portfolioai.html   # entire prototype: markup, styles, and behavior
└── README.md
```

Everything is intentionally kept in one file for easy sharing and review. If this moves into a real codebase, the natural split is:

```
components/    # Button, Card, Input, Chip, Toast, Accordion, etc.
sections/      # Hero, Features, Pricing, FAQ, Dashboard panels, Builder panels
lib/           # theme, animation, and state utilities
app/           # Next.js routes: /, /dashboard, /builder, /templates, /analytics, /settings
```

## Roadmap

This prototype covers Landing, Dashboard, and Builder. Not yet built out:

- [ ] Templates gallery (filterable by category, hover preview, favorites)
- [ ] Full published portfolio page (public-facing, SEO-optimized)
- [ ] Analytics page with real charts (weekly / monthly / yearly)
- [ ] Settings page (theme, language, notifications, export, account, privacy)
- [ ] Real AI integration (resume parsing, bio/summary generation, tone rewriting)
- [ ] Auth, persistence, and a real publish/deploy pipeline
- [ ] Port to Next.js + Tailwind + shadcn/ui + Framer Motion for production use

## Accessibility

The prototype uses semantic HTML, visible focus states, and AA-contrast color pairs from the spec. Full keyboard navigation, ARIA labeling, and screen-reader passes are still needed before this would be production-ready.

## License

Add a license of your choice (MIT is a common default for prototypes like this).
