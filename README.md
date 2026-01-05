# fabric-end-to-end-data-platform

Project Overview
  - This project demonstrates an end-to-end implementation of Medallion Architecture in Microsoft Fabric, covering the full lifecycle from raw data ingestion to business-ready analytics.
  - The objective was to design a scalable, maintainable data platform that separates concerns across Bronze, Silver, and Gold layers, and exposes trusted metrics through a semantic   model and    Power BI.

Architecture Summary
  Bronze Layer
  - Raw ingestion from ADLS Gen2 using Fabric Data Pipelines
  - Immutable, replayable data storage

Silver Layer
 - Data validation, cleansing, and enrichment using PySpark
 - Incremental processing with timestamp-based logic

Gold Layer
- Business-ready aggregations (daily sales, category sales)
- Optimized for analytics and reporting

Semantic Model
- Centralized business logic and relationships
- Consistent metric definitions

Power BI
- Interactive dashboards built on the semantic model
- No transformation logic pushed into reports

Tech Stack
- Microsoft Fabric (Lakehouse, Pipelines, Notebooks)
- PySpark / Spark SQL
- Azure Data Lake Gen2
- Power BI
- Medallion Architecture

Why this project matters
- This project focuses on design discipline, not just tooling:
- Clear separation of concerns
- Incremental and replayable pipelines
- Business logic centralized outside reports
- Real-world data quality challenges handled explicitly
