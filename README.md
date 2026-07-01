# Banking Risk Analytics 

Analyzing banking customer data to understand risk profiles, income patterns, loyalty segments, and financial behavior — helping banks minimize lending risk and make smarter credit decisions.

---

## Brief Summary

An end-to-end risk analytics project on a banking customer dataset — involving data cleaning, encoding, univariate & bivariate analysis using Python, and an interactive Power BI dashboard — to answer: "How can data be used to minimise the risk of losing money while lending to customers?"

---

## Overview

This project develops a foundational understanding of risk analytics in banking and financial services. It explores how customer demographics, income levels, credit card usage, loan balances, loyalty classification, and financial account behavior relate to risk weighting — enabling banks to identify high-risk customers before approving credit or loans.

---

## Problem Statement

Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

---

## Dataset

|Column | Description |
|-------|-------------|
| client_id | Unique identifier for each customer |
| age | Age of the client in years |
| genderid | Gender (Male, Female) |
| brid | Business region (Retail, Institutional, Private Bank, Commercial) |
| estimated_income | Estimated annual income of the client |
| superannuation_savings | Superannuation/retirement savings balance |
| credit_card_balance | Outstanding credit card balance |
| bank_loans | Total bank loans held |
| bank_deposits | Total deposits with the bank |
| checking_accounts | Checking account balance |
| saving_accounts | Savings account balance |
| foreign_currency_account | Foreign currency account balance |
| business_lending | Business lending amount |
| amount_of_credit_cards | Number of credit cards held |
|fee_structure | Fee tier assigned to the customer |
| loyalty_classification | Customer loyalty segment |
| properties_owned | Number of properties owned |
| risk_weighting | Target variable — customer risk level |
| nationality | Client nationality |
| occupation | Client occupation |
| joined_bank | Date the client joined the bank |
| iaid | Investment advisor ID |
| income_band | Engineered — Low / Mid / High income group |

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Jupyter Notebook) | Data cleaning, EDA & visualization |
| Pandas / NumPy | Data manipulation & feature engineering |
| Matplotlib / Seaborn | Visualizations (countplots, KDE plots, heatmaps) |
| Power BI | Interactive dashboard & reporting |

---

## Methods

| Step | Description |
|------|-------------|
| Initial Inspection | Checked shape, data types, null values, and duplicates |
| Data Cleaning & Encoding | Converted joined_bank to datetime, standardized column names to lowercase, mapped genderid (Male/Female) and brid (Retail/Institutional/Private Bank/Commercial), created working copy df_new |
| Feature Engineering | Created income_band by bucketing estimated_income into Low (< 100K), Mid (100K–300K), High (> 300K) |
| Univariate Analysis | Avg risk by income band (bar chart), countplots for all categorical columns, histograms for all numerical columns |
| Bivariate Analysis | Cross-tabulation of categorical columns vs risk_weighting (stacked bar charts), KDE plots of numerical columns split by risk_weighting |
| Correlation Heatmap | Computed and visualized correlation matrix for all numerical financial variables |

---

## Key Insights

1. Income band significantly influences risk — higher income customers tend to have lower average risk weighting, while low-income customers show elevated risk profiles.
2. Bank deposits show strong positive correlation with both checking and saving accounts — customers with higher balances also tend to have higher total deposits.
3. Credit card balance and bank loans show different KDE distributions across risk levels — higher balances are associated with higher risk weighting.
4. Business region (brid) reveals different risk concentrations — commercial and institutional segments behave differently from retail customers.
5. Loyalty classification is a meaningful segment — loyal customers tend to exhibit lower risk profiles compared to newer or less engaged customers.
6. Properties owned acts as a proxy for financial stability — customers owning more properties tend to be lower risk.
7. Gender distribution across risk categories shows nuanced patterns worth monitoring in lending policy.
8. Superannuation savings show that customers with higher retirement savings tend to cluster in lower risk bands — indicating overall financial health.   

---

## Dashboard 

The Power BI dashboard is organized into 3 pages:

Page 1 — Risk Analysis

| Section | Details |
|---------|---------|
| KPI Cards | Total Clients · Total Loans · Total Deposit · Checking Accounts · Saving Accounts. |
| Clients by Risk Weighting | Bar chart showing client count across risk levels 1–5 (Risk 2 has highest clients ~1000) |
| Clients by Income Band | Donut chart — Mid (50.32%) · Low (34.37%) · High (15.31%) |
| Clients by Loyalty Classification | Donut chart — Jade (44.23%) · Gold (25.59%) · Silver (19.55%) · Platinum (10.63%) |
| Slicers | Nationality (African, American, Asian, Australian, European) · Gender (Male, Female) |


Page 2 — Loan Analysis

| Section | Details |
|---------|---------|
| Bank Loan by Nation | Bar chart — European leads (~0.8bn) · Asian · American · Australian · African |
| Bank Loan by BR | Bar chart — Private Bank leads (~1.0bn) · Retail · Commercial · Institutional |
| Bank Loan by Occupation | Top 10 occupations by loan amount — Account Coordinator & Database Admin lead (~15–20M each) |
| Bank Loan by Income Band | Donut chart — Mid (53.12%) · Low (25.26%) · High (21.61%) |
| Slicers | Nationality · Gender |


Page 3 — Deposit Analysis

| Section | Details |
|---------|---------|
| Bank Deposit by Nation | Bar chart — European leads (~1.0bn) · Asian · American · Australian · African |
| Bank Deposit by BR | Bar chart — Private Bank leads (~0.8bn) · Retail · Commercial · Institutional |
| Bank Deposit by Occupation | Top 10 occupations by deposit — Structural Analyst & Database Admin lead (~20M each) |
| Bank Deposit by Income Band | Donut chart — Mid (54.17%) · Low (24.79%) · High (21.05%) | 
| Slicers | Nationality · Gender |

---

## Results & Conclusion

The analysis reveals that income level, credit card balance, bank loans, and loyalty classification are the strongest indicators of customer risk in this dataset. Customers in the low-income band with high credit card balances and outstanding loans represent the highest lending risk. Conversely, high-income customers with strong deposit behaviors and property ownership are significantly lower risk. These insights provide a data-driven foundation for building risk scoring models and improving credit approval policies.

---

## Author & Contact

| Field | Info |
|-------|------|
| Name | (Your Name) |
| LinkedIn | https://www.linkedin.com/in/krishna-krishna-26a106231/ |
| GitHub |https://github.com/ |
