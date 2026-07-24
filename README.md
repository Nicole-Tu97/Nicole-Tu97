# Hi, I'm Yejun (Nicole) Tu 👋

**Data Scientist · Machine Learning in Finance**

I'm a data scientist with about five years in finance, and I really enjoy this work. I build and validate machine-learning models and own them end to end: framing the problem, building the model, checking it holds up in production, and seeing it drive real decisions. I also work with deep learning (PyTorch), and lately I've been getting into reinforcement learning.

📍 Vancouver, Canada · open to Toronto & remote

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)

## 🚀 What I do
- Build & validate **ML models end-to-end** — data → features → modeling → validation → deployment
- Use **data science to solve financial problems** — from risk modeling to optimizing profit
- Build the **risk controls and real-time trade monitoring** around live models — exposure, P&L, and drawdown safeguards
- Care about **impact and rigor** — models that are accurate, calibrated, fair, and defensible, not just built

## 🛠️ Skills
- **Languages** — Python, SQL, R, C++, Rust, Go, Java
- **ML / modeling** — scikit-learn, XGBoost, LightGBM, statsmodels, SciPy, SHAP, CVXPY, Numba, NumPy, pandas, Polars
- **Deep learning** — PyTorch, neural networks
- **Data** — PostgreSQL, MySQL, IBM Db2, Redshift, MongoDB · Matplotlib, Plotly, Jupyter
- **Focus areas** — predictive & risk modeling, model validation & governance, feature engineering, time-series, LLM/AI tooling
- **Currently exploring** — reinforcement learning (RL)
- **Certificates** — AWS Certified Cloud Practitioner · IBM Data Science Professional

## 📌 Featured Projects

### [LLM Validation Harness — challenging a grounded banking assistant](https://github.com/Nicole-Tu97/llm-validation-harness)
`Python · LLM · model risk`

A reproducible harness that validates an LLM assistant the way a second-line model-risk team would: hallucination and unsupported-number detection, abstention, reproducibility, paraphrase robustness, confidence calibration (ECE), persona-swap fairness, PII-leak probes, and prompt-injection attacks — each with a declared pass/fail threshold, benchmarked champion-vs-challenger, ending in a written validation report.

- **Validated a real Claude (Haiku) model** across 9 controls: a strict grounding prompt cleared all of them (0 PII leaks, all 22 injection attacks resisted), while a weakened prompt made the *same* model **leak PII on 50% of probes** and slip below the hallucination, reproducibility, and robustness gates — the harness catches real, prompt-induced risk *without* false-alarming a good model.
- Nine checks (133 items) with declared thresholds and champion-vs-challenger benchmarking; deterministic value-based scoring that runs with no API key, or against a live model via `USE_LLM=1`.

### [Credit-Decision PD Model — a governed, AI-augmented ML workflow](https://github.com/Nicole-Tu97/credit-risk-ml-sample)
`Python · scikit-learn · SHAP · LLM`

An end-to-end probability-of-default model built with the validation, fairness checks, SHAP explainability, failure-mode analysis, LLM adverse-action layer, and up-front governance a credit-risk function actually needs. Public UCI data, nothing proprietary.

| Model | AUC | Gini | KS | Brier | PSI |
|---|--:|--:|--:|--:|--:|
| Logistic regression (baseline) | 0.754 | 0.509 | 0.397 | 0.192 | 0.001 |
| **HistGradientBoosting + isotonic (champion)** | **0.784** | **0.569** | **0.429** | **0.134** | **0.001** |

- Leakage-safe feature engineering (23 → 36 features), CV-tuned, isotonic-calibrated — 5-fold CV AUC **0.787** ≈ test **0.784** (small train–test gap): a *validated* result, not an overfit one.
- Fairness across sex / age / education · SHAP explainability · documented failure modes.
- LLM adverse-action layer constrained to the model's **real** risk drivers; governance mapped to **OSFI E-23** and **FCAC**.

## 💼 Experience

**Quantitative Researcher, Data Science · Deepcoin** · 2024 – Present
- Built market-neutral systematic strategies end to end (research, backtesting, live trading), including a ~$2M basis-arbitrage book at **2.93 Sharpe** with 0.88% max drawdown, plus on-chain rate-derivative and prediction-market strategies.
- Owned the ML defense layer of a live ETH/USDT market-making system: trained and deployed directional-drift, order-cancellation, and spread-widening classifiers (**0.81–0.84 AUC**; 84.9% capture of toxic flow).
- Built the surrounding real-time infrastructure (data pipelines, backtesting framework, risk controls, P&L and exposure monitoring) and an **LLM-driven correlation-mining engine** over ~2,000 markets (~98× speedup).

**Quantitative Analyst, Data Science · CITIC Securities** · 2020 – 2023
- Engineered hundreds of alpha factors (momentum, reversal, volatility, liquidity, order-flow) across the A-share universe, and ran factor mining end to end — IC/IR, turnover, decay, orthogonalization — into a reusable factor library.
- Built **factor-combination models (XGBoost, logistic/linear regression)** to predict short-horizon cross-sectional returns.
- Built large-scale market-data pipelines (price/volume, fundamentals, tick/order-book) with automated data-quality checks, and presented factor research to portfolio managers to support allocation decisions.

## 🎓 Education
- **MSc, Data Science** — University of British Columbia · 2023–2024
- **BSc, Mathematics & Economics** — Boston University · 2016–2020

## 📫 Contact
- 📧 [yejun.tu1202@gmail.com](mailto:yejun.tu1202@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/yejun-tu-453b7414b/)
- 📍 Vancouver, BC — open to Vancouver / Toronto / remote
