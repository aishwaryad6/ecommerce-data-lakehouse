# 🛒 E-Commerce Data Lakehouse Pipeline  

This project demonstrates an **end-to-end data lakehouse solution** for e-commerce data, leveraging **Azure Data Lake Gen2, Azure Data Factory (ADF), and Azure Databricks (PySpark)**.  
It follows the **Medallion Architecture (Bronze, Silver, Gold layers)** to enable **scalable, reliable, and high-quality analytics**.  

---

## 🚀 Project Workflow  

1. **Data Ingestion**  
   - Raw CSVs (users, buyers, sellers, countries) ingested into Azure Data Lake Gen2 (landing zone).  
   - Automated **ADF pipelines** convert CSVs to Parquet and move them into the **Bronze layer**.  
   - Event-based triggers run pipelines automatically when new files arrive.  

2. **Data Transformation**  
   - **Bronze Layer**: Raw Parquet files stored with minimal processing, ensuring traceability and schema evolution.  
   - **Silver Layer**: Data cleaning (deduplication, type casting, missing values), standardization, and enrichment using PySpark in Databricks.  
   - **Gold Layer**: Curated Delta tables created with joins, aggregations, and business logic for analytics-ready consumption.  

3. **Data Consumption**  
   - Gold tables queried in **Databricks SQL**.  
   - Visualized with **Tableau/Power BI** dashboards for KPIs such as sales, user activity, and regional performance.  

---

## 🛠️ Tech Stack  

- **Azure Data Factory** → Data ingestion pipelines  
- **Azure Data Lake Gen2** → Data storage (Bronze, Silver, Gold layers)  
- **Azure Databricks (PySpark)** → Data transformation and enrichment  
- **Delta Lake** → Unified lakehouse with schema evolution & ACID transactions  
- **BI Tools** → Tableau / Power BI for dashboarding  

---

## 📂 Repository Structure  

```bash
ecommerce-data-lakehouse/
│
├── datasets/                 # Sample e-commerce raw datasets (CSV)
│
├── pipelines/                # Azure Data Factory pipeline JSONs
│   ├── users_pipeline.json
│   └── transactions_pipeline.json
│
├── notebooks/                # Azure Databricks notebooks (PySpark transformations)
│   ├── bronze_to_silver.ipynb
│   ├── silver_to_gold.ipynb
│   └── kpi_aggregations.ipynb
│
├── docs/                     # Architecture & documentation
│   ├── data_architecture.png
│   ├── medallion_layers.md
│   └── business_kpis.md
│
└── README.md                 # Project overview

```
---

## 🎯 Key Skills Demonstrated  

- Building a **Lakehouse Architecture** on Azure (ADF, ADLS, Databricks)  
- Implementing **Medallion architecture** (Bronze → Silver → Gold)  
- Writing **PySpark transformations** for cleaning, enrichment, and aggregation  
- Delivering **BI-ready curated data** for dashboards and analytics  
- Showcasing **cloud-native scalable pipelines** for real-world e-commerce use cases  

---

## 📈 Example Insights  

- Top-selling product categories by revenue and geography  
- Buyer-seller transaction patterns and customer activity trends  
- Regional sales distribution and user engagement over time  

---

