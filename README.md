# Project5_ClimateHazardRisk-on-Smallbusiness-Loan
# 🌍 Climate Hazard Risk Analysis for SBA 7(a) Loan Portfolio

## 📋 Project Overview

This project investigates the impact of **climate hazard risk** on credit risk within the U.S. **Small Business Administration’s (SBA) 7(a) loan program**. Using FEMA’s **National Risk Index for Natural Hazards** and historical loan data from the SBA, we aim to determine whether climate-related hazards influence loan performance, particularly in the form of interest rates and loan loss ratios.

---

## 🧠 Key Objectives

- Assess historical and future **exposure of the SBA’s 7(a) portfolio to climate hazards**
- Evaluate if **climate hazard risk contributes to loan risk**
- Integrate **climate and loan datasets** at the county level using FIPS codes
- Build **machine learning models** to quantify the relationship between hazard exposure and credit risk

---

## 🗂️ Data Sources

- **SBA 7(a) Loan Program Data (1991–2019)**  
  [SBA FOIA Portal](https://data.sba.gov/dataset/7-a-504-foia)
- **Climate Hazard Data** from FEMA’s National Risk Index  
  [FEMA National Risk Index](https://hazards.fema.gov/nri/data-resources)

---

## 🔍 Methodology

- **Data Cleaning:** Addressed missing values, merged multi-decade loan datasets, imputed missing interest rates using historical bank prime loan data.
- **Data Integration:** Joined loan and climate data using **state-county FIPS codes**
- **Credit Risk Metrics:** 
  - `InitialInterestRate` (proxy for perceived borrower risk)
  - `LoanLossRatio = GrossChargeOffAmount / GrossApprovalAmount`
- **Modeling Techniques:**
  - Regression models: Ridge, ElasticNet
  - Tree-based models: Random Forest, Gradient Boosting, XGBoost
- **Performance Metrics:** R² and RMSE

---

## 🔎 Key Findings

- Over **66% of the SBA 7(a) portfolio** is exposed to **moderate to very high climate hazard risk**
- **No significant linear or nonlinear relationship** was found between climate hazard risk scores and credit risk metrics
- **Temperature, flooding, and wildfires** are the most common hazards in high-risk regions like California, Texas, and Florida
- Areas with **higher hazard risk** do not consistently receive higher loan interest rates — indicating an underestimation of climate risk in credit pricing

---

## 📈 Visualizations

- Geospatial risk heatmaps created with Tableau show **loan exposure by county and risk level**
- Distribution charts reveal **portfolio concentration in high-risk states and regions**

---

## 💡 Recommendations

- Introduce **more granular climate data** (e.g., census tract level)
- Collect **time-series and financial data** on companies' revenue, cash flow, and losses post-hazard
- Consider **risk-adjusted interest rate models** for loans issued in high-risk counties
- Start with focused analysis on **Los Angeles County**, which shows the highest combined loan value and risk score

---

## ⚠️ Limitations

- Climate hazard data lacks **exact dates**, making causal inference difficult
- Loan data lacks **detailed borrower financial information**
- County-level aggregation may hide **micro-level exposure differences**

---

## 🧰 Tools & Technologies

- **Python** (data cleaning, modeling)
- **Pandas, Scikit-learn, XGBoost**
- **Tableau** (visualizations)
- **Jupyter Notebooks**


