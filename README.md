## **Incremental Data Processing Pipeline with SCD Type 1 Implementation**
<br>

### **Objective** 
 To build a scalable, automated data engineering pipeline that ingests, processes, and visualizes car sales data, enabling business users to track sales performance.

### **Outcome**
Reduced manual reporting time by 80% and provided near real-time insights to sales teams.

### **Tech Stack** 
PySpark, Azure Data Factory, ADLS Gen2, Azure Synapse Analytics, Azure Databricks, Azure SQL Database, Unity Catalog, Power BI, Key Vaults

### **Description**
1. **Data Ingestion** - Designed two pipelines in Azure Data Factory:
    - Static Pipeline: Pulls initial data from a GitHub repository and appends it to Azure SQL Database.
    - Dynamic Parameterized Pipeline: Extracts incremental data from Azure SQL DB, converts it into Parquet format, and stores it in ADLS Gen2.

2. **Data Transformation & Data Modelling**
    - Orchestrated Databricks notebooks to build an ETL workflow that reads incremental Parquet data from ADLS, processes it using Apache Spark, and stores it in Delta Lake format with support for incremental loading.
    - Modeled the final data into a Star Schema and implemented Slowly Changing Dimensions (SCD Type-1) to maintain historical consistency.
    - Followed Medallion Architecture (Bronze, Silver, Gold) and managed data governance and access using Unity Catalog.

3. **Visualization** - Created a Power BI dashboard to analyze sales performance.
