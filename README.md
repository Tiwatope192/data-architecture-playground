
# data-architecture-playground
This is my brainstorming space to explore business problems and designing data architectures and pipelines to solve them.

Business Case study 1 - Palmpay
Palmpay Data Architecture Evolution: AS-IS → TO-BE Overview

This project demonstrates the transition from a fragmented, transaction-driven data environment to a modern, scalable data platform designed for analytics and business intelligence.

AS-IS: Current Challenges**

The existing architecture relies on multiple transactional databases (Transaction, User/Wallet, and Merchant DBs) with no centralized data warehouse or structured data pipeline.

Key Issues Direct querying of production systems Data analysts query transactional databases directly Leads to system strain and downtime (up to 40%) No centralized data model Data is siloed across multiple sources No single source of truth Manual and error-prone processes Finance team performs reconciliation using spreadsheets High risk of human error and inefficiency Inconsistent metrics Different teams use different logic Results in conflicting business insights Lack of governance and versioning No traceability of changes No collaboration framework Risk of data loss and inconsistency Impact Slow and unreliable dashboards Poor data quality and trust Delayed decision-making Incorrect business insights

TO-BE: Proposed Solution
The proposed architecture introduces a modern data stack with a centralized data warehouse and automated data pipelines.

Key Components Data Ingestion Extract data from transactional systems in controlled batches Removes direct load on production systems Data Warehouse (Snowflake) Centralized storage for all data Separation between raw, processed, and analytical layers Data Transformation (dbt) Structured modeling and transformation Creation of: Raw layer (ingested data) Silver layer (cleaned data) Gold layer (business-ready datasets) Version Control (GitHub) Tracks all data model and pipeline changes Enables collaboration and reproducibility Data Consumption Analysts access curated datasets Dashboards and reports built on trusted data Benefits Improved system performance No direct queries on transactional databases Single source of truth Consistent and reliable metrics across teams Automation and scalability Reduced manual processes and errors Faster and more reliable insights Optimized data models for analytics Governance and traceability Full version control and auditability

Conclusion
This transformation shifts the organization from a manual, fragmented, and unreliable data environment to a scalable, automated, and governed data platform, enabling accurate, timely, and data-driven decision-making.

“This project demonstrates my approach to designing scalable data architectures, from identifying system bottlenecks to implementing a modern analytics stack.”

Author
Peju Sokunle
