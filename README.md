# Reply AI Refactor (Next.js + TypeScript)

This is a refactored skeleton of the ReplyGenerator project:
- Next.js (App Router)
- TypeScript
- Modular hooks and utils
- Sonner toast UI
- Jest tests

To run locally:
1. `npm install`
2. `npm run dev`

Notes: This repo is a skeleton to get started. Install additional dev tools and tailor to your environment.


## Additional setup
- TailwindCSS: install `tailwindcss`, `postcss`, `autoprefixer` and run the init if needed.
- Playwright: to run e2e, ensure Playwright browsers are installed: `npx playwright install --with-deps`.

## Tailwind Installation
Run: `npm install -D tailwindcss postcss autoprefixer`

## Deployment (Vercel)

1. Create a GitHub repository and push this project.
2. Go to https://vercel.com/new and import your GitHub repo.
3. Use the default build command `npm run build` and output directory `.next`.
4. Vercel will detect Next.js and deploy automatically. Ensure `NODE_ENV` is set to `production` in Vercel env if needed.

## CI / GitHub Actions

- The included workflow runs lint, unit tests and Playwright e2e tests.
- For Playwright to run on CI, the workflow installs Playwright browsers.

## Increase Test Coverage

- Run `npm test -- --coverage` (requires jest config to collect coverage).
- Aim to add tests for analyzeContext, generateReplies edge cases, and UI snapshot tests with React Testing Library.

## Push to GitHub (example script)

Run these commands locally to initialize and push:

```bash
git init
git add .
git commit -m "Initial refactor to TS + hooks + tests + CI"
gh repo create my-reply-ai --public --source=. --remote=origin
git push -u origin main
```

(Use GitHub CLI `gh` or create repo manually on GitHub.)

