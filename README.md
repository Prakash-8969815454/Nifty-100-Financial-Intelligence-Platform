# Nifty-100-Financial-Intelligence-Platform
The Nifty 100 Financial Intelligence Platform is a production-grade, self-contained data analytics and financial screening system. Its core mission is to transform raw, tabular financial statement data into fully structured, auditable analytics intelligence covering constituents of the Nifty 100 Index.

# Nifty 100 Financial Intelligence Platform
### *Enterprise Data Engineering, Machine Learning Segmentation, and Analytics Architecture*

---

## 📋 Executive Overview
The **Nifty 100 Financial Intelligence Platform** is an end-to-end data engineering and predictive analytics pipeline designed to ingest, process, segment, and expose comprehensive financial statement data (~11,000+ data points) across major corporate entities. 

The platform normalizes disparate unstructured accounting files into a unified relational database schema, evaluates over 50+ institutional financial metrics, groups companies based on financial behavior profiles using unsupervised machine learning, and serves insights via an interactive presentation layer and production-grade REST microservices.

## ⚙️ Technical Stack Architecture

| Layer | Component Technology |
| :--- | :--- |
| **Core Storage Engine** | SQLite 3, Relational Database Modeling |
| **ETL & Analytics Processing Engine**| Python 3, Pandas, NumPy, OpenPyXL |
| **Machine Learning Core** | Scikit-Learn (K-Means Clustering, StandardScaler) |
| **Interactive Visualization Data Layer**| Plotly Express, Plotly Graph Objects |
| **Presentation Framework** | Streamlit Web Server |
| **Microservice Application Layer** | FastAPI, Uvicorn ASGI Server Framework |

---

## 🧩 Core Modular Architecture
├── Module 1: Data Engineering & Robust ETL Pipeline 
├── Module 2: Core Financial Ratio Engine 
├── Module 3: Advanced Investment Screening Engine 
├── Module 4: Cross-Sectional Cohort Peer Benchmarking 
├── Module 5: Interactive Executive Dashboard (Streamlit) 
├── Module 10: Statistical Segmentation Modeling (K-Means) 
└── Module 11: Production REST API Gateway (FastAPI)

### 🗄️ Module 1: Data Engineering & Pipeline Ingestion
 * Parses, cleans, and structures fundamental historical datasets covering Company Profiles, Profit & Loss (P&L), Balance Sheets, Cash Flows, Stock Price CAGR, and qualitative "Pros & Cons" scripts.
 * Enforces relational data consistency by sanitizing primary and foreign key variables (`company_id`).
 * Configures a structured database file (`nifty100.db`) optimized with indexes to achieve low-latency query handling.
 ### 📊 Module 2: Core Financial Ratio Engine 
* Executes complex cross-table arithmetic calculations using consolidated balance sheet items and income statement factors.
 * Programmatically derives key valuation parameters including: * **Operating Profit Margin (OPM %)** * **Return on Equity (ROE %)** * **Debt-to-Equity Ratio** 
### 🔍 Module 3: Advanced Investment Screening Engine 
* Filters the financial universe dynamically through a multi-parameter constraint matrix
. * Implements a rank-aggregation algorithm that maps percentile metrics into a consolidated, proprietary **Financial Health Score (0–100)**. * Saves outputs to a persistent data table (`screener_output`) for low-overhead reporting. 
### 📉 Module 4 & 10: Statistical Segmentation & Peer Benchmarking 
* Uses unsupervised machine learning (**K-Means Clustering**, where $k = 5$) to group entities by risk-return profiles rather than static industry labels.
 * Classifies entities into automated strategies: *High-Quality Growth, Defensive Dividend, Value Cyclicals, Emerging Growth*, and *Distressed / High Debt*. * Computes variance matrices mapping individual corporate metric deviations directly against peer-group cross-sectional means.
 ### 🖥️ Module 5: Interactive Executive Dashboard
 * A responsive, interactive multi-tab internal dashboard powered by **Streamlit**. * Integrates interactive time-series financial trend lines, asset performance tracking, visual margin expansion ratios, and automated textual extraction of qualitative fundamental pros and cons.


 ### ⚡ Module 11: Production REST API Gateway
 * Exposes enterprise services using high-performance **FastAPI** ASGI microservice endpoints. * Includes built-in auto-generated **Swagger / OpenAPI Documentation** via `/docs`. * Features structured telemetry check-points, company index parameters, historical query maps, and real-time clustering peer endpoints. —
 ## 🚀 Deployment & Execution Guide (Google Colab Environment)
 ### 1. Repository Setup & Ingestion Implementation Ensure raw `.csv` resource files are moved to the root level of your virtual cloud directory workspace (`/content/`). Execute the database setup pipeline script cell: ```python
 ##Creates and aggregates datasets into nifty100.db python module_etl_pipeline.py 

