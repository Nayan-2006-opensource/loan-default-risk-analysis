# Loan Default Risk Analysis

## 📌 Project Overview

This project focuses on analyzing personal loan data to understand the factors associated with loan default risk.

The project covers the complete data analytics process starting from data assessment and cleaning to exploratory data analysis and identification of important patterns in the dataset.

Machine Learning modeling and dashboard development are planned as the next stages of the project.

---

## 🎯 Objectives

- Understand the structure and quality of the dataset
- Perform data assessment and cleaning
- Handle missing and invalid values
- Perform univariate analysis
- Perform bivariate analysis
- Identify patterns related to loan defaults
- Generate meaningful insights from the data

---

## 📊 Dataset

The dataset contains information about personal loan applicants, including:

- Age
- Gender
- Marital Status
- City Tier
- State
- Employment Type
- Bank Account Vintage
- Monthly Income
- Existing Loans
- Existing EMI
- Credit Utilization
- Credit Inquiries
- Late Payments
- Loan Amount
- Loan Tenure
- Loan Purpose
- Collateral
- CIBIL Score
- Interest Rate
- Default Risk Score
- Default Flag

### Dataset Size

- Original dataset: 25,000 rows
- Final cleaned dataset: 24,493 rows
- Total columns: 22

---

## 🧹 Data Cleaning

The dataset was assessed for:

- Missing values
- Invalid values
- Logical inconsistencies
- Potential statistical outliers
- Incorrect or inconsistent data

### Major Cleaning Steps

- Missing values in `num_credit_inquiries_last_6m` were handled using the median.
- Missing values in `existing_emi_monthly_inr` were handled appropriately.
- Customers with `existing_loans_count = 0` were assigned an existing EMI of `0`.
- Records where `age < bank_account_vintage_years` were removed because they were logically invalid.
- Statistical outliers were investigated but were not automatically removed when they appeared to be potentially valid observations.

Final cleaned dataset:

```text
Rows: 24,493
Columns: 22


📈 Exploratory Data Analysis
1. Univariate Analysis

Univariate analysis was performed on numerical and categorical variables to understand their individual distributions and characteristics.

The analysis included:

Mean
Median
Minimum and maximum values
Quartiles
Standard deviation
Skewness
Distribution plots
Boxplots
Frequency analysis
2. Bivariate Analysis

Bivariate analysis was performed to understand relationships between two variables.

Numerical × Numerical

The following relationships were analyzed:

Monthly Income vs Loan Amount
CIBIL Score vs Interest Rate
CIBIL Score vs Late Payments
Monthly Income vs Existing EMI
Existing Loans vs Existing EMI
Credit Utilization vs CIBIL Score
Loan Amount vs Loan Tenure
Monthly Income vs Existing Loans

Scatter plots and correlation were used to study these relationships.

Categorical × Default

The following relationships were analyzed:

Employment Type vs Default
Loan Purpose vs Default
Collateral Provided vs Default
Numerical × Default

The following relationships were analyzed:

Age vs Default
CIBIL Score vs Default
Late Payments vs Default
Credit Utilization vs Default
Existing Loans vs Default
Monthly Income vs Default
Loan Amount vs Default
Interest Rate vs Default
Default Risk Score vs Default

Boxplots and group-wise statistical summaries were used for comparison.

🔍 Key Findings
CIBIL Score vs Default

Customers with CIBIL scores below 500 had a default rate of approximately 42.6%, while customers with CIBIL scores above 770 had a default rate of 0% in this dataset.

This shows a strong association between CIBIL score and loan default.

Late Payments vs Default

The average number of late payments was:

Non-defaulted customers: 1.37
Defaulted customers: 2.64

The median was:

Non-defaulted customers: 1
Defaulted customers: 2

This shows a noticeable association between late payments and default.

Existing Loans vs Default

The average number of existing loans was:

Defaulted customers: 1.433
Non-defaulted customers: 1.08

Both groups had a median of 1 and an observed range of 0–6.

The difference between the two groups was relatively small.

Age vs Default

The average age was:

Defaulted customers: 34.89 years
Non-defaulted customers: 35.34 years

The age distributions of the two groups were quite similar.

Employment Type vs Default

Default rates across employment types were:

Business Owner: 7.36%
Salaried - Government: 6.72%
Salaried - PSU: 5.62%
Salaried - Private: 5.83%
Self-Employed Professional: 5.50%
Loan Purpose vs Default

Default rates across loan purposes were relatively close, ranging from approximately 5.60% to 6.54%.

Collateral vs Default

Default rates were:

Without collateral: 6.83%
With collateral: 3.59%

This indicates an observed association between collateral status and default in the dataset.

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook



Loan Default Risk Project/
│
├── data/
│   ├── Raw_Dataset.csv
│   └── Cleaned_Dataset.csv
│
├── notebooks/
│   ├── Data_Cleaning.ipynb
│   └── Loan_EDA.ipynb
│
├── visuals/
│   ├── univariate/
│   ├── bivariate/
│   └── multivariate/
│
├── README.md
└── requirements.txt




▶️ How to Run

Clone the repository:

git clone <repository-url>
cd <repository-folder>

Install the required libraries:

pip install -r requirements.txt

Run Jupyter Notebook:

jupyter notebook


🚧 Project Status
Completed
 Data Assessment
 Data Cleaning
 Univariate Analysis
 Numerical × Numerical Bivariate Analysis
 Categorical × Default Bivariate Analysis
 Numerical × Default Bivariate Analysis
 Key Findings
Upcoming
 Machine Learning Modeling
 Model Evaluation
 Model Comparison
 Interactive Dashboard
🚀 Future Scope
Machine Learning

The next stage of the project will focus on building machine learning classification models to predict loan default.

This will include:

Feature preparation
Train-test split
Model training
Model evaluation
Model comparison
Feature importance and interpretation
Dashboard

An interactive dashboard will be developed to visualize:

Default rates
Customer demographics
Credit score patterns
Loan characteristics
Financial behavior
Important risk-related insights
👤 Author

Nayan Samadhiya

Aspiring AI/ML Engineer | Data Analytics