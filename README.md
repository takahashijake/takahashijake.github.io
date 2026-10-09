# Jake Takahashi — Portfolio

Dependency-free static developer portfolio for GitHub Pages at https://takahashijake.github.io/.

## Local development

Requires Node.js 22+ (no npm dependencies).

```sh
npm run build
npm test
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. Re-run `npm run build` after modifying source files; reload the page to inspect changes.

## Architecture

- `index.html` — semantic content, navigation, structured project case studies, verified repository links.
- `styles.css` — design tokens, responsive layout, keyboard focus and reduced-motion support.
- `script.js` — minimal progressive enhancement.
- `assets/headshot-placeholder.svg` — **illustrative placeholder, not a real photograph**; replace with an authentic photo, change its alt text, and update the label when ready.
- `scripts/build.mjs` — packages static files into `dist/`.
- `tests/` — Node built-in smoke tests for structure, asset paths and project links.
- `.github/workflows/pages.yml` — validates PRs and builds/deploys on pushes to `main`.

## Deployment

1. Review and merge the portfolio PR to `main`.
2. In repository Settings → Pages, select **GitHub Actions** as the source (if needed).
3. The workflow validates on PRs, and on a push to `main` uploads the built `dist/` artifact and deploys it using `actions/deploy-pages`.
4. Check Actions for a successful deploy run, then verify https://takahashijake.github.io/ directly before announcing the site as live.

The PR alone does **not** deploy the site. Do not claim a successful deployment until the Pages workflow and live URL are confirmed.

## Content provenance

Project descriptions are intentionally qualitative and grounded in inspected public `main` source, documentation, tests, and commit-specific CI runs for [LLM-Town](https://github.com/takahashijake/LLM-Town), [BenchForge](https://github.com/takahashijake/BenchmarkingProject), [AgentBench](https://github.com/takahashijake/AgentBench), [MiniGame](https://github.com/takahashijake/MiniGame), and [GestureDetectionPractice](https://github.com/takahashijake/GestureDetectionPractice). No fabricated benchmark scores, employment history, email address, LinkedIn identity, or live-demo links.

Evidence reviewed October 9, 2026: GestureDetectionPractice `2c40ce0` (PRs #2/#3 merged), AgentBench `9d3280c` (privacy fix #37 and progress #40 open), and MiniGame `d643a1d` (persistence/replay PR #4 open). AgentBench progress PR #40 CI passes at `457bcf4` (run `37713880440`); MiniGame PR #4 CI passes at `9d9b231` (run `37493870041`). Both remain unmerged. Case-study links pin source evidence to the inspected commit and CI run. Passing CI is scoped to its actual checks; it does not establish real-agent performance, real-camera accuracy, or graphical browser/offline behavior.

## Maintenance

Update project claims only after checking source/docs; link to the actual code and verification material. Preserve keyboard navigation, contrast, responsive layout and respectful reduced-motion settings. Replace the SVG headshot placeholder when an approved portrait is available.
