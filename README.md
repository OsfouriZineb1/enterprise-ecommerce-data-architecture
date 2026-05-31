# Enterprise Data Architecture: E-Commerce Performance (Olist)

## Project Overview
This repository outlines an end-to-end data engineering and business intelligence workflow analyzing 100,000+ e-commerce logistics and sales records. The project is structured in two phases: a traditional BI pipeline (completed) and a Big Data distributed architecture blueprint designed for enterprise scale.

**Note:** The complete Phase 1 technical documentation and dashboard outputs are available in the attached PDF: `ZINEB OSFOURI_PROJET_Pilotage de la Performance E-commerce Cas Olist.pdf`.

## Phase 1: Traditional BI & ETL Pipeline (Completed)
* **Data Modeling:** Designed a Star Schema in MySQL optimized for OLAP. Centralized quantitative metrics in a `fact_sales` table and descriptive axes in dimension tables (`dim_customers`, `dim_products`).
* **ETL Processing:** Engineered an ETL pipeline using Talend Open Studio. Mapped raw CSV data to the schema, handled missing values via Java conditions in `tMap`, and ensured data integrity using `tUniqRow`.
* **Visualization:** Exported structured data to Qlik Sense to develop interactive dashboards analyzing revenue evolution, geographic customer distribution, and loyalty indices.

## Phase 2: Distributed Big Data Architecture (Current Focus)
To scale this supply chain analysis beyond the initial 100k records, the architecture is being re-engineered utilizing the Apache Hadoop ecosystem to bypass single-node MySQL memory constraints.
* **Distributed Storage (HDFS):** Transitioning raw e-commerce data into HDFS for fault tolerance and high-availability parallel storage.
* **Distributed Processing (Hive & YARN):** Upgrading the local Talend ETL workload to Apache Hive. This translates SQL into parallelized MapReduce jobs, enabling massive-scale table joins across multiple geographic data nodes.

## Tech Stack
* **Phase 1 (BI):** MySQL, Talend Open Studio, Qlik Sense
* **Phase 2 (Big Data):** Apache Hadoop (HDFS, YARN), Apache Hive, MapReduce
* **Author:** Zineb Osfouri
