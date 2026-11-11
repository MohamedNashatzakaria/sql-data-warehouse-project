# SQL Data Warehouse Project

A modern data warehouse built in SQL Server, using the Medallion Architecture (Bronze, Silver, Gold). Raw CSV files from two source systems (CRM and ERP) are loaded, cleaned, and modeled into a star schema ready for analytics.

> Based on the [SQL Data Warehouse Project](https://github.com/DataWithBaraa/sql-data-warehouse-project) by Data With Baraa (MIT License). Built by me as part of my data analytics learning.

---

## 🏗️ Data Architecture

![Data Architecture](docs/data_architecture.png)

1. **Bronze Layer**: raw data as-is from the source CSV files, loaded into SQL Server.
2. **Silver Layer**: cleansing, standardization, and normalization.
3. **Gold Layer**: business-ready star schema for reporting and analysis.

---

## 📂 Repository Structure

```
sql-data-warehouse-project/
├── datasets/           source files
│   ├── source_crm/     3 CRM files
│   └── source_erp/     3 ERP files
├── docs/               architecture, data flow, data model, data catalog, naming conventions
├── scripts/
│   ├── init_database.sql
│   ├── bronze/         DDL + load procedure
│   ├── silver/         DDL + clean/load procedure
│   └── gold/           views for dimensions and facts
├── tests/              data quality checks (silver and gold)
└── README.md
```

---

## 🚀 Project Requirements

### Data Engineering
- **Sources**: ERP and CRM, provided as CSV files.
- **Data quality**: clean and fix issues before analysis.
- **Integration**: combine both sources into one analytical data model.
- **Scope**: latest data only, no historization.
- **Documentation**: clear data model docs for business and analytics teams.

### Data Analysis
SQL-based analytics covering:
- Customer behavior
- Product performance
- Sales trends

---

## 🔄 What I Built

| Layer | What I did |
|:--|:--|
| Bronze | Created tables, bulk loaded 6 CSV files with a stored procedure |
| Silver | Cleaned 6 tables: duplicates, nulls, invalid dates, standardized values |
| Gold | Built `dim_customers`, `dim_products`, `fact_sales` as a star schema |
| Tests | Quality checks for silver and gold layers |

---

## ⚙️ How to Run

1. Install SQL Server and SSMS.
2. Place the `datasets/` folder on your machine and update the file paths in `scripts/bronze/proc_load_bronze.sql`.
3. Run `scripts/init_database.sql` to create the database and schemas.
4. Run the bronze, silver, and gold scripts in order.
5. Run the scripts in `tests/` to validate the data.

---

## 🛠️ Tools

- SQL Server and SSMS
- Git and GitHub
- draw.io (architecture and data model diagrams)
- Notion (project plan)

---

## 📸 Diagrams

- Data flow: `docs/data_flow.png`
- Data model (star schema): `docs/data_model.png`
- Data catalog: `docs/data_catalog.md`

---

## 🤝 Connect

**Mohamed Nashat**
- LinkedIn: https://www.linkedin.com/in/mohamed-nashat-298998191/
- GitHub: https://github.com/MohamedNashatzakaria
- Email: mohamednashat313@gmail.com

## 🛡️ License

[MIT](LICENSE). Original project by [Data With Baraa](https://github.com/DataWithBaraa/sql-data-warehouse-project).
