# 📊 Data Dictionary

## Banking Customer Churn Dataset

This document describes all variables used in the Banking Customer Churn Analysis project. The dataset contains customer demographic, financial, and behavioral information used to analyze churn patterns.

---

## 🧾 Dataset Overview
- **Total Records:** ~28,000 customers  
- **Type:** Structured tabular data  
- **Domain:** Banking / Financial Services  

---

## 📌 Column Descriptions

| Column Name | Data Type | Description | Example |
|------------|----------|-------------|---------|
| age | Integer | Age of the customer in years | 45 |
| gender | Categorical | Gender of the customer | Male / Female |
| dependents | Integer | Number of dependents linked to the customer | 0, 2 |
| occupation | Categorical | Employment category of customer | salaried, self_employed |
| customer_nw_category | Integer | Net worth / customer value segment | 1, 2, 3 |
| current_balance | Float | Current account balance | 5400.75 |
| previous_month_end_balance | Float | Balance at the end of previous month | 5100.30 |
| average_monthly_balance_prevQ | Float | Average monthly balance in previous quarter | 4900.20 |
| average_monthly_balance_prevQ2 | Float | Average monthly balance in quarter before previous quarter | 4700.80 |
| current_month_credit | Float | Total credit amount in current month | 1200.50 |
| previous_month_credit | Float | Total credit amount in previous month | 950.40 |
| current_month_debit | Float | Total debit amount in current month | 700.00 |
| previous_month_debit | Float | Total debit amount in previous month | 680.00 |
| current_month_balance | Float | Average balance during current month | 5200.25 |
| previous_month_balance | Float | Average balance during previous month | 5050.90 |
| churn | Integer | Target variable indicating churn status | 0 / 1 |
| last_transaction | Date | Date of most recent transaction | 2019-08-15 |
| customer_tenure_years | Float | Customer relationship duration in years (derived) | 6.28 |

---

## 🧠 Encoded Variables

### churn

| Value | Meaning |
|------|--------|
| 0 | Retained Customer |
| 1 | Churned Customer |

---

### customer_nw_category

| Value | Meaning |
|------|--------|
| 1 | Low Net Worth |
| 2 | Medium Net Worth |
| 3 | High Net Worth |

---

## 🛠️ Derived Features

The following features were created during preprocessing and feature engineering:

- **customer_tenure_years**  
  → Derived from vintage (converted from days to years)

- **balance_diff** *(if used in your project)*  
  → Difference between current and previous balance to capture financial trend

- **is_active** *(if used)*  
  → Derived based on recent transaction activity

- **age_group** *(if used)*  
  → Categorized age ranges for segmentation

- **risk_segment** *(if used)*  
  → Derived using behavioral and financial indicators to classify customers into risk categories

---

## 🧹 Removed Columns During Cleaning

| Column | Reason |
|--------|--------|
| customer_id | Identifier only (not useful for analysis) |
| city | Synthetic / not relevant to analysis |
| branch_code | Synthetic / not relevant to analysis |

---

## 📌 Notes

- The dataset was cleaned to remove inconsistencies and missing values  
- Derived features were created to improve analysis and interpretability  
- Data is used for churn analysis, segmentation, and dashboard visualization  

---

## 🚀 Usage

This dataset is used for:
- Exploratory Data Analysis (EDA)  
- Customer behavior analysis  
- Churn pattern identification  
- Tableau dashboard development  