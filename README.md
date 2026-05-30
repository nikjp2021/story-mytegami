
# Tegami — Tell Me Your Story

Short description

Tegami is a bilingual (English/Japanese) oral-history landing page and micro-site for the "Tell Me Your Story" project. This repo contains a single-file static landing page (index.html) designed to be deployed to Vercel or any static host.

Live

- https://tegami-oral-history.vercel.app

What’s here

- index.html — the full landing page (inline CSS + JS). Mobile-first, accessible-ish, light animations, dark mode, EN/JA copy.
- vercel.json — Vercel configuration used on deployment.
- README.md — this file.

Quick start

1. Clone the repository and open index.html directly for a fast preview.
2. For a local server (recommended):

   python3 -m http.server 8080

   Then visit http://localhost:8080

Deployment

- The project is ready for static deployment. Pushing to the main branch will trigger Vercel if the project is linked.
- If you use Vercel CLI: `vercel --prod` (requires VERCEL_TOKEN / account access).

Editing notes

- All markup, styles, and scripts are in index.html for simplicity. For maintainability, consider extracting CSS and JS into separate files and updating vercel.json if needed.
- Language toggle uses body.lang-ja; the default language is English.
- Theme preference is stored in localStorage under `tegami-theme`.

Contributing

- For content fixes (copy, translations, links): edit index.html and submit a PR to main.
- For larger refactors (componentize CSS/JS, add forms, analytics), open an issue describing the scope before starting.

Contact

- Project contact: hello@mytegami.win

License

- Add a LICENSE file to this repo to indicate the intended license. If you want, I can add an MIT or CC-BY license.
