# Tegami — Tell Me Your Story

A bilingual (English/Japanese) oral-history landing page for the **Tegami Oral History Project** — preserving the voices of the pre-Facebook generation.

**Live:** [tegami-oral-history.vercel.app](https://tegami-oral-history.vercel.app)

---

## What's here

| File | Purpose |
|------|---------|
| `index.html` | Full landing page (inline CSS + JS). Responsive, accessible, dark mode, EN/JA toggle. |
| `vercel.json` | Vercel deployment config with security headers and caching. |
| `README.md` | This file. |

## Features

- **Bilingual** — English ↔ Japanese toggle, persisted in `localStorage`
- **Dark mode** — System preference detection + manual toggle, persisted in `localStorage`
- **Responsive** — Mobile-first with hamburger navigation at ≤768px
- **Accessible** — Skip-to-content link, ARIA landmarks, keyboard navigation (Escape to close menu), `prefers-reduced-motion` support
- **SEO-ready** — Open Graph, Twitter Card, JSON-LD structured data, canonical URL
- **Performance** — `preconnect` hints, `font-display: swap`, minimal JS (~80 lines), no dependencies
- **Decorative** — Paper noise texture, animated swoosh lines, waveform visualization, scroll-reveal animations

## Quick start

```bash
# Clone and open directly
open index.html

# Or use a local server (recommended)
python3 -m http.server 8080
# → http://localhost:8080
```

## Deployment

Pushing to `main` triggers Vercel if the project is linked. Manual deploy:

```bash
vercel --prod
```

## Architecture

Single-file static site — all markup, styles, and scripts live in `index.html` for simplicity. Key systems:

- **Theme**: CSS custom properties (`oklch` color space) with `html.dark` class swap
- **Language**: `.en` / `.ja` span pairs toggled via `body.lang-ja` class
- **Animations**: IntersectionObserver for scroll-reveal, CSS keyframes for decorative elements
- **Mobile menu**: Full-screen overlay with staggered entry animations, `aria-expanded` state management

## Contributing

- **Content fixes** (copy, translations, links): edit `index.html`, submit a PR to `main`.
- **Larger refactors**: open an issue first to discuss scope.

## Contact

hello@mytegami.win · [LinkedIn](https://linkedin.com/company/mytegami) · [mytegami.win](https://mytegami.win)

## License

Add a `LICENSE` file to indicate the intended license.
