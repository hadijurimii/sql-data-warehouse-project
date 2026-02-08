# 🏗️ SQL Data Warehouse Project

## 📌 Project Overview
This repository contains a SQL-based Data Warehouse project designed to transform raw transactional data into analytics-ready datasets.  
The project follows modern data engineering best practices, including layered architecture, star schema modeling, and data quality validation.

The primary objective is to enable reliable reporting and analytics for business users and data analysts.

---

## 🧱 Data Warehouse Architecture
The warehouse is designed using a **multi-layer architecture**:

### 1️⃣ Staging Layer
- Stores raw data from source systems
- Minimal to no transformation
- Acts as a temporary landing zone for ingestion

### 2️⃣ Core / Transformation Layer
- Applies business logic and data cleansing
- Handles:
  - Deduplication
  - Data type standardization
  - Null handling
- Produces clean and consistent datasets

### 3️⃣ Analytics / Presentation Layer
- Implements fact and dimension tables
- Optimized for BI tools and analytical queries

---

## 📊 Data Modeling Approach
This project uses a **Star Schema** design:

- **Fact Tables**
  - Store measurable business metrics (e.g. sales, revenue, transactions)
- **Dimension Tables**
  - Store descriptive attributes (e.g. customer, product, date)

Benefits:
- Improved query performance
- Simplified analytical queries
- Better scalability for future reporting needs

---

## 🗂️ Project Structure
```text
sql-data-warehouse/
│
├── staging/
│   ├── stg_customers.sql
│   ├── stg_orders.sql
│
├── core/
│   ├── dim_customers.sql
│   ├── dim_products.sql
│   ├── fact_sales.sql
│
├── analytics/
│   ├── sales_summary.sql
│   ├── customer_metrics.sql
│
├── tests/
│   ├── row_count_checks.sql
│   ├── null_validation.sql
│
└── README.md
