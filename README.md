# 🛒 Global Retail Sales & Profit Intelligence Dashboard (AdventureWorks DW)
### Enterprise Relational Data Modeling & Financial BI in Microsoft Excel | Power Query • Power Pivot • DAX • Star Schema

[![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![Power Pivot](https://img.shields.io/badge/Power_Pivot-xVelocity_In--Memory-green?style=for-the-badge)](https://support.microsoft.com/en-us/office/power-pivot-overview-and-learning-f3cacf4b-7e18-4e8c-8e39-2a91289196b0)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-orange?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power_Query-M_Code_ETL-yellow?style=for-the-badge)]()
[![Domain](https://img.shields.io/badge/Domain-Retail_E--Commerce_&_Merchandising-blue?style=for-the-badge)]()

---

## 📌 Executive Summary
In global retail and e-commerce enterprises, managing multi-tier product catalogs, monitoring gross profit margins, and identifying inventory deadweight are essential for maintaining healthy cash flows and capital efficiency. Traditional spreadsheet reporting often relies on slow, denormalized flat sheets with fragile `VLOOKUP` formulas that cause workbook crashes and severe maintenance overhead.

This project delivers an enterprise-grade **Global Retail Sales & Profitability Intelligence Solution** built entirely inside **Microsoft Excel using Power Query, Power Pivot, and DAX**. Analyzing **60,400 sales transactions generating $307.09M in revenue and $126.29M in profit (41.1% margin)** across 18,484 customers, this system uncovered that **448 of 606 catalog products (73.9%) were completely unsold dead inventory**, while the **50+ age cohort drove 53.56% ($67.65M) of total enterprise profit**.

---

## 🖥️ Executive Dashboard Previews

### 1️⃣ Time Analysis Dashboard
![Time Analysis Dashboard](dashboard_time_analysis.png)

### 2️⃣ Details Analysis & Deep-Dive Dashboard
![Details Analysis Dashboard](dashboard_details_view.png)

---

## 🎯 Business Problem & Core Objectives
1. **Relational Enterprise Modeling:** Avoid denormalized single-sheet data dumping by building a clean star-schema relational model with one-to-many relationships inside Power Pivot.
2. **Catalog & Inventory Diagnostic:** Audit catalog performance to distinguish active revenue-generating SKUs from stagnant dead inventory.
3. **Temporal & Seasonal Profitability:** Analyze profit volatility across years, quarters, months, and weekday vs. weekend shopping cycles.
4. **Demographic & Pricing Sensitivity:** Uncover customer age concentration, gender profit splits, and high-ticket (> $150) price elasticity.
5. **C-Suite Interactive Presentation:** Design a two-page executive dashboard (Time Analysis & Details Analysis) with KPI cards, slicers, dynamic narrative callouts, and button navigation.

---

## 📊 Core Financial & Retail KPI Snapshot

| Metric Category | Key Performance Indicator (KPI) | Portfolio Result | Business Context / Finding |
| :--- | :--- | :--- | :--- |
| **Sales Scale** | Total Transactions (#Transaction) | **60,400 orders** | Complete multi-year transactional ledger |
| **Gross Volume** | Total Revenue | **$307,090,000.00** | Net sales volume across 6 global markets |
| **Cost Exposure** | Cost of Goods Sold (COGS) | **$180,800,000.00** | Direct product inventory manufacturing cost |
| **Bottom-Line** | Total Profit | **$126,290,000.00** | Gross operating profit |
| **Margin Health** | Profit Margin % | **41.1%** | Solid retail profit margin |
| **Order Scale** | Total Order Quantity | **631,920 units** | Total physical units shipped |
| **Catalog Health** | Total Catalog Products | **606 items** | Full active catalog |
| **Active SKUs** | Sold Products | **158 products (26.1%)** | Active revenue drivers |
| **Dead Stock** | **Unsold Products (Dead Inventory)** | **448 products (73.9%)** | ⚠️ Severe inventory capital lockup |
| **Customer Scale**| Total Active Customers | **18,484 accounts** | Average customer age: 47 years |
| **Key Demographic**| **50+ Age Group Profit Contribution** | **53.56% ($67.65M)** | 🎯 Primary high-margin customer persona |
| **Top Territories**| **United States & Australia** | **62.74% of Profit** | US ($41M) and Australia ($39M) dominant |
| **Pricing Skew** | **Expensive Products (> $150)** | **95.43% ($120.52M)** | Luxury/high-ticket equipment dependency |

---

## 🏗️ Data Architecture & Power Pivot Star Schema

The analytical model was engineered inside **Excel's Power Pivot xVelocity In-Memory Engine**:

```text
FactInternetSales (60,400 Transactions)
│
├── DimProduct (606 Products: ProductKey, Product Name, Color, Model)
├── DimCustomer (18,484 Customers: CustomerKey, BirthDate, Gender, Age-Group)
├── DimDate (Calendar Dimension: Date, Year, Month, WeekTypes, Quarter, Day of Week)
├── DimSalesTerritory (SalesTerritoryKey, Region, Country, Group)
└── DimGeography (GeographyKey, City, Country, State) ──► DimCustomer
