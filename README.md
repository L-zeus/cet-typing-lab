# CET Typing Lab

CET Typing Lab is a Vite + React typing trainer for CET4/CET6 sentence drills and full-passage practice. It focuses on WPM, accuracy, weak keys, slow words, passage reading, local progress, and shareable result cards.

## Local Development

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

The production build is configured for GitHub Pages at `/cet-typing-lab/`. If the GitHub repository name changes, update `base` in `vite.config.js` to match the new repository path.

## GitHub Pages

For GitHub Free, keep source code in a private repository and publish only built files to a separate public repository.

Recommended repository split:

- Private source repo: `L-zeus/cet-typing-lab-source`
- Public Pages repo: `L-zeus/cet-typing-lab`

Setup:

```bash
git remote set-url origin git@github.com:L-zeus/cet-typing-lab-source.git
git remote add pages git@github.com:L-zeus/cet-typing-lab.git
```

Configure the repositories once:

1. In `L-zeus/cet-typing-lab`, add a writable Deploy Key.
2. In `L-zeus/cet-typing-lab-source`, add the matching private key as the Actions secret `PAGES_DEPLOY_KEY`.
3. Keep the `pages` remote pointed at `git@github.com:L-zeus/cet-typing-lab.git`.

After that, every push to `origin/main` will:

1. run `npm ci`
2. run `npm run build`
3. run `npm run deploy:pages`
4. push the built site to the public Pages repository automatically

The deploy script builds the app, adds `404.html` and `.nojekyll`, syncs the source repository root `README.md` into the public Pages repository root, and then pushes the published site files. It refuses to run if `pages` points to the same repository as `origin`, which prevents accidentally publishing source history. It also fails fast if the source repository root `README.md` is missing.

In the public Pages repository, open `Settings > Pages` and set `Source` to `Deploy from a branch`, branch `main`, folder `/root`.

Visit `https://L-zeus.github.io/cet-typing-lab/` after Pages finishes deploying.

If the GitHub Action is unavailable or fails and you need an immediate fallback release, run:

```bash
npm run deploy:pages
```

## Notes

- Practice data and accounts are stored locally in the browser.
- No required environment variables are needed for local-auth mode.
- Sound assets live under `public/sounds/` and are served with the GitHub Pages base path.
