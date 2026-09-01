# SMART RETAIL & INVENTORY INTELLIGENCE PLATFORM: PREDICTIVE DEMAND FORECASTING AND CUSTOMER SEGMENTATION SYSTEM

An end-to-end retail analytics, machine learning, and inventory optimization platform designed to minimize stockouts, forecast future demand, segment customer behaviors, and deliver interactive executive insights.

---

## 🚀 Live Application
👉 **Access the Live Dashboard Here:** [Smart Retail & Inventory Intelligence Platform](https://YOUR-STREAMLIT-APP-URL.streamlit.app)(https://smart-retail-inventory-intelligence-platform-6wwyrj5myawmhslsm.streamlit.app/

---

## 📓 Google Colab Development & Notebooks
The data engineering, exploratory data analysis, and machine learning pipelines were developed, trained, and executed across four dedicated Google Colab notebooks:

* [🔗 Colab Notebook 1: Data Ingestion, Cleaning & EDA](https://colab.research.google.com/drive/1zIuz7mxIGHE5Xe8PcUHVITldXiGhbfVv?usp=sharing)
* [🔗 Colab Notebook 2: Module 1 - Customer Segmentation (RFM & K-Means)](https://colab.research.google.com/drive/1cSr_3Kjqw2M43Y1Ql8Iojshfh_IgyNDy?usp=sharing)
* [🔗 Colab Notebook 3: Module 2 - Demand Forecasting (ARIMA Time-Series)](https://colab.research.google.com/drive/1Da-HuNxeq5l4gjs2n5ZDhKN1srg1AD_E?usp=sharing)
* [🔗 Colab Notebook 4: Module 3 - Inventory Optimization & Replenishment](https://colab.research.google.com/drive/1Da-HuNxeq5l4gjs2n5ZDhKN1srg1AD_E?usp=sharing)

---

## 📊 Dashboard Architecture & Pages
The analytics platform is structured into four core analytical pages providing granular visibility across operations:

1. **Page 1: ONLINE RETAIL TRANSACTIONS DASHBOARD**
   * *Focus:* Exploratory data overview, transactional trends, revenue metrics, and data distribution patterns from cleaned master data.
2. **Page 2: CUSTOMER SEGMENTATION ANALYSIS**
   * *Focus:* Behavioral clustering using Recency, Frequency, and Monetary (RFM) metrics to isolate VIP, loyal, and at-risk customer tiers.
3. **Page 3: SALES FORECASTING ANALYSIS**
   * *Focus:* Time-series predictive projections using ARIMA models to anticipate forward-looking daily sales velocity.
4. **Page 4: STOCK HEALTH & REPLENISHMENT ANALYSIS**
   * *Focus:* Automated safety stock calculations, reorder point (ROP) thresholds, and SKU-level risk classification (*Critical Stockout Risk*, *Reorder Required*, *Optimal*).

---

## 📂 Uploaded Datasets & Repository Structure
The repository contains the cleaned and structured data marts generated from the modeling pipeline:

```text
├── app.py                             # Main Streamlit interactive web application
├── cleaned_retail_data_new.xlsx       # Cleaned foundational retail master dataset
├── customer_segments_output.xlsx      # Customer-level K-Means cluster output table
├── demand_forecast_data.xlsx          # Chronological daily sales projection output
├── inventory_optimization_data.xlsx   # SKU-level inventory control & safety stock table
├── requirements.txt                   # Python dependencies (streamlit, pandas, openpyxl)
└── README.md                          # Project documentation
