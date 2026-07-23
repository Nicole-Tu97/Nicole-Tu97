# Hi, I'm Yejun (Nicole) Tu 👋

**Machine Learning & Data Science in Finance**

Data scientist with ~5 years applying machine learning across the finance industry — turning data into models that drive **real business impact**. I'm genuinely passionate about data, data science, and ML: I love the full arc of a problem — framing it, building and validating the model, and making sure it holds up in production and actually moves the needle.

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
- **Languages** — Python, SQL, R, C++
- **ML / modeling** — scikit-learn, XGBoost, LightGBM, PyTorch, SHAP, statsmodels, CVXPY, NumPy, pandas, Polars
- **Data** — PostgreSQL, MySQL, Redshift, MongoDB · Matplotlib, Plotly, Jupyter
- **Focus areas** — predictive & risk modeling, model validation & governance, feature engineering, time-series, LLM/AI tooling
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

## 💼 Experience — 5 years of ML in finance

**Deepcoin** · Machine Learning / Quantitative Research · 2024 – Present
- Built and validated **ML models that drive live decisions** (predictive classifiers, 0.81–0.84 AUC) and the risk-control, monitoring, and data pipelines around them; built **LLM / agentic analytical tooling**.
- Developed **data-driven strategies delivering measurable, risk-managed impact** — e.g., a live book at a **2.93 Sharpe with <1% drawdown**.

**CITIC Securities** · Data Science / Quantitative Analysis · 2020 – 2023
- Built hundreds of predictive features and **ML models (XGBoost)** for equity return prediction across the A-share market, with end-to-end validation (IC/IR, decay) and a reusable modeling framework.
- Built large market-data pipelines in **SQL & pandas** and presented model-driven insights to portfolio managers to inform decisions.

## 🎓 Education
- **MSc, Data Science** — University of British Columbia · 2023–2024
- **BSc, Mathematics & Economics** — Boston University · 2016–2020

## 📫 Contact
- 📧 [yejun.tu1202@gmail.com](mailto:yejun.tu1202@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/yejun-tu-453b7414b/)
- 📍 Vancouver, BC — open to Vancouver / Toronto / remote

*Passionate about data, machine learning, and building models that make a real impact in finance.*
