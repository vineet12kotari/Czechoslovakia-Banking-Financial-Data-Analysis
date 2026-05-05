# 🏦 Czechoslovakia Banking Financial Data Analysis

An end-to-end **financial data analytics project** analyzing banking operations, customer demographics, loans, transactions, and account activity using **AWS S3, Snowflake, SQL and Power BI**.

This project demonstrates a **modern cloud analytics pipeline** that transforms raw banking data into **interactive dashboards and actionable business insights**.

---

# 📌 Project Overview

Banks generate large volumes of customer and transaction data. Extracting insights from this data helps financial institutions improve **risk assessment, customer segmentation, and product strategy**.

This project analyzes **Czechoslovakia banking data** to understand:

* Customer demographics across districts
* Bank popularity and balance distribution
* Loan repayment patterns
* Account and card usage trends
* Transaction trends over time

The workflow implements a **real-world analytics architecture used in data teams.**

---

# 🎯 Business Questions

The analysis aims to answer several key questions:

* Which banks have the **highest total customer balances**?
* What are the **most commonly used card types**?
* Which account types have the **highest loan repayment issues**?
* How have **transactions evolved over time**?
* Which districts show **higher average salaries and demographic influence**?
* Which banks attract **high-value premium customers**?

---

# 🧰 Technology Stack

| Tool          | Purpose                            |
| ------------- | ---------------------------------- |
| **AWS S3**    | Cloud data storage                 |
| **Snowflake** | Data warehouse and transformations & Cortex Ai querying |
| **Snowpipe**  | Automated data ingestion           |
| **Power BI**  | Dashboard development              |
| **DAX**       | KPI calculations                   |

---

# 🗂 Dataset Description

The project uses **8 relational tables** representing banking operations.

| Table        | Description                               |
| ------------ | ----------------------------------------- |
| Account      | Information about bank accounts           |
| Card         | Details of issued credit/debit cards      |
| Client       | Client demographic information            |
| Disposition  | Relationship between clients and accounts |
| District     | Demographic data of regions               |
| Loan         | Loan details and repayment status         |
| Order        | Financial order records                   |
| Transactions | Historical account transactions           |

---

# 🏗 Data Pipeline Architecture

```text
Raw Banking Data
      │
      ▼
AWS S3 Data Lake
      │
      ▼
Snowflake Data Warehouse & Cortex Ai
      │
      ▼
Power BI Dashboard
```

---

# ☁️ AWS S3 Data Storage

Raw datasets are stored in **AWS S3 bucket folders** for scalable cloud storage.

```
ACCOUNT/
CARD/
CLIENT/
DISPOSITION/
DISTRICT/
LOAN/
ORDER/
TRANSACTIONS/
```

![AWS S3 Storage](images/awsS3.png)

---

# 🧱 Data Warehouse (Snowflake)

Snowflake is used to create the **analytics warehouse**.

Key steps:

* Creating database and schema
* Defining tables for each dataset
* Creating file formats
* Loading staged data from S3
* Automating ingestion using **Snowpipe**

---

# 🔗 Entity Relationship Model

The dataset follows a relational structure connecting clients, accounts, loans, and transactions.

![Database ER Diagram](images/ER_diagram.png)

---

# 📊 Power BI Data Model

Snowflake tables are imported into Power BI to create a **semantic data model**.

![Power BI Data Model](images/data_model.png)

---

# 📊 Dashboard Overview

The Power BI dashboards provide insights into banking operations.

![Banking Dashboard](images/overview.png)

Key metrics visualized:

* Total banks
* Total transactions
* Accounts by card type
* Balance distribution by bank
* Transaction trends

---

# 📊 Bank Performance Analysis

![Bank Performance](images/bank_perf.png)

This dashboard highlights:

* Bank popularity ranking
* Premium customers by balance
* Top account holders
* Loan accounts by bank

---

# 👥 Client Demographics Analysis

![Client Demographics](images/client.png)

Key insights include:

* Total districts
* Total clients
* Gender distribution
* Top districts by salary
* Average age distribution

---

# 📈 Key Insights

### Customer Demographics

* The dataset contains **5.37K clients across 77 districts**
* Gender distribution is relatively balanced

### Card Usage

* **Gold cards dominate usage**, followed by silver and diamond cards
* Some banks do not offer premium card services

### Transaction Trends

* A noticeable **drop in transactions during 2020**, likely due to economic slowdown

### Loan Repayment Patterns

* **Salary account holders show higher loan default or delayed repayment**

### Bank Performance

* **Sky Bank leads in maintaining account holders**
* Northern Bank and Nanital Bank follow in popularity

---

# 💡 Strategic Recommendations

Based on the analysis:

* Introduce **premium card offerings** for high-balance customers
* Launch targeted financial products for **NRI account holders**
* Improve **loan risk monitoring for salary accounts**
* Track **top depositors** to strengthen customer retention strategies

![Client Demographics](images/sugg1.png)
![Client Demographics](images/sugg2.png)

---

# 🤖 Snowflake Cortex Analyst (Semantic Querying)

To enhance accessibility of insights, Snowflake Cortex Analyst was used to enable 
natural-language querying on structured datasets.

This allows users to:
- Query data using plain English instead of SQL
- Retrieve insights without technical knowledge
- Reduce dependency on ad-hoc SQL queries

Example use cases:
- "Show top banks by total balance"
- "Which districts have highest average salary?"
- "Loan default trends by account type"

---

# 🚀 Skills Demonstrated

✔ Cloud Data Storage (AWS S3)

✔ Data Warehousing (Snowflake)

✔ Cortex Ai querying (Snowflake)

✔ Automated Data Pipelines (Snowpipe)

✔ Data Modeling

✔ Business Intelligence Dashboards (Power BI)

✔ Financial Data Analysis

✔ KPI Development using DAX
