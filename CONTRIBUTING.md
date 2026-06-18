# Contributing — Intern to Impact

## Branch hierarchy

```
original  → frozen archive (Lexington + first branding) — never delete, never merge from
lab       → experiments and active editing
develop   → staging — Ari reviews here
main      → production live site
```

| Branch | Purpose | Netlify | Merge direction |
|--------|---------|---------|-----------------|
| `original` | Archive only | Ignore | — |
| `lab` | Experiments + day-to-day edits | `lab--intern-to-impact.netlify.app` | → `develop` |
| `develop` | Staging / Ari review | `develop--intern-to-impact.netlify.app` | → `main` |
| `main` | Production | `intern-to-impact.netlify.app` | — |

**Never merge directly:** `lab` → `main`, or anything → `original`.

## Workflow

### 1. Edit on `lab`

```bash
git checkout lab
# make changes
git add .
git commit -m "describe change"
git push origin lab
```

Preview: https://lab--intern-to-impact.netlify.app

### 2. Ready for Ari → merge to `develop`

```bash
git checkout develop
git merge lab
git push origin develop
```

Share https://develop--intern-to-impact.netlify.app and `/Users/ksm/Desktop/ari/REVIEW.md`.

### 3. Ari approves → merge to `main`

```bash
git checkout main
git merge develop
git push origin main
```

Production updates automatically.

## Ari’s feedback

- Edit `Desktop/ari/content-drafts/`
- Voice notes / Otter / Zoom
- Comments on preview site

## Local dev

```bash
cd intern-to-impact
nvm use
npm install
npm run dev
```

Open http://localhost:4321

## Do not commit

- GitHub tokens or `.env`
- Large reference screenshots (keep in `Desktop/ari/references/`)

## Restoring the original template

```bash
git checkout original
# or inspect without switching:
git show original:src/pages/index.astro
```
