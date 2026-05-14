# DevOps Downtime Website

Static website for the DevOps Downtime community meetup in Nepal.

## Tech Stack

- HTML + CSS (no framework)
- Static assets in `Resources/`
- Cloudflare Pages deployment via GitHub
- Optional `wrangler.toml` included for Cloudflare Workers static assets

## Project Structure

- `index.html` : Main website page
- `assets/css/style.css` : Stylesheet
- `Resources/` : Logo, background image, and Sora font files
- `robots.txt` : Search crawler rules
- `sitemap.xml` : Sitemap for search engines
- `package.json` : Build script for clean deploy output
- `wrangler.toml` : Worker/static assets config

## Local Development

Open the site directly:

```bash
open index.html
```

## Build Output (for Cloudflare Pages)

Generate a clean deployment folder:

```bash
npm run build
```

This creates:

- `dist/` with only deployable files
- Excludes `.git`, `node_modules`, zip files, and local config artifacts

## Cloudflare Pages (GitHub Connected)

Use these settings in Cloudflare Pages:

- Build command: `npm run build`
- Build output directory: `dist`
- Root directory: `/`

This ensures non-site files (like `.git`) are not deployed.

## Optional: Deploy with Wrangler

If deploying with Workers static assets instead of Pages:

```bash
npx wrangler deploy
```

## SEO + Analytics Included

- Canonical URL and meta tags
- Open Graph and Twitter tags
- JSON-LD structured data
- `robots.txt` and `sitemap.xml`
- Microsoft Clarity tracking snippet

## Contact

Hosting inquiries:

- host@devopsdowntime.com
