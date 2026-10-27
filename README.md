# Davao Ordinance Observatory

Read-only public dashboard for the temporal analysis of Davao City ordinances.

**Dashboard:** https://edmcorpuz.github.io/davao-ordinance-observatory/

This repository contains only the static HTML/CSS/JavaScript interface and compact
exported research results. It does not contain raw ordinance text, embeddings,
private reviewer information, or training controls. No sign-in is needed.

## Research source

- Source: [Hackeddog/Thesis_Ordinance-Analysis](https://github.com/Hackeddog/Thesis_Ordinance-Analysis/tree/research/coarse-grained-dashboard)
- Published interface/data snapshot: commit `7739bdc54acfe332fe8e4a78eb0f9093fa1d2499`, directory `dashboard/`.
- Fresh coarse-grained results: 49 lexical / 36 Legal-BERT topics at primary seed 42; sensitivity seeds 43 and 44.
- Dataset: 2,118 source documents / 7,832 model units, 2016–2025.
- All topic labels are drafts, not expert-validated legal categories. Intrinsic metrics are not legal accuracy scores.

## Hosting and updates

GitHub Pages serves `main` at the repository root. `.nojekyll` keeps this a plain
static site with no build dependencies. GitHub Actions builds the Pages deployment
automatically after a push. Only the owner and authorized collaborators can update
this snapshot; visitors cannot upload, modify, or rerun the analysis.

To update, first validate a new publication in the source research repository.
Copy `index.html`, `styles.css`, `app.js`, `data-utils.js`, `data/`, and `downloads/`
from its dashboard directory, retain exact exported bytes, update the source commit
above, and push here. Never replace generated metrics by hand. The research branch
and this deployment repository do not sync automatically.

If collecting legal-expert feedback, use an institution-approved separate channel;
do not commit personal information or completed review responses to this public repo.
