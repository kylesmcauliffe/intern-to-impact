# Intern to Impact

Career blog and resources by Ariana — from intern to impact. Built with Astro.

## Live site

- **Production:** https://intern-to-impact.netlify.app
- **Staging (Ari):** https://develop--intern-to-impact.netlify.app
- **Experiments:** https://lab--intern-to-impact.netlify.app

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

## Branches

| Branch | Role |
|--------|------|
| `original` | Frozen Lexington archive — never delete |
| `lab` | **Edit here** — experiments and daily work |
| `develop` | Staging — merge from `lab`, Ari reviews |
| `main` | Production — merge from `develop` only |

**Flow:** `lab` → `develop` → `main`. See `CONTRIBUTING.md`.

## Netlify (Artometrics)

- Production branch: `main`
- Branch deploys: `lab`, `develop` (or All)
- Build: `netlify.toml` (`npm run build`, publish `dist`, Node 22)

## Project layout

| Path | Purpose |
|------|---------|
| `src/content/posts/` | Published blog posts |
| `src/pages/` | Routes |
| `docs/BRAND.md` | Colors, fonts, voice |
| `public/` | Favicon and static assets |

Drafts outside repo: `/Users/ksm/Desktop/ari/content-drafts/`

## Theme

Outkast (Lexington Themes) customized for Intern to Impact. See `docs/BRAND.md`.
