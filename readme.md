Motor Vehicle Collision Analysis
🚦 Project Overview
This project analyzes over 10 million vehicle crash records across metropolitan areas to uncover insights into accident trends, high-risk zones, and injury patterns. Leveraging modern data engineering practices, the solution ensures scalable, maintainable, and reliable pipelines for processing large-scale structured data. The project emphasizes data quality, traceability, and insightful analytics using cloud-native technologies and dimensional modeling techniques.

Tools & Technologies:
Azure Data Factory | Snowflake | Alteryx | SQL | ER Studio | Power BI | dbt (for modeling)

📂 Data Sources
The datasets were sourced from official city data portals and span a 5-year period, covering:

New York City

Chicago

Austin

Montgomery

Each dataset had schema inconsistencies, requiring extensive profiling and normalization.

🔧 Key Implementation Highlights
🔍 1. Data Profiling & Cleansing
Alteryx was used for initial data profiling: checking for nulls, outliers, and pattern inconsistencies.

Identified schema mismatches and standardized data types and formats for downstream processing.

🔁 2. Data Pipeline Architecture
Built a modular Azure Data Factory pipeline to ingest raw crash data from each city.

Data was staged in a Bronze-Silver-Gold architecture:

Bronze: Raw CSV ingestion

Silver: Cleaned and standardized parquet-formatted data

Gold: Final Snowflake tables ready for analytics

🧠 3. Dimensional Modeling
Designed a Snowflake schema using ER Studio with separate Fact and Dimension tables.

Incorporated Slowly Changing Dimensions (SCD Type 2) to track evolving attributes like collision category changes over time.

Used audit columns for versioning and traceability.

📈 4. Analytics & Insights
Created dashboards in Power BI to analyze:

Accident distribution by time, weather, location

Injury vs. fatality hotspots

City-wise comparative risk

Geospatial analysis using lat/long coordinates for heatmaps.

🔎 Business Insights Delivered
Most accident-prone intersections by city.

Injury trends by day/time/season.

Pedestrian vs. motorist injury and fatality comparisons.

Common causes and conditions during high-severity accidents.
