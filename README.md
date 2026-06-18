# 🚗 TIROO – Tire & Battery Management System
> A full-scale Business Intelligence platform for a multi-branch tire & battery company, transforming raw operational data into actionable insights.

---

## 📌 Project Overview

**TIROO** is an end-to-end BI solution that covers the full data lifecycle — from a normalized operational database, through a Medallion Architecture Data Warehouse, to interactive dashboards and an AI-powered automated alert system.

The system was designed to solve real-world business challenges faced by multi-branch tire & battery retailers — including inventory tracking across locations, sales performance monitoring, customer behavior analysis, and automated low-stock alerting with zero manual intervention.

---

## 🏗️ Architecture

```
Operational DB (SQL Server)
        ↓
ETL Pipeline (SSIS)
        ↓
Data Warehouse – Medallion Architecture
  ├── Bronze Layer (Raw)
  ├── Silver Layer (Cleaned)
  └── Gold Layer (Star Schema – Sales, Inventory, Reservation Marts)
        ↓
Reporting & Visualization
  ├── SSRS Reports (6 operational reports)
  ├── Power BI Dashboards (3 data marts)
  └── Python Dashboard
        ↓
AI Automation (n8n + Groq AI) – Daily stock alerts via email
```

---

## 📁 Repository Structure

```
TIROO/
│
├── 📁 Database/
│   ├── Files/          # SQL scripts (schema + data)
│   └── Screenshots/    # ERD & schema diagrams
│
├── 📁 DWH_ETL_SSIS/
│   ├── Files/          # DWH SQL scripts + SSIS packages
│   └── Screenshots/    # Medallion architecture & star schema
│
├── 📁 SSRS/
│   ├── Files/          # SSRS report files (.rdl)
│   └── Screenshots/    # Report previews
│
├── 📁 power pi/
│   ├── Files/          # Power BI (.pbix) files
│   └── Screenshots/    # Dashboard screenshots
│
├── 📁 Python_Dashboard/
│   ├── Files/          # Python scripts
│   └── Screenshots/    # Dashboard previews
│
├── 📁 Automation/
│   ├── Files/          # n8n workflow (JSON)
│   └── Screenshots/    # Workflow & email alert screenshots
│
└── README.md
```

---

## 🛠️ Technologies Used

| Layer | Tools |
|---|---|
| Database | SQL Server, T-SQL |
| ETL | SSIS (SQL Server Integration Services) |
| Reporting | SSRS (SQL Server Reporting Services) |
| Visualization | Power BI, Python (matplotlib / plotly) |
| Automation | n8n, Groq AI |
| Design | ERD, Star Schema, Medallion Architecture |

---

## ✅ Key Features

- **15+ entity** normalized SQL Server operational database covering Products, Inventory, Orders, Customers, Employees, Payments, Reservations, and more
- **Medallion Architecture DWH** (Bronze → Silver → Gold) ensuring clean, reliable, analysis-ready data
- **3 Star Schema Data Marts** – Sales, Inventory, and Reservation — each optimized for a specific business domain
- **Fully Automated ETL Pipeline** using SSIS — extracting, transforming, cleaning, and loading data from operational sources into the warehouse
- **6 SSRS Operational Reports** – Brands, Inventory, Payments, Services, Customers, and Reserved Stock
- **Interactive Power BI Dashboards** covering Sales trends, Customer Behavior, Branch Performance, Inventory Levels, and Reservation Patterns
- **Python Dashboard** for additional inventory and branch-level visualizations
- **AI-Powered Automated Stock Alert System** — runs a daily check, detects low-stock items, groups alerts by branch, generates AI-structured priority reports via Groq AI, and sends email notifications to branch managers automatically 🤖

---

## 🎓 About

Business Intelligence Track | ITI Graduation Project | Class of 2025
