# Hi, I'm Yejun (Nicole) Tu 👋

**Data Scientist · Machine Learning in Finance**

I'm a data scientist with five years in finance. I build and validate machine-learning models and take them through to production — I care less about a good offline score than about whether a model still holds up once it's making real decisions. I also work with deep learning in PyTorch.

📍 Vancouver, Canada · open to Toronto & remote

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)

## 🚀 What I do
- Own the data layer day to day: SQL data models, pipelines, and the data-quality checks under them
- Design experiments and use causal inference to answer product and business questions
- Build and validate ML models end to end, from data and features to a deployed, monitored model
- Use data science on financial problems: risk modeling, forecasting, and trading strategy
- Build the risk controls and monitoring around live models (limits, exposure, P&L, safeguards)
- Care as much about validation, calibration, and fairness as about the model itself

## 🛠️ Skills
- **Languages** — Python, SQL, R, C++, Rust, Go, Java
- **ML / modeling** — scikit-learn, XGBoost, LightGBM, statsmodels, SciPy, SHAP, CVXPY, Numba, NumPy, pandas, Polars
- **Deep learning** — PyTorch, neural networks
- **Experimentation & causal inference** — A/B test design, power/MDE, CUPED, multiplicity correction, uplift/CATE modeling, propensity weighting, difference-in-differences
- **Data modelling & pipelines** — dbt (staging → marts, data tests), SQL data modelling, ELT/real-time pipelines, data-quality checks · DuckDB, PostgreSQL, MySQL, IBM Db2, Redshift, MongoDB
- **Analytics** — Matplotlib, Plotly, Jupyter, dashboards and automated reporting
- **Focus areas** — data modelling & pipelines, experimentation & causal inference, predictive & risk modeling, model validation & governance, feature engineering, time-series, LLM/AI tooling
- **Certificates** — AWS Certified Cloud Practitioner · IBM Data Science Professional

## 📌 Featured Projects

### [LLM Validation Harness — challenging a grounded banking assistant](https://github.com/Nicole-Tu97/llm-validation-harness)
`Python · LLM · model risk`

A reproducible harness that validates an LLM assistant against nine model-risk checks: hallucination and unsupported-number detection, abstention, reproducibility, paraphrase robustness, confidence calibration (ECE), persona-swap fairness, PII-leak probes, and prompt-injection attacks — each with a declared pass/fail threshold, benchmarked champion-vs-challenger, and a written validation report.

- **Validated a real Claude (Haiku) model** across 9 controls (one live run): a strict prompt passed all of them (0 PII leaks, all 22 injection attacks resisted), while a weakened prompt made the *same* model **leak PII on 50% of probes** and slip below the hallucination, reproducibility, and robustness gates — separating the two configurations without false-alarming the stronger one on this run.
- Nine checks (133 items) with declared thresholds and champion-vs-challenger benchmarking; deterministic value-based scoring that runs with no API key, or against a live model via `USE_LLM=1`.

### [Credit-Decision PD Model — a governed, AI-augmented ML workflow](https://github.com/Nicole-Tu97/credit-risk-ml-sample)
`Python · scikit-learn · SHAP · LLM`

An end-to-end probability-of-default model built with the validation, fairness checks, SHAP explainability, failure-mode analysis, LLM adverse-action layer, and up-front governance a credit-risk function actually needs. Public UCI data, nothing proprietary.

| Model | AUC | Gini | KS | Brier | PSI |
|---|--:|--:|--:|--:|--:|
| Logistic regression (baseline) | 0.749 | 0.499 | 0.396 | 0.143 | 0.001 |
| **HistGradientBoosting + isotonic (champion)** | **0.781** | **0.563** | **0.428** | **0.135** | **0.002** |

- Leakage-safe features — 32 model inputs (13 engineered + 19 raw credit-history; the 4 protected demographics are excluded from the model), CV-tuned, isotonic-calibrated — 5-fold CV AUC **0.787** ≈ test **0.781**: a *validated* result, not an overfit one.
- **Measured the ceiling rather than asserting one** — the hold-out AUC carries a 95% bootstrap interval of **±0.012**, so the 0.032 gap to the baseline is ~2.7× the noise; a 5×-wider hyperparameter search, random forest, extra trees and a 3-model stack all land in 0.775–0.780, and six `PAY_*` columns alone reach 0.739. The binding constraint is the feature set, not the model — so the 13 engineered features are justified on explainability, not on a discrimination lift that sits inside the noise.
- Disparate-impact fairness audit across sex / age / education / marital status (attributes the model never sees) · SHAP explainability · documented failure modes.
- LLM adverse-action layer constrained to the model's **real** risk drivers; governance mapped to **OSFI E-23** and **FCAC**.

### [Crypto Product Experiment — A/B test, causal inference, ship decision](https://github.com/Nicole-Tu97/crypto-experiment-analysis)
`Python · SQL · dbt/DuckDB · experimentation · causal inference`

Does a crypto auto-invest ("recurring buy") feature actually cause new clients to activate and stick? Raw events → a dbt/DuckDB modelling layer → a full randomized-experiment analysis → two non-randomized causal cross-checks → a one-page ship recommendation. Runs offline from one command; the data is synthetic, so **every estimate is checked against known ground truth** — and the same estimators are then re-run on a **real** experiment to show they aren't tuned to my own generator.

- **Experiment done properly, not just significantly:** pre-registered primary/co-primary/guardrail metrics with a declared MDE and decision rule; SRM and covariate-balance checks before trusting anything; CUPED variance reduction (reporting variance *and* CI-width reduction separately, because they are not the same number); Bonferroni and Benjamini–Hochberg multiplicity control; a simulation showing interim peeking inflates false positives from 5% to ~20%.
- **Causal inference where you can't randomize:** inverse-propensity weighting cuts a self-selection-inflated **+22.8pp** naive retention gap to **+13.2pp** (true value +13.1pp), cross-checked by difference-in-differences. With only 12 clusters, clustering *shrank* the SE — the opposite of the textbook result and a small-cluster warning sign — so a **wild cluster bootstrap** is what the conclusion rests on. A 400-panel simulation confirms the DiD estimator is unbiased and that the classical interval, not the clustered one, is the one that covers.
- **Validated on a real experiment, not just my own data:** the same helpers run against the Hillstrom e-mail experiment (64k real customers, genuinely randomized). Using the experimental contrast as the benchmark, I deliberately confound the sample and then try to recover the answer — **IPW removes 90.8% of the confounding bias on average and 73.2% at worst across 30 draws**.
- **A null result, reported as one:** uplift targeting **failed** on real data (top-vs-bottom separation +1.04pp, p = 0.365). Splitting on the strongest single covariate also failed, and real segment effects span only 6.15–9.90pp — so it's the data, not the model. That also means the 3.5× separation on synthetic data exists because the generator was written to contain it. Worth saying out loud rather than leaving for a reader to find.
- Verified rather than asserted: 500-run Monte Carlo showing **95.4% CI coverage**, 23 dbt data tests, 25 Python tests (dbt-vs-plain-SQL parity, report-vs-metrics consistency), and CI on every push. The stakeholder summary is LLM-drafted behind a mechanical guardrail that rejects any number not traceable to the computed metrics.

## 💼 Experience

**Data Scientist, Quantitative Research · Deepcoin** · 2024 – Present

**Quantitative Analyst · CITIC Securities** · 2020 – 2023

## 🎓 Education
- **MSc, Data Science** — University of British Columbia · 2023–2024
- **BSc, Mathematics & Economics** — Boston University · 2016–2020

## 📫 Contact
- 📧 [yejun.tu1202@gmail.com](mailto:yejun.tu1202@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/yejun-tu-453b7414b/)
- 📍 Vancouver, BC — open to Vancouver / Toronto / remote
