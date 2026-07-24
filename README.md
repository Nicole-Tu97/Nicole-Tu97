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
- Build and validate ML models end to end, from data and features to a deployed, monitored model
- Use data science on financial problems: risk modeling, forecasting, and trading strategy
- Build the risk controls and monitoring around live models (limits, exposure, P&L, safeguards)
- Care as much about validation, calibration, and fairness as about the model itself

## 🛠️ Skills
- **Languages** — Python, SQL, R, C++, Rust, Go, Java
- **ML / modeling** — scikit-learn, XGBoost, LightGBM, statsmodels, SciPy, SHAP, CVXPY, Numba, NumPy, pandas, Polars
- **Deep learning** — PyTorch, neural networks
- **Data** — PostgreSQL, MySQL, IBM Db2, Redshift, MongoDB · Matplotlib, Plotly, Jupyter
- **Focus areas** — predictive & risk modeling, model validation & governance, feature engineering, time-series, LLM/AI tooling
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
- Disparate-impact fairness audit across sex / age / education / marital status (attributes the model never sees) · SHAP explainability · documented failure modes.
- LLM adverse-action layer constrained to the model's **real** risk drivers; governance mapped to **OSFI E-23** and **FCAC**.

## 💼 Experience

**Quantitative Researcher, Data Science · Deepcoin** · 2024 – Present

**Quantitative Analyst, Data Science · CITIC Securities** · 2020 – 2023

## 🎓 Education
- **MSc, Data Science** — University of British Columbia · 2023–2024
- **BSc, Mathematics & Economics** — Boston University · 2016–2020

## 📫 Contact
- 📧 [yejun.tu1202@gmail.com](mailto:yejun.tu1202@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/yejun-tu-453b7414b/)
- 📍 Vancouver, BC — open to Vancouver / Toronto / remote
