# 🚦 Motor Vehicle Collision Analysis

## 📌 Overview
This project analyzes over **10 million vehicle crash records** across major U.S. cities to uncover insights into accident trends, high-risk zones, and injury patterns. It leverages cloud-based data engineering practices to ensure scalable, maintainable, and reliable pipelines for large-scale data. Emphasis is placed on **data quality**, **traceability**, and **dimensional modeling**.

**Technologies Used**:  
Azure Data Factory · ADLS Gen2 · Snowflake · Alteryx · SQL · ER Studio · Power BI

---

## 📂 Data Sources
Crash datasets were collected from open data portals for the following cities:
- New York City
- Chicago
- Austin
- Montgomery

These datasets spanned 5+ years and exhibited schema and format inconsistencies which were resolved in the pipeline.

---

## ⚙️ Implementation Details

### 1. Data Profiling and Cleansing
- Used **Alteryx** to perform data profiling, identify nulls, outliers, and schema anomalies.
- Standardized fields across city datasets for compatibility in downstream processes.

### 2. Pipeline Architecture (ADF)
- Developed modular **Azure Data Factory pipelines** for batch ingestion of raw files.
- Followed a **Bronze → Silver → Gold** architecture:
  - **Bronze**: Raw data ingested from blob storage
  - **Silver**: Cleaned, standardized parquet outputs
  - **Gold**: Modeled tables in Snowflake for analytics

### 3. Dimensional Modeling in Snowflake
- Created **Fact** and **Dimension** tables using ER Studio for logical design.
- Applied **SCD Type 2** logic to track changes in collision-related categories.
- Optimized schema for performance and extensibility.

---

## 📊 Analytics & Insights
- Built interactive dashboards in **Power BI** to visualize:
  - Collision trends by location, time, and severity
  - Heatmaps of high-risk intersections
  - Comparisons of injuries and fatalities across cities

---

## 🧠 Key Outcomes
- Query performance improved by **60%** due to optimized schema and indexing
- Enabled city-wise comparison dashboards for risk mitigation strategies
- Achieved end-to-end automation and repeatability of data ingestion


