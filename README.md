# Living Branch Development (Astro)

Production website for Living Branch Development, built with **Astro 5** (static output), **Tailwind CSS**, and optional **React islands**.

## Project structure (production-grade)

```text
/
├── public/                       # Static files served as-is (favicons, robots.txt, etc.)
├── src/
│   ├── assets/                   # Optional convention for imported assets (non-breaking)
│   ├── components/               # Reusable UI components (Astro / React)
│   │   └── sections/             # Page sections
│   ├── data/                     # Shared data/copy objects (optional convention)
│   ├── images/                   # Image assets imported via astro:assets (current location)
│   ├── layouts/                  # Page layouts
│   ├── lib/                      # Shared utilities (optional convention)
│   ├── pages/                    # Routes
│   ├── styles/                   # Global styles
│   ├── types/                    # Shared types
│   └── env.d.ts                  # Env typings
├── astro.config.mjs              # Astro config (sitemap enabled)
├── package.json
└── tsconfig.json
```

## Commands

```bash
npm install
npm run dev
npm run build
npm run preview
```

## Sitemap + canonical URLs

This project enables `@astrojs/sitemap`. Set your production site URL:

- **Local (PowerShell):**

```powershell
$env:SITE_URL="https://yourdomain.com"; npm run build
```

- **Mac/Linux:**

```bash
SITE_URL=https://yourdomain.com npm run build
```

Or set `SITE_URL` in your hosting platform environment variables.

## Deployment (static hosting)

Build output is generated into `dist/`. Deploy by uploading the **contents** of `dist/` to your host.

Common hosts:
- **Hostinger shared**: upload `dist/` contents to `public_html`
- **Netlify/Vercel/Cloudflare Pages**: set build command `npm run build`, output folder `dist`

