<div align="center">

# 🏦 Customer Churn Intelligence in Banking

### DVA Capstone 2 — Data Visualization & Analytics | Newton School of Technology (RU)

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Tableau](https://img.shields.io/badge/Tableau-Public-E97627?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Sector](https://img.shields.io/badge/Sector-Banking%20%26%20Financial%20Services-22c55e?style=for-the-badge)]()

---

**Section A · Group 9 · Submission Date: 29 April 2026**

</div>

---

## 👥 Team Members

| Name | Student ID | Contribution | Resume | Portfolio |
|---|---|---|---|---|
| Lakshya Bapna | 2401010252 | Dataset Sourcing, ETL & Cleaning, Tableau Dashboard | — | — |
| Aarya Srivastava | 2401010008 | EDA & Analysis, Tableau Dashboard | [Resume](./DVA-focused-Resume/Aarya-Resume/Aarya_Srivastava_Resume.pdf) | [Portfolio](https://aarya-sr.github.io/Portfolio_DVA/) |
| Mayank Yadav | 2401010271 | EDA & Analysis, PPT & Viva | — | — |
| Sarvjeet Yadav | 2401010424 | EDA & Analysis, PPT & Viva | — | — |
| Omkar Hadole | 2401010175 | Tableau Dashboard, PPT & Viva | [Resume](./DVA-focused-Resume/Omkar%20Hadole/omkar-hadole_resume.pdf) | [Portfolio](https://omkar-dva-portfolio.vercel.app/) |
| Debasish Karan | 2401010141 | Statistical Analysis, PPT & Viva | — | — |

**Faculty Mentor:** Satyaki Das
**Team ID:** Group 9

---

## 📌 Problem Statement

> *"What key customer behavioural and financial factors influence churn in a banking system, and how can high-risk customers be identified early enough for effective retention intervention?"*

Customer churn is a major concern in the banking sector as it directly impacts revenue and long-term customer value. Banks lose substantial income when customers close accounts and switch to competitors — and the cost of acquiring a replacement customer far exceeds that of retaining an existing one.

This project addresses the challenge of **identifying the key behavioural and financial factors that drive churn**, enabling early intervention before customers leave.

---

## 🎯 Objectives

1. Identify the primary drivers of customer churn through structured exploratory analysis.
2. Segment customers by risk level to prioritize retention resources.
3. Analyze the financial behavior patterns of churned vs. retained customers.
4. Build interactive Tableau dashboards that enable non-technical stakeholders to explore churn trends dynamically.

---

## 💡 Solution

The project delivered an end-to-end descriptive and diagnostic analytics pipeline:

1. **Data Ingestion & ETL** — A customer-level banking dataset of ~28,000 records was sourced, cleaned, and preprocessed using Python.
2. **KPI Engineering** — Derived KPIs including Churn Rate, Active Rate, Average Balance, and Balance Change were computed from raw fields.
3. **Exploratory Data Analysis (EDA)** — Patterns across activity status, tenure, balance trends, and risk segments were uncovered through structured visual and statistical analysis.
4. **Statistical Validation** — Hypothesis testing (chi-square), correlation analysis (point-biserial), distribution analysis, and anomaly detection were applied to validate findings.
5. **Interactive Dashboards** — Three Tableau dashboards translate analytical findings into accessible, decision-ready tools for non-technical stakeholders.

### 🔑 Key Insights

- 🔴 **Inactive customers** churn at rates significantly above the overall average — inactivity is the single most reliable leading indicator of churn.
- 🟠 **New customers (0–2 year tenure)** have the highest churn probability; the first two years are the critical retention window.
- 🟡 **Declining account balances** reliably precede customer churn — balance trajectory is an actionable early-warning signal.
- 🔵 **High-risk segment customers** exhibit disproportionately higher churn rates; risk classification is a valid targeting criterion for retention investment.
- 🟢 Customers with **both inactive status and low balance** represent a concentrated, immediately actionable churn-risk cluster.

### ✅ Key Recommendations

| # | Recommendation | Estimated Churn Reduction |
|---|---|---|
| 1 | Deploy early engagement campaigns for new customers (0–2 yr) with 30/60/90-day onboarding touchpoints | 10–20% of early-stage churn |
| 2 | Implement automated balance-decline alerts (>20% drop over 60 days) for proactive outreach | 5–15% of balance-driven churn |
| 3 | Launch reactivation programs for customers inactive for 60+ days | 8–15% reactivation rate |
| 4 | Develop personalized retention plans for high-risk segments | 15–25% of high-risk churn |
| 5 | Create occupation-specific financial products to reduce financial stress-driven exits | 5–10% in targeted segments |

---

## 🛠️ Tech Stack & Tools Used

| Category | Tools / Libraries |
|---|---|
| **Language** | Python 3.10+ |
| **Data Processing** | Pandas, NumPy |
| **Statistical Analysis** | SciPy (chi-square, point-biserial correlation) |
| **Visualization (Python)** | Matplotlib, Seaborn |
| **Business Intelligence** | Tableau Public |
| **Notebooks** | Jupyter Notebook |
| **ETL Pipeline** | Custom Python script (`scripts/etl_pipeline.py`) |
| **Version Control** | Git & GitHub |
| **Outlier Handling** | IQR-based winsorization (capped at 1st/99th percentile) |
| **Missing Value Strategy** | Median (numeric) / Mode (categorical) imputation |

---

## 📊 Tableau Dashboards

Three interactive dashboards were designed, each serving a distinct business question:

| Dashboard | Business Question | Key Visualizations |
|---|---|---|
| **1. Behavior Analysis** | *Why are customers churning?* | Activity vs. Churn, Tenure vs. Churn (cohort), Balance Decline Analysis |
| **2. Customer Segmentation** | *Who is at risk?* | Risk Segmentation Breakdown, Age Group Heatmap, Occupation Breakdown |
| **3. Customer Value & Balance** | *What is the financial impact?* | Balance Distribution, Balance Change Analysis, Avg Balance by Segment |

> 🔗 Dashboard links are documented in [`tableau/dashboard_links.md`](./tableau/dashboard_links.md)

---

## 📁 Project Structure

```
SectionA_G9_Customer_Churn_Intelligence/
│
├── 📂 data/
│   ├── raw/                        # Original unprocessed dataset
│   └── processed/                  # Cleaned & feature-engineered data
│
├── 📂 notebooks/
│   ├── 01_extraction.ipynb         # Data sourcing & initial load
│   ├── 02_cleaning.ipynb           # Data cleaning & standardisation
│   ├── 03_eda.ipynb                # Exploratory Data Analysis
│   ├── 04_statistical_analysis.ipynb  # Hypothesis testing & correlations
│   └── 05_final_load_prep.ipynb    # Final export for Tableau
│
├── 📂 scripts/
│   └── etl_pipeline.py             # End-to-end ETL pipeline script
│
├── 📂 tableau/
│   └── dashboard_links.md          # Tableau Public dashboard URLs
│
├── 📂 docs/
│   └── data_dictionary.md          # Field definitions & metadata
│
├── 📂 reports/
│   ├── DVA_Capstone2_Report_Condensed.pdf   # Final project report
│   ├── presentation.pdf            # Project presentation slides
│   ├── project_report.pdf          # Full detailed report
│   └── kpi_summary.csv             # KPI summary output
│
├── 📂 DVA-focused-Portfolio/       # Portfolio artifacts
├── 📂 DVA-focused-Resume/          # Resume artifacts
│
└── README.md
```

---

## 📈 Dataset Overview

| Attribute | Detail |
|---|---|
| **Records** | ~28,000 customer-level rows |
| **Sector** | Banking & Financial Services |
| **Target Variable** | `Churn Label` (Binary: 1 = Churned, 0 = Retained) |

### Key Features

| Field | Type | Description |
|---|---|---|
| `Churn Label` | Binary | 1 = Churned, 0 = Retained |
| `Activity Status` | Categorical | Active / Inactive based on recent transactions |
| `Tenure (Years)` | Numeric | Years the customer has held an account |
| `Account Balance` | Numeric | Current or average account balance in currency units |
| `Risk Segment` | Categorical | Customer risk classification (Low / Medium / High) |
| `Age` | Numeric | Customer age in years |
| `Occupation` | Categorical | Customer's reported occupation category |
| `Gender` | Categorical | Customer's gender |

---

## 🔬 Analytics Pipeline

```
Raw Data
   │
   ▼
01_extraction.ipynb       ← Source & load dataset
   │
   ▼
02_cleaning.ipynb         ← Missing values, outliers, standardisation
   │
   ▼
03_eda.ipynb              ← Visual patterns, distributions, segment analysis
   │
   ▼
04_statistical_analysis.ipynb   ← Chi-square, correlation, anomaly detection
   │
   ▼
05_final_load_prep.ipynb  ← Export clean data for Tableau
   │
   ▼
Tableau Dashboards        ← Interactive decision-support tools
```

### Cleaning Steps Applied

- Churn labels standardised to binary integer format (1 = Churned, 0 = Retained)
- Activity Status values normalised to consistent categorical encoding (Active / Inactive)
- Date fields converted to datetime format for tenure computation
- Categorical columns stripped of whitespace and converted to title case
- Missing values imputed using **median** (numeric) or **mode** (categorical) strategies
- Rows with missing churn labels were excluded from analysis to preserve integrity
- Numeric fields (Balance, Age, Tenure) assessed via **IQR-based outlier detection** and capped at 1st/99th percentiles (winsorization)

### Feature Engineering

| Derived Feature | Description |
|---|---|
| **Churn Rate** | Proportion of churned customers within each segment or cohort |
| **Activity Status Flag** | Derived binary field used for segmentation analysis |
| **Balance Difference** | Delta between opening and closing balance — proxy for financial trajectory |
| **Tenure Band** | Customers grouped into cohorts: 0–2 yrs, 3–5 yrs, 6–10 yrs, 10+ yrs |

---

## 📐 Project Scope

| In Scope | Out of Scope |
|---|---|
| Descriptive & diagnostic analytics | Real-time data pipelines |
| KPI computation | Live CRM integration |
| Exploratory Data Analysis (EDA) | ML-based churn prediction models *(future scope)* |
| Tableau dashboard development | Time-series micro-level tracking |

---

## 🎯 Success Criteria

- ✅ Clear, evidence-based identification of the top churn drivers
- ✅ Actionable insights that map directly to retention strategies
- ✅ Three fully functional, publicly accessible Tableau dashboards with interactive filters

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### Running the Notebooks
```bash
# Clone the repository
git clone https://github.com/lakshyabapna/SectionA_G9_Customer_Churn_Intelligence.git
cd SectionA_G9_Customer_Churn_Intelligence

# Launch Jupyter
jupyter notebook

# Run notebooks in order:
# 01_extraction → 02_cleaning → 03_eda → 04_statistical_analysis → 05_final_load_prep
```

### Running the ETL Pipeline
```bash
python scripts/etl_pipeline.py
```

---

## 📋 Contribution Matrix

| Team Member | Dataset & Sourcing | ETL & Cleaning | EDA & Analysis | Statistical Analysis | Tableau Dashboard | PPT & Viva |
|---|:-:|:-:|:-:|:-:|:-:|:-:|
| Lakshya Bapna (2401010252) | ✓ | ✓ | | | ✓ | |
| Aarya Srivastava (2401010008) | | | ✓ | | ✓ | |
| Mayank Yadav (2401010271) | | | ✓ | | | ✓ |
| Sarvjeet Yadav (2401010424) | | | ✓ | | | ✓ |
| Omkar Hadole (2401010175) | | | | | ✓ | ✓ |
| Debasish Karan (2401010141) | | | | ✓ | | ✓ |

> *Contributions are verifiable through GitHub Insights, PR history, and submitted deliverables.*

---

## 📜 License

This project was developed as part of the **DVA Capstone 2** coursework at **Newton School of Technology (RU)**. All rights reserved by the team and the institution.

---

<div align="center">

Made with ❤️ by **Group 9 — Section A**
Newton School of Technology · Data Visualization & Analytics · SEM IV

</div>
