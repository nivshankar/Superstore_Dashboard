<div align="center">

# -- ! Superstore Sales Dashboard ! --
### *Interactive Power BI Analytics — Sales, Profit & Quantity Performance Overview*

[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures_%26_KPIs-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Microsoft_Excel-Source_Data-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![Data Model](https://img.shields.io/badge/Data_Model-Relational_Design-0078D4?style=for-the-badge&logo=powerbi&logoColor=white)](https://powerbi.microsoft.com/)

<br/>

> *"Data isn't just numbers on a grid — visualize it well, and it becomes a strategy that drives decisions."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🗂️ Dataset — Superstore.csv](#️-dataset--superstorecsv)
- [🔺 Part A — Executive Dashboard](#-part-a--executive-dashboard)
- [🔢 Part B — Data Table View](#-part-b--data-table-view)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Superstore Sales Dashboard** is a fully interactive Power BI report built on the classic Superstore retail dataset. Loaded from `Superstore.csv` into Power BI Desktop, it delivers executive-level visibility into sales performance, profit distribution, order quantities, and discount behaviour — all filterable in real time by **Region**, **Category**, and **Period** using dropdown slicers.

The report is organised into two pages — a **Dashboard** page for visual KPIs and charts, and a **Table** page for granular order-level data exploration.

This project is designed to:
- Aggregate 9,994 order records into clear, high-level KPI metric cards
- Visualise total sales and profit breakdowns across product categories and regions
- Enable real-time interactive filtering through Power BI dropdown slicers
- Provide a drillable data table for detailed order and customer-level exploration

---

## 🎯 Problem Statement

> **Objective:** Build an interactive Power BI executive dashboard to monitor total sales, profit, quantity, and discount metrics across product categories and regions for a US retail superstore.

Retail organisations dealing with thousands of orders across multiple regions, categories, and customer segments need a single consolidated view to quickly identify top-performing areas, under-performing regions, and category-level revenue gaps.

| 📂 Feature | 📄 Type | 🔍 Description |
|------------|---------|----------------|
| KPI Summary Cards | Metric Display | Sum of Sales, Total Profit, Sum of Quantity, Average Discount |
| Total Sales by Category | Bar Chart | Horizontal bars comparing Technology, Furniture, Office Supplies |
| Total Profit by Region | Bar Chart | Horizontal bars ranking West, East, South, Central by profit |
| Interactive Slicers | Filter Controls | Dropdown filters for Region, Category, and Period |
| Data Table Page | Detail View | Full order-level grid with Category, City, Customer, Product, Sales, Discount, and more |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 🎛️ **3 Dropdown Slicers** | Real-time filtering by Region (All/Central/East/South/West), Category, and Period |
| 🏷️ **4 Dynamic KPI Cards** | Sum of Sales, Total Profit, Sum of Quantity, Average Discount — update with every filter |
| 📊 **Dual Bar Chart Layout** | Side-by-side horizontal charts for Sales by Category and Profit by Region |
| 🔴⬛ **Dual-Tone Colour Scheme** | Red bars for top performers, black bars for secondary metrics — clean visual hierarchy |
| 📋 **Full Data Table Page** | Scrollable detail grid with 12+ columns including Customer ID, Order ID, Product Name, Sum of Discount, Year, Quarter, Month |
| 🌍 **4-Region Coverage** | West, East, South, Central — all regions represented and filterable |
| 📦 **3-Category Coverage** | Technology, Furniture, Office Supplies |
| 👥 **3-Segment Dataset** | Consumer, Corporate, and Home Office customer segments |
| 📅 **Multi-Year Data** | Orders spanning 2014–2017 with Quarter and Month breakdowns in the Table view |
| 🔄 **Two Report Pages** | Dashboard page for executive overview, Table page for raw data exploration |

---

## 🏗️ Project Structure

```
📦 Superstore-Dashboard/
│
├── 📊 SuperStore_Dashboard.pbix     ← Power BI report file (2 pages: Dashboard + Table)
├── 🗂️ Superstore.csv                ← Source data: 9,994 order records, 21 columns
│
├── 📁 Assets/                       ← Screenshot assets for documentation
│   ├── 🖼️ Dashboard.png             ← Screenshot of Dashboard page
│   └── 🖼️ Table.png                 ← Screenshot of Table page
│
└── 📄 README.md                     ← Project documentation
```

> **How to open:**
> ```
> 1. Install Power BI Desktop (free): https://powerbi.microsoft.com/desktop
> 2. Open SuperStore_Dashboard.pbix in Power BI Desktop
> 3. If prompted, re-point the data source to Superstore.csv
> 4. Use the Region, Category, and Period slicers to explore the dashboard
> ```

---

## 🔄 Project Workflow

```
Superstore.csv  (9,994 rows × 21 columns)
       │
       ▼  Import into Power BI Desktop
  Data Model
       │
       ├──▶  DAX Measures Created
       │     Sum of Sales · Total Profit · Sum of Quantity · Average Discount
       │
       ├──▶  Page 1: Dashboard
       │     ├── 3 Dropdown Slicers (Region / Category / Period)
       │     ├── 4 KPI Cards (Sales / Profit / Quantity / Avg Discount)
       │     ├── Horizontal Bar Chart → Total Sales by Product Category
       │     └── Horizontal Bar Chart → Total Profit by Region
       │
       └──▶  Page 2: Table
             └── Full data grid (Category, City, Customer, Order, Product, Sales, etc.)
```

---

## 🗂️ Dataset — Superstore.csv

| Column | Type | Description |
|--------|------|-------------|
| `Row ID` | `int` | Unique row identifier |
| `Order ID` | `str` | Unique order reference |
| `Order Date` | `date` | Date the order was placed |
| `Ship Date` | `date` | Date the order was shipped |
| `Ship Mode` | `str` | Shipping method: Standard Class, Second Class, First Class, Same Day |
| `Customer ID` | `str` | Unique customer identifier |
| `Customer Name` | `str` | Full name of the customer |
| `Segment` | `str` | Customer segment: Consumer, Corporate, Home Office |
| `Country` | `str` | Country (United States) |
| `City` | `str` | City of the order destination |
| `State` | `str` | State of the order destination |
| `Postal Code` | `int` | ZIP code |
| `Region` | `str` | Geographic region: Central, East, South, West |
| `Product ID` | `str` | Unique product identifier |
| `Category` | `str` | Product category: Furniture, Office Supplies, Technology |
| `Sub-Category` | `str` | Product sub-category (17 sub-categories) |
| `Product Name` | `str` | Full product name |
| `Sales` | `float` | Order line revenue in USD |
| `Quantity` | `int` | Number of units ordered |
| `Discount` | `float` | Discount rate applied (0.0–1.0) |
| `Profit` | `float` | Profit generated on the order line |

**Dataset Summary:**

| Metric | Value |
|--------|-------|
| Total Records | 9,994 orders |
| Total Sales | ₹ 2.30M (2,297,200.86) |
| Total Profit | ₹ 286.397K (286,397.02) |
| Total Quantity | 38K (37,873 units) |
| Average Discount | 0.16 (16%) |
| Date Range | 2014 – 2017 |
| Regions | 4 (Central, East, South, West) |
| Categories | 3 (Furniture, Office Supplies, Technology) |
| Customer Segments | 3 (Consumer, Corporate, Home Office) |
| Ship Modes | 4 (Standard Class, Second Class, First Class, Same Day) |

**Sales by Category:**

| Category | Total Sales |
|----------|------------|
| Technology | ₹ 836,154.03 |
| Furniture | ₹ 741,999.80 |
| Office Supplies | ₹ 719,047.03 |

**Profit by Region:**

| Region | Total Profit |
|--------|-------------|
| West | ₹ 108,418.45 |
| East | ₹ 91,522.78 |
| South | ₹ 46,749.43 |
| Central | ₹ 39,706.36 |

**Top 5 Sub-Categories by Sales:**

| Sub-Category | Total Sales |
|-------------|------------|
| Phones | ₹ 330,007.05 |
| Chairs | ₹ 328,449.10 |
| Storage | ₹ 223,843.61 |
| Tables | ₹ 206,965.53 |
| Binders | ₹ 203,412.73 |

---

## 🔺 Part A — Executive Dashboard

### 📝 1. Dashboard Architecture

The Dashboard page consolidates all key performance metrics into a clean, executive-ready single-screen layout with interactive slicers at the top, four KPI cards below, and two side-by-side bar charts at the bottom.

![Superstore Sales Dashboard](Dashboard.png)

---

### 🗺️ 2. Core Dashboard KPI Cards

The four KPI cards sit below the slicers and update dynamically whenever a slicer selection is changed:

| KPI Card | Value (All Filters) | Description |
|----------|--------------------|----|
| 💰 **Sum of Sales** | **₹ 2.30M** | Total revenue across all orders |
| 📈 **Total Profit** | **₹ 286.397K** | Net profit across all order lines |
| 📦 **Sum of Quantity** | **38K** | Total units sold |
| 🏷️ **Average Discount** | **0.16** | Mean discount rate across all transactions |

---

### 🎛️ 3. Interactive Slicers

Three dropdown slicers at the top of the dashboard control all visuals simultaneously:

| Slicer | Options | Effect |
|--------|---------|--------|
| **Region** | All / Central / East / South / West | Filters all 4 KPI cards and both charts by region |
| **Category** | All / Furniture / Office Supplies / Technology | Narrows KPIs and charts to one product category |
| **Period** | All / (Year/Quarter/Month options) | Filters the entire report to a specific time period |

---

### 📊 4. Total Sales by Product Category (Bar Chart)

The left chart shows horizontal bars for each of the three product categories ranked by total sales:

| Category | Total Sales |
|----------|------------|
| 🔴 **Technology** | **₹ 0.84M** — top bar (red) |
| ⬛ **Furniture** | **₹ 0.74M** — second bar (black) |
| 🔴 **Office Supplies** | **₹ 0.72M** — third bar (red) |

Technology leads revenue at ₹ 0.84M, with Furniture and Office Supplies closely following at ₹ 0.74M and ₹ 0.72M respectively.

---

### 📊 5. Total Profit by Region (Bar Chart)

The right chart shows horizontal bars for each region ranked by total profit:

| Region | Total Profit |
|--------|-------------|
| 🔴 **West** | **₹ 108K** — top bar (red) |
| ⬛ **East** | **₹ 92K** — second bar (black) |
| 🔴 **South** | **₹ 47K** — third bar (red) |
| ⬛ **Central** | **₹ 40K** — fourth bar (black) |

West leads all regions with ₹ 108K profit — nearly 3× the Central region's ₹ 40K.

---

## 🔢 Part B — Data Table View

### 🔍 6. Full Order-Level Data Table

The Table page provides a complete scrollable grid of all order records for detailed exploration. It is accessible via the **Table** tab at the bottom of the Power BI report.

![Data Table View](Table.png)

**Columns visible in the Table page:**

| Column | Description |
|--------|-------------|
| `Category` | Product category (Furniture shown by default sort) |
| `City` | Destination city |
| `Country` | Country of order (United States) |
| `Customer ID` | Unique customer identifier |
| `Customer Name` | Full customer name |
| `Sum of Discount` | Aggregated discount for the row grouping |
| `Year` | Year of the order |
| `Quarter` | Quarter of the order (Qtr 1 – Qtr 4) |
| `Month` | Month name of the order |
| `Day` | Day of the order |
| `Order ID` | Unique order reference |
| `Count of Postal Code` | Aggregated postal code count |
| `Product ID` | Unique product identifier |
| `Product Name` | Full product name |
| `Sum of...` | Sales/Quantity aggregations per grouping |

The table is sorted by Category alphabetically (Furniture first), then by City, enabling drill-down exploration of specific customer-product-region combinations.

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 🟡 **Power BI Desktop** | Latest | Report authoring, data modelling, DAX, and publishing |
| 📐 **DAX** | Built-in | Measures for Sum of Sales, Total Profit, Sum of Quantity, Average Discount |
| 🎛️ **Power BI Slicers** | Built-in | Dropdown slicers for Region, Category, and Period filtering |
| 📊 **Power BI Bar Charts** | Built-in | Horizontal bar charts for category and region comparisons |
| 🗂️ **CSV / Excel** | Source | `Superstore.csv` — 9,994 rows, 21 columns of retail order data |
| 🎨 **Report Theme** | Custom | Light grey background, red/black dual-tone bar chart colour scheme |

---

## 📈 Results & Insights

| Insight | Value |
|---------|-------|
| 💰 Total Revenue | **₹ 2.30M** across 9,994 orders |
| 📈 Total Profit | **₹ 286.397K** (overall profit margin ~12.5%) |
| 📦 Total Units Sold | **38K** units |
| 🏷️ Average Discount | **16%** across all transactions |
| 🏆 Top Category by Sales | **Technology** — ₹ 0.84M |
| 🏆 Top Region by Profit | **West** — ₹ 108K |
| 📉 Lowest Profit Region | **Central** — ₹ 40K (63% lower than West) |
| 🔴 Most Profitable Sub-Cat | **Phones** — ₹ 330K in sales |
| 👥 Largest Customer Segment | **Consumer** — ₹ 1.16M in sales |
| 🚚 Most Used Ship Mode | **Standard Class** — 5,968 of 9,994 orders |
| 📅 Data Span | **2014 to 2017** (4 years) |

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 💼 **Executive Ready** | Clean, polished single-screen layout suitable for management presentations |
| ⚡ **Real-Time Filtering** | All 4 KPI cards and both charts update instantly with every slicer change |
| 🔀 **Dual-Page Structure** | Dashboard for high-level view, Table for granular order-level exploration |
| 🎨 **Consistent Visual Theme** | Red/black dual-tone bar charts with light grey background for easy reading |
| 🔗 **Scalable Data Model** | CSV-based import means the dashboard refreshes automatically when data is updated |
| 📊 **Multi-Dimension Analysis** | Simultaneously slice by Region, Category, and Period with no formula editing |
| 🖥️ **No Code Required** | Built entirely in Power BI Desktop — shareable as a `.pbix` file with no server setup |
| 🌍 **Complete Regional Coverage** | All 4 US retail regions (West, East, South, Central) visible and filterable |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Neev Shankar

> *"Data transformed into structure becomes insight; insight transformed into strategy becomes growth."*

**🎓 Role:** Data Analyst | Power BI & Excel Specialist \
**📍 Location:** India \
**🛠️ Skills:** Power BI · DAX · Microsoft Excel · Data Visualisation · Dashboard Design · Data Modelling

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/) — Official Power BI Desktop and DAX reference
- 🟡 [Microsoft Power BI Community](https://community.powerbi.com/) — Dashboard design tips and DAX guidance
- 📊 [Kaggle — Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) — Original Superstore retail dataset
- 🎓 [SQLBI — DAX Guide](https://dax.guide/) — DAX function and measure reference
- 💬 [Stack Overflow Community](https://stackoverflow.com/) — Problem-solving support
- 📖 [Chandoo.org](https://chandoo.org/) — Dashboard design guidelines and techniques

---

<div align="center">

---

*Made with ❤️ and ☕ — Last updated: 11 October, 2026*

</div>
