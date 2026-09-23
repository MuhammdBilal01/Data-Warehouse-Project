# Data Warehouse Project

A **SQL Server Data Warehouse project** demonstrating dimensional modeling, ETL concepts, SQL analytics, database design, and Data Warehouse architecture.

---

## 📌 Project at a Glance

| Area                  | Details                      |
| --------------------- | ---------------------------- |
| **Project Type**      | Data Warehouse               |
| **Database Platform** | Microsoft SQL Server         |
| **Query Language**    | SQL / T-SQL                  |
| **Main Focus**        | Data Warehousing & Analytics |
| **Modeling**          | Dimensional Modeling         |
| **Schema**            | Fact & Dimension Tables      |
| **ETL**               | Extract, Transform, Load     |
| **Analytics**         | SQL Queries & Aggregations   |
| **Tools**             | SQL Server / SSMS            |

---

# 🏗️ Data Warehouse Architecture

The overall Data Warehouse workflow can be represented as:

```text
┌──────────────────┐
│   Source Data    │
│                  │
│ Operational Data │
│ Files / Datasets │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│     EXTRACT      │
│                  │
│ Collect Source   │
│ Data             │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│    TRANSFORM     │
│                  │
│ Clean            │
│ Validate         │
│ Standardize      │
│ Apply Rules      │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│      LOAD        │
│                  │
│ Load Data into   │
│ Data Warehouse   │
└────────┬─────────┘
         │
         ▼
┌────────────────────────┐
│     DATA WAREHOUSE     │
│                        │
│ Fact Tables            │
│ Dimension Tables       │
└────────────┬───────────┘
             │
             ▼
┌────────────────────────┐
│   ANALYSIS & REPORTING │
│                        │
│ SQL Queries            │
│ Aggregations           │
│ OLAP Analysis          │
└────────────────────────┘
```

---

# 🎯 Project Objectives

| Objective                | Description                                            |
| ------------------------ | ------------------------------------------------------ |
| **Warehouse Design**     | Design a structured analytical database                |
| **Dimensional Modeling** | Work with fact and dimension concepts                  |
| **ETL**                  | Understand data extraction, transformation and loading |
| **Data Integration**     | Prepare data for centralized analysis                  |
| **SQL Analytics**        | Perform analytical queries and aggregations            |
| **Data Modeling**        | Represent business data for analytical workloads       |
| **Documentation**        | Document warehouse structures and processes            |

---

# ⭐ Key Data Warehouse Concepts

```text
                 DATA WAREHOUSE
                       │
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
      ETL        Dimensional       Analytical
                  Modeling           Queries
        │              │              │
        │        ┌─────┴─────┐        │
        │        │           │        │
        ▼        ▼           ▼        ▼
     Extract   Fact      Dimension   SQL
     Transform Table       Tables    Analysis
     Load
```

| Concept             | Purpose                                       |
| ------------------- | --------------------------------------------- |
| **Data Warehouse**  | Centralized environment for analytical data   |
| **ETL**             | Moves and prepares data for warehouse storage |
| **Fact Table**      | Stores measurable business/transactional data |
| **Dimension Table** | Stores descriptive information                |
| **Star Schema**     | Connects a central fact table with dimensions |
| **OLAP**            | Supports multidimensional analysis            |
| **Aggregation**     | Summarizes data for analysis                  |
| **Analytical SQL**  | Extracts insights from warehouse data         |

---

# ⭐ Dimensional Modeling

The project covers the basic structure of dimensional modeling.

### Fact Table

A fact table generally contains measurable values.

| Example Measure   | Purpose                |
| ----------------- | ---------------------- |
| Quantity          | Number of items        |
| Sales             | Sales amount           |
| Cost              | Transaction cost       |
| Revenue           | Revenue generated      |
| Transaction Count | Number of transactions |

### Dimension Table

Dimension tables provide descriptive information used to analyze facts.

| Dimension    | Example Information    |
| ------------ | ---------------------- |
| **Customer** | Customer details       |
| **Product**  | Product details        |
| **Date**     | Day, month, year       |
| **Supplier** | Supplier information   |
| **Location** | Geographic information |

---

# ⭐ Star Schema

A typical star schema can be represented as:

```text
                  ┌───────────────┐
                  │ Date Dimension│
                  └───────┬───────┘
                          │
                          │
┌─────────────────┐       ▼       ┌──────────────────┐
│ Product         │────► FACT ◄────│ Customer         │
│ Dimension       │       │        │ Dimension        │
└─────────────────┘       │        └──────────────────┘
                          │
                          │
                  ┌───────▼────────┐
                  │ Supplier       │
                  │ Dimension      │
                  └────────────────┘
```

The **Fact Table** acts as the center of the analytical model while Dimension Tables provide different perspectives for analysis.

---

# 🔄 ETL Process

ETL stands for:

| Stage | Meaning   | Main Purpose                            |
| ----- | --------- | --------------------------------------- |
| **E** | Extract   | Collect data from source systems        |
| **T** | Transform | Clean, validate and modify data         |
| **L** | Load      | Insert prepared data into the warehouse |

### Common Transformation Activities

```text
Raw Data
   │
   ├──► Remove duplicates
   │
   ├──► Handle missing values
   │
   ├──► Standardize formats
   │
   ├──► Convert data types
   │
   ├──► Apply business rules
   │
   └──► Prepare warehouse-ready data
                    │
                    ▼
             Data Warehouse
```

---

# ⚠️ ETL Process Folder — Important Note

The repository contains:

```text
ETL Process (InventoryDW)
```

This folder contains **ETL material from a different Inventory Data Warehouse project**.

The original ETL screenshots belonging specifically to this main Data Warehouse project were **misplaced, deleted, or are no longer available**.

Therefore:

| Material                                 | Status                             |
| ---------------------------------------- | ---------------------------------- |
| Main Data Warehouse project              | ✅ Main project                     |
| Data Warehouse diagrams                  | ✅ Main project                     |
| Data Warehouse documentation             | ✅ Main project                     |
| SQL Showcase                             | ✅ Main project                     |
| `ETL Process (InventoryDW)`              | ⚠️ Separate/reference ETL material |
| Original ETL screenshots of this project | ❌ Missing                          |

The `InventoryDW` folder has been retained because **ETL is an essential Data Warehouse concept** and the material provides relevant practical examples.

It should **not** be interpreted as the original ETL implementation or screenshots of this main project.

---

# 🗂️ Repository Structure

```text
Data-Warehouse-Project/
│
├── 📁 Data Warehouse Diagrams/
│   └── Warehouse architecture & design diagrams
│
├── 📁 Data Warehouse Documents/
│   └── Project documentation
│
├── 📁 ETL Process (InventoryDW)/
│   └── ⚠️ Supplementary ETL material
│      from a separate InventoryDW project
│
├── 📁 SQL Showcase/
│   └── SQL queries & analytical demonstrations
│
└── 📄 README.md
```

---

# 💻 SQL Showcase

The SQL section demonstrates techniques useful for analyzing Data Warehouse data.

| SQL Concept         | Example Use                    |
| ------------------- | ------------------------------ |
| `SELECT`            | Retrieve data                  |
| `WHERE`             | Filter records                 |
| `ORDER BY`          | Sort results                   |
| `GROUP BY`          | Group analytical results       |
| `HAVING`            | Filter grouped results         |
| `JOIN`              | Combine related data           |
| Aggregate Functions | Calculate totals and averages  |
| Subqueries          | Perform nested analysis        |
| Nested Queries      | Complex data retrieval         |
| T-SQL               | SQL Server-specific operations |

---

# 📊 Analytical Workflow

```text
             SOURCE DATA
                  │
                  ▼
                ETL
                  │
                  ▼
        ┌──────────────────┐
        │  DATA WAREHOUSE  │
        └────────┬─────────┘
                 │
       ┌─────────┼─────────┐
       ▼         ▼         ▼
     FACT    DIMENSIONS   DATA
    TABLES     TABLES    MODEL
       │         │         │
       └─────────┼─────────┘
                 ▼
          ANALYTICAL SQL
                 │
                 ▼
          AGGREGATION &
             ANALYSIS
```

---

# 🛠️ Technologies & Tools

| Technology                       | Usage                                       |
| -------------------------------- | ------------------------------------------- |
| **Microsoft SQL Server**         | Database & Data Warehouse platform          |
| **T-SQL**                        | SQL Server querying                         |
| **SQL Server Management Studio** | Database development and management         |
| **SQL**                          | Data analysis and querying                  |
| **ETL**                          | Data extraction, transformation and loading |
| **Dimensional Modeling**         | Analytical database design                  |

---

# 🧠 Skills Demonstrated

### Database

* Relational Database Concepts
* Primary & Foreign Keys
* Relationships
* SQL Queries
* Joins
* Aggregations
* Subqueries

### Data Warehousing

* Data Warehouse Architecture
* Fact Tables
* Dimension Tables
* Star Schema
* Dimensional Modeling
* OLAP Concepts
* Analytical Data Modeling

### Data Engineering

* ETL
* Data Extraction
* Data Transformation
* Data Loading
* Data Integration
* Data Preparation
* Analytical Data Processing

---

# 📚 Project Scope

This project focuses on the fundamental concepts involved in building and working with a **SQL Server Data Warehouse**.

The main areas covered are:

```text
Data Warehouse
      │
      ├── Architecture
      ├── Dimensional Modeling
      ├── Fact & Dimension Tables
      ├── ETL
      ├── SQL
      ├── Analytical Queries
      └── Data Analysis
```

The repository is primarily intended to demonstrate **database, Data Warehouse, SQL, and data-engineering knowledge**.
