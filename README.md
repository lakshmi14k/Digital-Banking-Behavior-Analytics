**Digital Banking Behavior & Product Impact Analysis**

**Problem Statement:**
Fintech product teams lack visibility into which user segments are at risk of churning 
and what behavioral patterns drive customer lifetime value, leading to missed retention 
opportunities and misaligned product investment decisions.

**Proposed Solution:**
A PySpark analytics pipeline on Databricks that segments users by churn risk, quantifies 
LTV across behavioral and demographic dimensions, and delivers an executive Power BI 
dashboard to guide product prioritization and retention strategy.

**Key Findings:**
- **925 high-risk customers (13%)** carry equal LTV to low-risk users — high-value users are silently churning
- **Middle income users drive highest LTV ($522K avg)** — counterintuitive finding that reframes targeting strategy
- **Weekly users outperform Daily users** in both LTV and satisfaction — over-engagement does not equal higher value
- **Satisfaction score, not spending, predicts churn risk** — product experience is the key retention lever

**Dataset Overview:**
Synthetic dataset simulating realistic fintech customer behavioral and transactional data.
- **Total Records:** 7,000 users
- **Features:** 20 behavioral and demographic attributes
- **Source:** [FinTech Customer LTV Dataset — Kaggle](https://www.kaggle.com/datasets/harunrai/fintech-customer-life-time-value-ltv-dataset)

**Tech Stack:**
- **Platform:** Databricks Community Edition
- **Processing:** PySpark + Spark SQL
- **Visualization:** Power BI Desktop
- **Export:** Python (Pandas)

**Project Structure:**
```
Digital-Banking-Behavior-Analytics/
│
├── data/
│   └── fintech_ltv_dataset.csv          ** Raw Kaggle dataset (7,000 users, 20 features)
│
├── notebooks/
│   └── digital_banking_analysis.ipynb   ** PySpark analysis notebook
│
├── dashboard/
│   ├── digital_banking_dashboard.pbix   ** Power BI dashboard file
│   └── dashboard.png                    ** Dashboard screenshot
│
└── README.md
```
**Results:**
- 7,000 users analyzed across 20 behavioral features
- 3 churn risk segments identified (High / Medium / Low)
- 4 key insights surfaced for product and retention teams
- Executive Power BI dashboard with 6 visuals and 3 interactive slicers

**How to Run:**
1. Download dataset from [Kaggle](https://www.kaggle.com/datasets/harunrai/fintech-customer-life-time-value-ltv-dataset)
2. Sign up for [Databricks Community Edition](https://community.cloud.databricks.com)
3. Upload CSV → Create table named `raw`
4. Run `notebooks/digital_banking_analysis.ipynb`
5. Open `dashboard/digital_banking_dashboard.pbix` in Power BI Desktop

Built with *Databricks, PySpark, Spark SQL, and Power BI*
