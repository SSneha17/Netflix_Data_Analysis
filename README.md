# 📊 Netflix End-to-End Data Engineering Project on Azure & Databricks  

## 🔥 Overview  
This project demonstrates an **end-to-end data pipeline** for processing Netflix data using **Azure and Databricks**. It follows the **Medallion Architecture** (Bronze, Silver, Gold) on **Azure Data Lake Storage (ADLS)** and utilizes **Azure Data Factory (ADF)**, **Databricks**, **Delta Live Tables**, and **Databricks Autoloader** for seamless data ingestion, transformation, and orchestration.  

## 🏗 Architecture  
1. **Data Ingestion (Bronze Layer)**
   - Source: GitHub repository containing Netflix data.  
   - Tool: **Azure Data Factory (ADF)** pipelines pull data from GitHub and load it into the **Bronze layer** on **ADLS**.
   - **Linked services** connect **GitHub → ADF** and **ADF → ADLS Bronze**.  
   - **Databricks Autoloader** is used to incrementally load new files into the **Bronze Layer**, reducing manual ingestion efforts.  

2. **Data Processing & Transformation (Silver Layer)**
   - **Databricks Access Connector** links ADLS to Databricks.  
   - **Azure Databricks** processes raw data and applies cleaning & transformations.  
   - Data is stored as **Delta Tables** in the **Silver Layer**.  

3. **Data Aggregation & Analysis (Gold Layer)**
   - Transformed data is further aggregated in **Delta Live Tables**.  
   - **Unity Catalog** is used for data governance & organization.  
   - **Databricks Workflows** schedule and orchestrate jobs.  

## 🛠 Technologies Used  
- **Azure Data Lake Storage (ADLS)** – Storage for Bronze, Silver, and Gold layers.  
- **Azure Data Factory (ADF)** – ETL tool for ingesting data from GitHub to ADLS.  
- **Azure Databricks** – Processing, transformation, and analysis engine.  
- **Delta Lake & Delta Live Tables** – Optimized storage & real-time transformations.  
- **Databricks Autoloader** – Automated and incremental ingestion of new data files.  
- **Unity Catalog** – Centralized governance for managing data assets.  
- **Databricks Workflows** – Job scheduling and orchestration.

  
## 📂 Project Structure  
- /RawDataFiles - contains 5 raw .csv files
- /Azure_Databricks_NetflixProject - contains the autoloader and the Notebooks
- /dataset, /factory, /linkedservices - code pushed from Azure ADF for creating data factory pipelines and the linked services.



## 🚀 Getting Started  
### 1️⃣ Prerequisites  
- Azure Subscription with **ADLS**, **ADF**, and **Databricks** enabled.  
- Databricks cluster configured with **Unity Catalog**.  


### 2️⃣ Deployment Steps  
1. Clone this repository:  
   ```bash
   git clone https://github.com/SSneha17/Netflix_Data_Analysis.git

2. Create Azure Data Lake Storage (ADLS) and set up Bronze, Silver, Gold containers.

3. Configure ADF Linked Services to connect GitHub → ADF ADLS → Bronze.

4. Set up Databricks Access Connector and create a Databricks Service.

5. Configure Databricks Autoloader to continuously ingest new data from ADLS to Databricks.

6. Import Databricks notebooks and configure Delta Tables.

7. Use Delta Live Tables to manage real-time transformations.

8. Schedule Databricks Workflows to automate the pipeline.


🎯 Key Features

✅ End-to-end data pipeline with Azure & Databricks.

✅ Medallion architecture (Bronze, Silver, Gold) for structured data processing.

✅ Delta Live Tables for real-time transformations.

✅ Automated workflows & scheduling using Databricks Workflows.

✅ Unity Catalog for centralized data governance.


[ ## 🎓 Credits & Acknowledgments  
This project is inspired by the YouTube tutorial:  
📺 **[Azure End to End Data Engineering Tutorial]** by **[Ansh Lamba]** – ([Watch Here](https://www.youtube.com/watch?v=uc-u_juRg-w))  

Special thanks to the creator for providing valuable insights into building data pipelines on **Azure & Databricks**! 🙌  ]
