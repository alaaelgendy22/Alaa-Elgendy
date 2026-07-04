# Retail Sales Intelligence Platform

**Enterprise-Grade Analytics, Machine Learning, and Reporting Architecture**

An end-to-end data analytics and engineering portfolio project simulating a real-world corporate data infrastructure. This project transforms 100,000+ raw, noisy transaction records into actionable business insights through a rigorous data pipeline, advanced SQL querying, machine learning models, and an interactive presentation-layer dashboard.

## 🚀 Business Problem Statement
The organization lacked a unified view of customer behavior, profitability, and sales performance across regional stores. Key decisions around marketing spend and inventory management were being made without understanding Customer Lifetime Value (CLV), churn risk, or product-level profit margins. 

This platform resolves these issues by delivering automated ETL processes, RFM-based segmentation, revenue forecasting, and executive-ready dashboards.

## 🏗️ Architecture Overview
```text
[ Raw Data Source ] ---> [ Data Cleaning & Feature Engineering ] ---> [ Relational SQL Database ]
(Synthetic Generator)       (Pandas: Deduping, RFM, CLV, Margin)        (SQL Server: DDL, Views)
                                      |                                          |
                                      v                                          v
                    [ Machine Learning Models ]                      [ Advanced SQL Analytics ]
                    - XGBoost: Revenue Forecasting                   - CTEs, Window Functions
                    - Random Forest: Churn Prediction                - Stored Procedures
                    - K-Means: Customer Segmentation                             |
                                      |                                          |
                                      +------------------------------------------+
                                                          |
                                                          v
                                        [ Streamlit Interactive Dashboard ]
                                        (Executive, Sales, Customer, Product)
```

## 🛠️ Technology Stack
- **Data Engineering & Cleaning**: Python (Pandas, Numpy)
- **Database Architecture**: SQL Server (T-SQL, Views, Procs, Window Functions)
- **Machine Learning**: Scikit-Learn, XGBoost
- **Data Visualization**: Plotly, Seaborn, Matplotlib
- **Web App / Dashboard**: Streamlit
- **Automated Reporting**: ReportLab (PDF Generation)

## 📊 Dataset Description
The synthetic dataset contains **100,000+ transaction records** designed to mimic real-world enterprise data challenges:
- **Tables**: `Customers`, `Products`, `Orders`, `Stores`, `Employees`.
- **Anomalies Engineered**: Missing values, duplicate records, extreme outliers, and inconsistent date formats requiring robust programmatic cleaning.

## 🧠 Machine Learning & Advanced Analytics
1. **Feature Engineering**: Engineered complex financial metrics including Profit Margin, Customer Lifetime Value (CLV), and Recency, Frequency, Monetary (RFM) scores.
2. **Customer Segmentation (K-Means)**: Grouped customers into 3 distinct cohorts based on purchasing behavior.
3. **Churn Prediction (Random Forest)**: Classified customers at risk of lapsing within 90 days.
4. **Sales Forecasting (XGBoost)**: Built a time-series regression model to predict daily aggregate revenue based on calendar features.

## 📈 Dashboard Capabilities
The Streamlit application (`Python/dashboard.py`) provides an interactive interface with global cross-filtering capabilities.
- **Executive Summary**: High-level KPIs and overarching revenue distributions.
- **Sales Analysis**: Monthly trending and top product rankings.
- **Customer Insights**: Segmentation distribution and cohort value.
- **Product Performance**: Category profit margins and revenue-to-profit correlation.

## 🚀 How to Run the Project

1. **Clone the Repository**
2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Automated Data Pipeline**
   Executes data generation, cleaning, feature engineering, and report generation in sequence.
   ```bash
   cd Python
   python run_all.py
   # Or use the provided PowerShell script: .\run_all.ps1
   ```
4. **Launch the Dashboard**
   ```bash
   cd Python
   streamlit run dashboard.py
   ```

## 📁 Folder Structure
```text
Retail-Sales-Analytics/
├── Data/                       # Raw and processed datasets (CSV/XLSX)
├── SQL/                        # Schema definitions and analytical queries
├── Python/                     # ETL, ML notebooks, Dashboard, and generation scripts
├── Dashboard_Images/           # High-resolution UI exports (PNG)
├── Reports/                    # Stitched presentation decks and Portfolio PDFs
├── PowerBI/                    # BI Design Specifications
├── requirements.txt            # Environment dependencies
└── README.md                   # Project documentation
```

*Designed and developed as a comprehensive demonstration of Senior Data Architect, Data Engineer, and Machine Learning Engineer capabilities.*
