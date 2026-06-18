# Contributing — Intern to Impact

## Branch hierarchy

```
original  → frozen baseline (Lexington + first branding) — do not delete
develop   → daily work + Ari preview on Netlify
main      → production live site
```

| Branch | Purpose | Netlify | Who merges |
|--------|---------|---------|------------|
| `original` | Archive — initial template state | No deploy | Nobody |
| `develop` | Staging / review | Preview URL | Kyle pushes |
| `main` | Production | Live site | Kyle after Ari approves |

**Do not use `lab`** in this project — use `develop` for experiments or branch off `develop` with a short-lived feature branch.

## Workflow

1. Check out `develop` and make changes.
2. `git push origin develop` → Netlify builds preview.
3. Share `develop--intern-to-impact.netlify.app` with Ari.
4. Ari reviews using `/Users/ksm/Desktop/ari/REVIEW.md`.
5. Merge `develop` → `main` when approved → production updates.

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
