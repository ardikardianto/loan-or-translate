# Loan or Translate? — Borrowing Asymmetry Dashboard

An interactive data dashboard and the coded dataset behind a contrastive study of how **Indonesian** and **Malay** rendered the same set of English **COVID-19 health terms**.

Two closely related Malayic standards, coordinated through a shared regional terminology council (MABBIM) yet administered by separate national bodies, were handed an identical glossary of English pandemic terms — and translated them in measurably different ways. Indonesian borrows English forms far more often than Malay, but the tendency is **conditioned by term type and register**, and even reverses for institutional acronyms.

## What's in this repository

| File | Description |
|------|-------------|
| `Borrowing Asymmetry Dashboard.html` | Self-contained interactive dashboard (no internet or libraries required). |
| `05 Coded Dataset.xlsx` | The full 185-term coded dataset (terms, techniques, term type, register, borrowing codes). |
| `validate.RData` | R workspace for reproducing the statistical tests. |

## Viewing the dashboard

Just **double-click `Borrowing Asymmetry Dashboard.html`** to open it in any web browser — it works fully offline. Features:

- **Primary ↔ Sensitivity coding toggle** — flips the native Indonesian initialisms (APD, PDP, ODP) between *borrowing* and *nativisation*; every figure, chart, and table recomputes live.
- **KPI cards** — overall borrowing rates, paired odds ratio, concordance counts.
- **Charts** — borrowing rate by term type and by register, the full translation-technique distribution, and a forest plot of the combined-model odds ratios with confidence intervals.
- **Searchable, sortable, filterable table** of all 185 terms (by English/Indonesian/Malay text, term type, register, or outcome).

## The dataset

185 English source terms from the [Translators without Borders COVID-19 Glossaries](https://glossaries.clearglobal.org/covid19/), each paired with its standard Indonesian and Malay equivalent and coded for:

- **Translation technique** (after Molina & Hurtado Albir 2002; Newmark 1988)
- **Term type** — acronym (n = 13), single-word (n = 88), multiword (n = 84)
- **Register** — Greco-Latin internationalism (n = 73) vs. common-core vocabulary (n = 112)
- **Borrowing** — a binary borrowing / non-borrowing variable, in both *primary* and *sensitivity* codings

## Key findings

- Indonesian borrows substantially more often than Malay: **62.7% vs 44.3%** (exact McNemar, *p* < .001; paired OR = **4.78**).
- The asymmetry is **conditioned by term type** — large for ordinary vocabulary but **reversed for acronyms**, where Malay keeps the English initialism (PPE/PUI/PUM) and Indonesian coins native ones (APD/PDP/ODP).
- **Register sets the volume, not the gap**: both languages borrow internationalisms readily, while Malay's resistance concentrates in common-core vocabulary — yet the Indonesian–Malay gap holds across both registers.
- The pattern is best read as a difference in **language-planning orientation**, not in linguistic structure.

## Reproducing the analysis

The statistics (exact McNemar, stratified interaction tests, and a Firth-penalised conditional matched-pair logistic regression) can be reproduced from the coded dataset in **R** — `validate.RData` contains the working session. See the study's statistics walkthrough for a step-by-step guide.

## Authors

Ardik Ardianto · Agus Riyanto

---

*This dashboard accompanies the manuscript "Loan or Translate? The Borrowing Asymmetry in English COVID-19 Health Terminology." Register coding is a first-pass classification pending native-speaker validation.*
