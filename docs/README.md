# Risky Business: Quantitative Portfolio Management for Optimized Risk

**Portfolio Resilience: Backtesting Asset Allocation Strategies During Financial Crises**

Dane Herrin & Alexander Jackson · DATA 510 Data Science Capstone · Willamette University · Summer 2026

**Project site:** https://awjackson00.github.io/data510-Quant-Back-Testing/
*(update this URL if your GitHub Pages username/repo differs — see "Publishing this site" below)*

**Analysis repository:** https://github.com/awjackson00/data510-Quant-Back-Testing

---

## What this is

A reproducible backtesting workflow comparing five portfolio constructions (Barbell,
Mega-Cap Technology, Energy, Real Estate, FMCG) across nine historical market regimes from
the Dot-com crash through the post-2023 period, evaluated on Sharpe ratio, Sortino ratio,
annualized return, and cumulative return — not return alone.

This folder (`/docs` in the analysis repo, or the root of a dedicated `-site` repo) is the
**public-facing project site**: landing page, full write-up, results and figures, a
reproducibility guide, an ethics and data notice, and team information. It is the Milestone 5
deliverable ("Project Website and Dissemination") for DATA 510.

## Site contents

| Page | Covers |
|---|---|
| `index.html` | Landing page: summary, key results snapshot, portfolio definitions, ethics notice, team |
| `results.html` | Full Table 1 (Sharpe/Sortino/return by portfolio × regime) and Figures 1–3 |
| `writeup.html` | Complete write-up: abstract through references |
| `reproducibility.html` | Step-by-step clone/install/reproduce guide |
| `assets/poster.pdf` | One-page project poster |
| `assets/figures/` | Figures 1–3, exported from the analysis notebooks |

## Publishing this site (GitHub Pages)

1. Push this folder to a repository — either as the `/docs` folder of the analysis repo, or
   as its own repo (e.g. `data510-Quant-Back-Testing-site`).
2. In the repo's **Settings → Pages**, set the source to the branch and folder containing
   these files (`main` / `/docs`, or `main` / `/root`).
3. GitHub serves the site over HTTPS automatically at
   `https://<username>.github.io/<repo>/` (or `.../<repo>/docs/` if published from a subfolder
   without moving it to root — publishing from `/docs` at the repo root avoids that extra
   path segment).
4. Replace the placeholder URL at the top of this README with the real Pages URL once it is
   live, and add the same link to your GitHub profile README and to Canvas.

## Reproducing the analysis

See [`reproducibility.html`](reproducibility.html) for the full guide, or the short version:

```bash
git clone https://github.com/awjackson00/data510-Quant-Back-Testing.git
cd data510-Quant-Back-Testing
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter lab notebooks/
```

Run the notebooks in order: `EDA Capstone.ipynb` → `portfolioConstruction.ipynb` →
`SharpeRatioSheet.ipynb` (source of Table 1) → `ARIMA Time-Series Modeling.ipynb` (optional).

## Data & ethics

All data are public market data pulled live from Yahoo Finance via `yfinance`; no raw market
data is redistributed in this repository. The project contains no personally identifiable
information. All results are historical and educational — **not investment advice**. See
`index.html#ethics` for the full notice, including backtesting limitations (hindsight bias,
survivorship bias, staggered asset inception dates, and excluded transaction costs).

## License

Site and analysis code: MIT License (see `LICENSE`). Market data is used under Yahoo
Finance's terms via the open-source `yfinance` package.
