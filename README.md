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

## 📌 Featured Project

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

**Quantitative Analyst · CITIC Securities** · 2020 – 2023


## 🎓 Education
- **MSc, Data Science** — University of British Columbia · 2023–2024
- **BSc, Mathematics & Economics** — Boston University · 2016–2020

## 📫 Contact
- 📧 [yejun.tu1202@gmail.com](mailto:yejun.tu1202@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/yejun-tu-453b7414b/)
- 📍 Vancouver, BC — open to Vancouver / Toronto / remote
