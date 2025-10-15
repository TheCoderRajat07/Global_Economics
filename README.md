# Global Economics Analyzer

**A friendly, research-first toolkit for understanding how the world economy and markets really behave.**

---

## What this is

Global Economics Analysis is a practical, reproducible codebase for exploring macro trends, market behavior, and the big events that shaped global economics. This is a pure analysis project — no web UI, no production model serving. Think of it as a research lab: clean data, transparent experiments, clear visuals, and reproducible notebooks you can share.

## Who it’s for

* Analysts and researchers who want a tidy workspace for macro work.
* Policy students and economists exploring transmission channels across markets.
* Anyone who wants reproducible, explainable studies of major economic events.

## Why it matters

Markets move for many reasons — policy shifts, supply shocks, investor psychology. This repo helps you gather the right data, run careful time-series and event studies, and produce insights you can trust and explain.

## Quick highlights

* Ingests public macro and market data and keeps it tidy and versioned.
* Tools for time-series analysis, event studies, and causal checks.
* Reproducible notebooks and static reports that document every step.

## Getting started (fast)

1. Clone the repo and create a Python environment (venv / conda / poetry).
2. Install dependencies: `pip install -r environment/requirements.txt`.
3. Fill `secrets.example` with API keys and set paths in `config.yml`.
4. Run a one-shot ingestion: `python src/ingestion/fetch_all.py --start 2000-01-01`.
5. Open `notebooks/` and run the example exploration notebooks.

## Example workflows

* **Trend analysis:** Decompose series, check stationarity, find structural breaks.
* **Market transmission:** Fit VARs, plot impulse responses, test Granger causality.
* **Event studies:** Pick an event window, compute abnormal changes, bootstrap confidence intervals.
* **Causal checks:** Run difference-in-differences or synthetic control where applicable.

## Data sources (examples)

We favor public, citable sources with clearly-stated licenses:

* FRED, World Bank, IMF (WEO/IFS), OECD
* National statistical agencies
* Public market data (index/price APIs)
* Policy docs, central bank minutes, filings

> **Heads up:** Respect all data licenses. For paid datasets, add instructions and keep keys out of version control.

## Repo layout

```
/GLOBAL-ECON-ANALYZER/
├─ data/                  # raw / interim / processed (don’t commit raw vendor data)
├─ notebooks/             # analysis notebooks (Jupyter)
├─ src/                   # ingestion / feature / analysis / viz modules
├─ reports/               # generated charts & PDFs
├─ environment/           # requirements / env files
├─ README.md
└─ LICENSE
```

## Tools we use

* **Data & analysis:** pandas, xarray, statsmodels, arch, pmdarima
* **Causal & econometrics:** linearmodels, causalimpact, econml (optional)
* **NLP & events:** spaCy, transformers (for extracting narratives)
* **Viz & reports:** matplotlib, seaborn, plotly, altair, nbconvert

## Reproducibility & provenance

* Keep `data/raw`, `data/interim`, `data/processed` with checksums and logs.
* Tag notebooks with the data snapshot and git commit used for results.
* Store config in `config.yml`; never commit secrets.

## Deliverables

* Cleaned, versioned datasets for core macro indicators.
* Reproducible notebooks for trend, transmission, and event studies.
* A final report summarizing findings and implications.

## How to contribute

1. Open an issue describing your idea.
2. Fork → create a feature branch → open a PR with notebooks & tests.
3. Document data sources and any manual cleaning in notebook cells.

## License & contact

MIT License.

Project lead: **Rajat K. Khairnar** 

---

*Tip: Start with one case study (e.g., 2008 or 2020) and a handful of high-quality indicators. Build reproducible insights, then expand.*
