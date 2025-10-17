## Copilot instructions for pets-breed-learning

Purpose: short, actionable notes to help an AI coding agent be productive editing this repository.

- Project shape
  - Single static page: `index.html` is the app. Styles are currently inline inside the `<head>` (see the `.container` and `body` rules). There is no `src/`, `package.json`, or build system.
  - README.md is minimal; treat this repo as a small static landing / learning prototype.

- Quick start (what to run)
  - Open `index.html` in a browser locally, or run a static server from the repo root:

    ```bash
    python3 -m http.server 8000
    # then open http://localhost:8000 in your browser
    ```

- Big-picture guidance for edits
  - Keep changes minimal and self-contained. Prefer adding new assets under a new `assets/` directory (images, fonts) and linking them from `index.html`.
  - If you add CSS, create `styles.css` at the repo root and link it from `index.html` instead of further inlining large style blocks.
  - If you add JavaScript, place scripts right before `</body>` and keep behavior progressive (the page should render without JS).

- Project-specific patterns found (examples)
  - Global reset and gradient background live in the `<style>` block in `index.html` — follow the same CSS variables and font stack when extending styles.
  - The visual layout centers content using a `.container` class with `max-width: 800px`, `border-radius: 20px`, and drop shadow. Use this class for primary content cards.

- Conventions & assumptions
  - No build tools present; assume changes are shipped directly as static files. If you introduce tooling (npm, bundlers), commit a clear README section and a `package.json` so reviewers know how to run it.
  - Add new resources under `assets/` and reference them with relative paths (e.g. `assets/img/dog.jpg`).

- Integration & deployment notes
  - This project is safe to host as a static site (GitHub Pages, Netlify, Vercel). No backend integrations or API keys are present in the repo.

- When creating PRs
  - Keep PRs focused (one UI/feature per PR), include a short screenshot of visual changes, and reference which files in `index.html` you modified.

- What is NOT present (so avoid assumptions)
  - There are no tests, no CI config, and no package manager files. Don't assume bundling, linting, or automated tests exist unless you add them and document how to run them.

If any of these assumptions are wrong or you want explicit conventions (branch naming, CI, tests), tell me which area to standardize next and I will update this file.
