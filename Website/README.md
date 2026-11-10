# STAT 330 soccer goals project website

A **checkpoint-ready starter website** based on the group's uploaded Quarto proposal. Pages: Home, Case Study, and AI Use.

## Contents

- `_quarto.yml`: Quarto website configuration (`output-dir: docs`).
- `index.qmd`, `case-study.qmd`, `ai-use.qmd`: editable Quarto website pages.
- `source/original_proposal.qmd`: the original uploaded proposal with its modeling code preserved.
- `docs/`: already-built static HTML pages for initial GitHub Pages deployment.
- `styles.css`: site formatting.

## Publish via GitHub Pages

1. Create a **public** GitHub repository for your group (or use an existing one).
2. Upload **all** the files/folders in this project, keeping `docs/` at the repository root. Push to the `main` branch.
3. Open the repository's **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**. Select **main** and **/docs**, then **Save**.
4. Open the URL GitHub Pages reports, and test **Home → Case Study → AI Use** links in an incognito/private window.
5. Confirm the site title, all group members, the research question, and the data source are visible, and the displayed site matches the repository.
6. Paste your actual repository URL and the actual published Pages URL into each group member's identical Canvas submission.

## Future edits

Edit the `.qmd` source files, then **if Quarto is installed** run:

```bash
quarto render
```

Commit **both the edited source files and the regenerated `docs/` folder** so the live website shows the current work. The checkpoint's R analysis is intentionally **not executed** on render (`execute: eval: false` in `_quarto.yml`), because installing StatsBombR and downloading match-event data are not necessary for this checkpoint. Remove that setting or override per chunk when you are ready to render the actual results.

## Important note about rendering

The initial `docs/` HTML was generated with Pandoc because the Quarto CLI was not installed in the creation environment. The source `.qmd` files and `_quarto.yml` are set up to render as a Quarto website in your own environment. **Re-render with Quarto before final submission if your instructor specifically requires proof that the HTML was built with Quarto.**
