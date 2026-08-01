# Dumoji static site

This directory is a self-contained static website for Dumoji. It is intentionally
separate from the parent Hugo site so it can be deployed as its own Cloudflare
Pages project.

## Routes

- `/` — English game page
- `/support/` — English support
- `/privacy/` — English Privacy Policy
- `/terms/` — English Terms of Service
- `/tr/` — Turkish game page
- `/tr/support/` — Turkish support
- `/tr/privacy/` — Turkish Gizlilik Politikası
- `/tr/terms/` — Turkish Kullanım Koşulları

## Cloudflare Pages

Connect this repository to Cloudflare Pages with:

- Production branch: `main`
- Build command: empty (or `exit 0`)
- Build output directory: `dumoji-site`

The site has no runtime dependencies or build step. The parent Hugo workflow
does not copy this directory into the personal site's `public/` output.

The internal links use explicit `index.html` targets so the site also works when
the homepage is opened directly from a `file://` URL. A static host will still
serve the same pages at their usual directory routes.
