# Intern to Impact

Career blog and resources by Ariana — from intern to impact. Built with Astro.

## Live site

After Netlify is connected:

- **Production:** `https://intern-to-impact.netlify.app` (update when custom domain is set)
- **Preview:** push to `develop` → `https://develop--intern-to-impact.netlify.app`

Update `site` in `astro.config.mjs` with the real production URL for RSS/sitemap.

## Requirements

- Node.js 22 (`nvm use` reads `.nvmrc`)
- npm

## Commands

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Local dev server (http://localhost:4321) |
| `npm run build` | Production build → `dist/` |
| `npm run preview` | Preview production build |

## GitHub push (first time)

Repo must be pushed before Netlify can import. Push all three branches:

```bash
cd /Users/ksm/Desktop/ari/intern-to-impact
git push -u origin main
git push -u origin develop
git push -u origin original
```

Use a GitHub Personal Access Token as the password (not your GitHub account password).

## Branches

| Branch | Role |
|--------|------|
| `original` | Frozen Lexington + first branding — never delete |
| `develop` | Staging — Netlify preview for Ari |
| `main` | Production live site |

Workflow: work on `develop` → Ari approves → merge to `main`. See `CONTRIBUTING.md`.

## Netlify setup (Artometrics Pro)

1. [Netlify](https://app.netlify.com) → **Add new site** → **Import from Git**
2. Choose **GitHub** → `kylesmcauliffe/intern-to-impact`
3. Build settings: use `netlify.toml` (command `npm run build`, publish `dist`)
4. **Production branch:** `main`
5. **Branch deploys:** enable for `develop` (not `original`)
6. Copy the production URL → update `astro.config.mjs` `site:`

Every push to `main` or `develop` triggers a deploy automatically.

## Project layout

| Path | Purpose |
|------|---------|
| `src/content/posts/` | Published blog posts |
| `src/pages/` | Routes |
| `docs/BRAND.md` | Colors, fonts, voice |
| `public/` | Favicon and static assets |

Drafts for Ari to review live outside the repo: `/Users/ksm/Desktop/ari/content-drafts/`

## Theme

Based on Outkast (Lexington Themes) Astro template, customized for Intern to Impact. See `docs/BRAND.md`.
