# Loan Default Risk Analysis

## 📌 Project Overview

This project analyzes personal loan data from Indian borrowers to identify patterns and factors associated with loan default risk.

It follows an end-to-end data analytics workflow — from raw data assessment and cleaning to exploratory data analysis and business insights — built on a dataset of 25,000 personal loan applicants.

---

## 🎯 Project Objective

To analyze personal loan applicant data and identify the customer, financial, and credit behavior factors most associated with a higher risk of loan default.

---

## 📊 Dataset

The dataset contains 25,000 rows and 22 columns covering applicant demographics, employment and banking history, credit behavior, loan details, and default outcomes.

Raw dataset: `data/india_personal_loan_default_risk_2026.csv`
Cleaned dataset: `data/Cleaned_Dataset.csv`

---

## 🔄 Project Workflow

```text
Raw Data
   ↓
Data Assessment
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis (Univariate)
   ↓
Exploratory Data Analysis (Bivariate) — in progress
   ↓
Data Visualization
   ↓
Insights & Recommendations
```

---

## 📂 Project Structure

```text
loan-default-risk-analysis/
│
├── data/
│   ├── india_personal_loan_default_risk_2026.csv
│   └── Cleaned_Dataset.csv
│
├── notebooks/
│   ├── 01_data_assessment.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_univariate_analysis.ipynb
│
├── visuals/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🔍 Key Findings So Far

**Data Quality**
- Found and fixed 7,920 rows where `existing_loans_count = 0` but a non-zero EMI was recorded — a logical inconsistency, corrected to 0.
- Removed 7 rows where customer age was less than their bank account vintage — physically impossible.
- Filled missing values in `bank_account_vintage_years`, `existing_emi_monthly_inr`, and `num_credit_inquiries_last_6m` using median imputation, chosen based on distribution skew.
- Final cleaned dataset: 24,493 rows × 22 columns (507 rows dropped/corrected).

**Applicant Profile**
- 59.7% of applicants are male, 38.4% female, 1.9% other.
- 58.2% are married; single applicants make up 31.7%.
- Tier 1 and Tier 2 cities account for nearly 78% of applicants combined.
- Gujarat has the highest share of applicants (7%); all other states cluster tightly around 6.4–6.5%.

**Loan Behavior**
- Personal expenses are the top loan purpose (22.4%), followed by wedding expenses (13.9%) — notably higher than education loans (9.8%), pointing to significant financial pressure around wedding costs.
- 78.2% of applicants did not provide collateral.
- Only 6.1% of applicants defaulted, versus 93.9% who did not — a significant class imbalance that will need to be handled (e.g. SMOTE, class weighting) at the modeling stage.

---

## 🛠️ Tools and Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## ▶️ How to Run

```bash
git clone <repo-url>
cd loan-default-risk-analysis
pip install -r requirements.txt
jupyter notebook
```

Run the notebooks in order: `01_data_assessment.ipynb` → `02_data_cleaning.ipynb` → `03_univariate_analysis.ipynb`.

---

## 🚧 Project Status

**In progress** — data assessment, cleaning, and univariate EDA are complete. Bivariate/multivariate analysis and predictive modeling are next.

---

## 📋 Roadmap

* [x] Data Assessment
* [x] Data Cleaning
* [x] Univariate Exploratory Data Analysis
* [ ] Bivariate / Multivariate Analysis
* [ ] Predictive Modeling (default risk classification)
* [ ] Data Visualization Dashboard
* [ ] Business Insights & Recommendations

---

## 👤 Author

**Nayan Samadhiya**