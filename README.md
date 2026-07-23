# Hi, I'm Yejun (Nicole) Tu 👋

**Data Scientist · Machine Learning in Finance**

Data scientist with ~5 years applying machine learning across the finance industry — turning data into models that drive **real business impact**. I'm genuinely passionate about data, machine learning, and **deep learning**: I love the full arc of a problem, from framing it to building, validating, and shipping a model that actually moves the needle. Lately I'm especially drawn to **reinforcement learning**, which I'm actively exploring.

📍 Vancouver, Canada · open to Toronto & remote

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)

## 🚀 What I do
- Build & validate **ML models end-to-end** — data → features → modeling → validation → deployment
- Apply ML across **financial problems**: credit & risk modeling, forecasting, and data-driven strategy
- Care about **impact and rigor** — models that are accurate, calibrated, fair, and defensible, not just built

## 🛠️ Skills
- **Languages** — Python, SQL, R, C++, Rust, Go, Java
- **ML / modeling** — scikit-learn, XGBoost, LightGBM, statsmodels, SciPy, SHAP, CVXPY, Numba, NumPy, pandas, Polars
- **Deep learning** — PyTorch, neural networks
- **Data** — PostgreSQL, MySQL, IBM Db2, Redshift, MongoDB · Matplotlib, Plotly, Jupyter
- **Focus areas** — predictive & risk modeling, model validation & governance, feature engineering, time-series, LLM/AI tooling
- **Currently exploring** — reinforcement learning (RL)
- **Certificates** — AWS Certified Cloud Practitioner · IBM Data Science Professional

## 📌 Featured Project

### [Credit-Decision PD Model — a governed, AI-augmented ML workflow](https://github.com/Nicole-Tu97/credit-risk-ml-sample)
`Python · scikit-learn · SHAP · LLM`

An end-to-end **probability-of-default** model built the way a real, defensible risk function should be — not just a classifier, but validation, fairness, explainability, failure-mode analysis, and an AI-augmented adverse-action layer, with governance documented up front. (Public UCI data — nothing proprietary.)

| Model | AUC | Gini | KS | Brier | PSI |
|---|--:|--:|--:|--:|--:|
| Logistic regression (baseline) | 0.754 | 0.509 | 0.397 | 0.192 | 0.001 |
| **HistGradientBoosting + isotonic (champion)** | **0.784** | **0.569** | **0.429** | **0.134** | **0.001** |

- Leakage-safe feature engineering (23 → 36 features), CV-tuned, isotonic-calibrated — 5-fold CV AUC **0.787** ≈ test **0.784** (small train–test gap): a *validated* result, not an overfit one.
- Fairness across sex / age / education · SHAP explainability · documented failure modes.
- LLM adverse-action layer constrained to the model's **real** risk drivers; governance mapped to **OSFI E-23** and **FCAC**.

## 💼 Experience

**Quantitative Researcher · Deepcoin** · 2024 – Present
- Built market-neutral systematic strategies end to end (research, backtesting, live trading), including a ~$2M basis-arbitrage book at **2.93 Sharpe** with 0.88% max drawdown, plus on-chain rate-derivative and prediction-market strategies.
- Owned the ML defense layer of a live ETH/USDT market-making system: trained and deployed directional-drift, order-cancellation, and spread-widening classifiers (**0.81–0.84 AUC**; 84.9% capture of toxic flow).
- Built the surrounding real-time infrastructure (data pipelines, backtesting framework, risk controls, P&L and exposure monitoring) and an **LLM-driven correlation-mining engine** over ~2,000 markets (~98× speedup).

**Quantitative Analyst · CITIC Securities** · 2020 – 2023
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

*Passionate about data, machine learning, and building models that make a real impact in finance.*
