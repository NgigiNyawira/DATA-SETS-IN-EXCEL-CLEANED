#  Sales & Operations Analytics — Excel Mastery Project

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Records](https://img.shields.io/badge/Records-633%20Orders-blue?style=flat)
![Regions](https://img.shields.io/badge/Regions-4%20Global-orange?style=flat)
![Years](https://img.shields.io/badge/Period-2023--2025-purple?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

A multi-regional electronics distributor dataset built for end-to-end Excel analytics — covering data cleaning, cohort analysis, SKU performance, salesperson productivity, scenario modeling, and an interactive dashboard.

---

## Dashboard Preview

> The workbook includes a fully built **interactive Dashboard** sheet with KPI cards, slicers, and charts across Revenue, Profit, Regions, Channels, and Salesperson performance.

---

##  File Structure

The workbook (`Sales_and_operations_data_set.xlsx`) contains **9 sheets**:

| Sheet | Description |
|---|---|
| `Data` | Cleaned & enriched raw dataset — 633 rows × 34 columns |
| `Brief` | Original assignment brief with all task requirements |
| `monthly revenue from start date` | Cohort analysis: revenue tracked per country from first-sale month |
| `sku` | ABC analysis — SKUs classified into A/B/C tiers by gross revenue |
| `person productivity` | Salesperson KPIs: Revenue/Order, Orders/Month, Profit/Order |
| `revenue shares by Channel` | Channel mix analysis and regional cannibalization insights |
| `7 lead time days` | Service level: % of orders meeting the ≤7-day lead time target |
| `SHARE of orders with >20%` | Price compliance: discount outliers by Region and Salesperson |
| `Dashboard` | Interactive single-page dashboard with slicers and dynamic visuals |

---

##  Dataset Schema

The main `Data` sheet contains **633 rows × 34 columns**:

### Core Order Fields
| Column | Type | Description |
|---|---|---|
| `OrderID` | Text | Unique order identifier (e.g., `ORD-2024-275203`) |
| `OrderDate` | Date | Date order was placed |
| `RequiredDate` | Date | Original requested delivery date |
| `Corrected od` | Date | Cleaned order date after data quality fixes |
| `corrected rd` | Date | Corrected required date (RequiredDate ≥ OrderDate enforced) |
| `Lead time days` | Integer | Days between order and required date |

### Geography & Customer
| Column | Type | Description |
|---|---|---|
| `Region` | Text | Global region (Africa, Asia, Americas, Europe) |
| `Country` | Text | 12 countries including Kenya, Brazil, Germany, Japan, USA |
| `City` | Text | 40 cities |
| `CustomerSegment` | Text | Corporate, Education, Non-Profit, Consumer, Small Business, Enterprise |
| `Channel` | Text | Direct, Online, Retail, Distributor, Marketplace |
| `Salesperson` | Text | 16 sales representatives |

### Product & Pricing
| Column | Type | Description |
|---|---|---|
| `ProductCategory` | Text | Components, Printers, Networking, Phones, Laptops, Monitors, Accessories |
| `SKU` | Text | Unique product identifier |
| `UnitCost` | Float | Cost per unit (USD) |
| `UnitPrice` | Float | Selling price per unit (USD) |
| `DiscountPct` | Float | Discount applied as a decimal (e.g., `0.20` = 20%) |
| `Quantity` | Integer | Units ordered |
| `Price band` | Text | Derived price tier: Low / Medium / High |

### Calculated Financial Metrics
| Column | Type | Formula |
|---|---|---|
| `Gross revenue` | Float | `UnitPrice × Quantity × (1 − DiscountPct)` |
| `Cost of goods` | Float | `UnitCost × Quantity` |
| `Gross profit` | Float | `Gross revenue − Cost of goods` |
| `Margin pct` | Float | `Gross profit / Gross revenue` |

### Derived Dimensions & Scenario Modeling
| Column | Description |
|---|---|
| `Month` / `QUARTER` | Time dimensions derived from OrderDate |
| `year` / `month` | Numeric/text year and month |
| `Region.1` | Full region hierarchy: Region → Country → City |
| `7 lead time` | YES/NO flag for orders meeting ≤7-day lead time |
| `>20%DISCT` | YES/NO flag for orders with discount > 20% |
| `DISC CAP` | Scenario: revenue under a global discount cap |
| `UNIT INFLATION` | Scenario: adjusted unit cost under cost inflation |
| `Quantity Increase` / `qup` | Scenario: quantity uplift projections |

---

##  Key Statistics

| Metric | Value |
|---|---|
| Total Orders | 633 |
| Date Range | Jan 2023 – Sep 2025 |
| Regions | 4 (Africa, Asia, Americas, Europe) |
| Countries | 12 |
| Salespersons | 16 |
| Product Categories | 7 |
| Avg Lead Time | 14.4 days |
| Orders with > 20% Discount | 90 (14.2%) |
| Orders meeting ≤7-day target | 172 (27.2%) |

---

## Analysis Modules

### Part A — Data Cleaning & Preparation
- Removed duplicate rows and fixed data types
- Imputed missing values for `City`, `Salesperson`, and `Channel`
- Flagged and corrected negative prices and discounts > 30%
- Enforced `RequiredDate ≥ OrderDate` rule with corrections documented
- Calculated derived columns: `GrossRevenue`, `CostOfGoods`, `GrossProfit`, `MarginPct`

### Part B — Analysis Tasks
- **Cohort Analysis** — Monthly revenue by Country from each country's first-sale month
- **ABC Analysis** — SKUs ranked A (top 80%), B (next 15%), C (last 5%) of revenue per category
- **Salesperson Productivity** — Revenue/Order, Orders/Month, Profit/Order with top/bottom 3 highlighted
- **Channel Mix** — Revenue share by Channel across Regions; online vs. retail cannibalization analysis
- **Service Level Proxy** — % of orders hitting the ≤7-day lead time by Country and Category
- **Price Compliance** — Discount outlier identification by Region and Salesperson

### Part C — Scenario Modeling (What-If)
Three scenario levers modeled against the baseline:
- **Global Discount Cap** — 0% to 25%
- **Unit Cost Inflation** — 0% to 15%
- **Quantity Uplift** — 0% to 20%

### Part D — Interactive Dashboard
Single-page dashboard featuring:
- **Slicers**: Region, Country, Channel, Product Category, Month, Salesperson
- **KPIs**: Total Revenue, Gross Profit, Margin %, Avg Order Value, On-Time %
- **Visuals**: Revenue by Month (line), Profit by Region & Channel (stacked column), Top 10 SKUs (bar), Discount Outliers (scatter)

---

##  Geographic Coverage

| Region | Countries |
|---|---|
| Africa | Kenya, Nigeria, South Africa |
| Americas | Brazil, Canada, USA |
| Asia | China, India, Japan |
| Europe | France, Germany, United Kingdom |

---

##  Getting Started

1. Clone or download the repository
2. Open `Sales_and_operations_data_set.xlsx` in **Microsoft Excel 2016 or later** (slicers and PivotTables require a modern version)
3. Start with the **`Brief`** sheet to understand the full project scope
4. Navigate to the **`Dashboard`** sheet for the interactive overview
5. Use slicers to filter by Region, Channel, Category, or Salesperson

```bash
git clone https://github.com/your-username/sales-operations-analytics.git
cd sales-operations-analytics
```

---

##  Notes & Assumptions

- All monetary values are in **USD**
- Missing `Channel` values were imputed as `"Not provided"` where business logic could not determine the correct channel
- `RequiredDate` values earlier than `OrderDate` were corrected by adding the average lead time
- `DiscountPct` is stored as a decimal — multiply by 100 for percentage display
- Approximately 1–2% of rows contain nulls in geographic and salesperson fields

---

##  Tools Used

- **Microsoft Excel** — Data cleaning, PivotTables, formulas, scenario modeling, and dashboard design
- **Power Pivot / Data Model** — For cross-sheet measure calculations

---

##  License

Shared for **educational and portfolio purposes**. Dataset is synthetic and intended for Excel skills demonstration.

---

##  Author

> Built and maintained by **[Gloria Ngigi]**  
> Feel free to fork, star ⭐, or raise an issue with suggestions!
