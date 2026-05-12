# 📉 Customer Churn & Engagement Analysis

> End-to-end churn analysis on 50,000 e-commerce customer records by data cleaning, EDA, behavioral analysis, customer segmentation, and business recommendations.

---

## 📌 Project Overview

This project performs a full data analyst workflow on a synthetic e-commerce dataset of **50,000 customers** across **25 features** spanning demographics, purchase history, and multi-channel engagement metrics (web, mobile, email, social media).

The dataset includes a binary target variable (`Churned`), and the analysis uncovers **why customers leave**, **who is most at risk**, and **what the business should do about it**.

---

## 🔍 Key Findings

| Finding | Detail |
|---|---|
| Overall churn rate | **28.9%** across 50,000 customers |
| Total LTV lost to churn | **~$20.6 million** |
| U-shaped LTV paradox | Both Low (41.3%) and Premium (39.6%) LTV tiers churn at the same rate - for different reasons |
| Gen Z retention crisis | Under-25s churn at **45.5%** - nearly double every other age group |
| Engagement is the #1 lever | Disengaged customers churn at **51.6%** vs 19.4% for highly engaged |
| Early warning rule | A 3-signal flag identifies at-risk customers at **84% churn rate** - a **3x lift** over baseline |
| Winback opportunity | Churned customers spent **13.8% more per order** than retained ones - worth targeting |

---

## 📂 Project Structure

```
customer-churn-analytics/
│
├── customer_churn_analysis.ipynb   # Main Jupyter Notebook (6 chapters)
├── ecommerce_customer_churn_dataset.csv  # Raw dataset
├── churn_cleaned.csv               # After Chapter 2 cleaning
├── churn_segmented.csv             # After Chapter 5 segmentation
├── churn_final.csv                 # Fully enriched final dataset
├── Customer_Churn_Analytics.docx   # Full project report with charts
└── README.md
```

---

## 📓 Notebook Structure

The analysis is split into **6 chapters**, each building on the last:

### Chapter 1 : Setup & Data Loading
- Load and inspect the raw dataset
- Check class balance of the churn target variable
- First look at data types and statistical summary

### Chapter 2 : Data Cleaning & Quality Audit
- Missing value audit with visualisation
- Remove duplicates
- Fix outliers (Age > 100 capped, negative purchases clipped)
- Median imputation for missing numerical values
- Standardise categorical text fields

### Chapter 3 : Exploratory Data Analysis
- Distribution of all numeric features
- Churn rate by age group, gender, country, membership tenure, signup quarter
- Feature correlation heatmap

### Chapter 4 : Behavioral Analysis
- Direct comparison of churned vs retained customers across 12 behavioral metrics
- Engagement metrics: login frequency, email open rate, mobile usage, social engagement
- Friction metrics: cart abandonment, days since purchase, customer service calls
- KDE distribution overlap plots
- The Average Order Value paradox

### Chapter 5 : Customer Segmentation
- **LTV Segments** - 4 tiers revealing the U-shaped churn paradox
- **Composite Engagement Score** — built from 5 normalised behavioral signals
- **At-Risk Flag** - 3-variable rule with 3x targeting lift over baseline

### Chapter 6: Business Insights & Recommendations
- Revenue impact quantification
- 5 prioritised insights with supporting charts
- Actionable recommendations for each segment
- Executive summary table

---

## 💡 Business Recommendations

| # | Recommendation | Impact | Effort |
|---|---|---|---|
| R1 | Fix onboarding journey for Low-LTV customers | High | Medium |
| R2 | Dedicated support tier for Premium accounts | Very High | Low |
| R3 | Weekly automated email re-engagement trigger | High | Low |
| R4 | Simplified checkout flow for under-25 segment | Medium | Medium |
| R5 | Deploy 3-signal at-risk CRM flag | Very High | Low |
| R6 | Personalised winback campaign for high-AOV churners | High | Low |

> **Start with R3 and R5** — highest impact, lowest implementation effort.

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|---|---|
| Python 3.x | Primary language |
| Pandas & NumPy | Data manipulation and cleaning |
| Matplotlib & Seaborn | All visualisations |
| Scikit-learn | Feature normalisation |
| Jupyter Notebook | Development environment |

---

## 📊 Dataset

- **Source:** Synthetic e-commerce dataset (Kaggle)
- **Records:** 50,000 customers
- **Features:** 25 columns demographics, behavior, purchase history, engagement
- **Target:** `Churned` (binary: 0 = retained, 1 = churned)
- **Channels covered:** Web, Mobile App, Email, Social Media

---

## 🚀 How to Run

1. Clone or download this repository
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```
3. Open the notebook:
```bash
jupyter notebook customer_churn_analysis.ipynb
```
4. Run all cells from top to bottom each chapter builds on the previous one

---

## 👤 Author

**Dhiraj Telwani**  
---

*This project is part of my data analytics portfolio. The dataset is synthetic and does not represent real customer data.*
