#  Jumia Product Performance Dataset & Dashboard

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Dataset](https://img.shields.io/badge/Records-115%20Products-blue?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

A structured Excel dataset and interactive dashboard analyzing product pricing, discount strategies, customer reviews, and ratings scraped/compiled from **Jumia** — one of Africa's largest e-commerce platforms.

---

##  Dashboard Preview

> The workbook includes a fully built Excel Dashboard (`DashBoard` sheet) with charts and KPIs summarizing key product performance metrics.

---

## File Structure

The workbook (`_Excel_jumia_Data_set.xlsx`) contains **13 sheets**:

| Sheet | Description |
|---|---|
| `Excel_jumia` | Raw dataset — 115 products with pricing, discount, and review data |
| `Product vs Rating` | Chart: Product names plotted against their ratings |
| `Reviews vs Discount Percentage` | Chart: Relationship between review count and discount depth |
| `Rating vs Reviews` | Chart: Correlation between customer ratings and review volume |
| `Discount vs Customer Engagement` | Chart: How discounts influence engagement |
| `Product rating vs Reviews` | Combined analysis of ratings and reviews per product |
| `Discount vs Rating and Reviews` | Multi-axis discount impact analysis |
| `Top 10 Discounted Products` | Products offering the highest discounts |
| `Top 10 Reviewed Products` | Products with the most customer reviews |
| `Bottom 5 Lowest Rated Products` | Poorest performing products by rating |
| `Top 5 Highest Rated Products` | Best performing products by rating |
| `Product Performance Analysis` | Consolidated performance summary |
| `DashBoard` | Interactive visual dashboard |

---

## 🗂️ Dataset Schema

The main dataset (`Excel_jumia` sheet) contains **115 rows × 10 columns**:

| Column | Type | Description |
|---|---|---|
| `Product` | Text | Full product name/description |
| `Current Price` | Integer | Current selling price (KES) |
| `old price` | Integer | Original price before discount (KES) |
| `Discount Amt.` | Integer | Absolute discount amount (KES) |
| `Discount` | Float | Discount as a decimal (e.g., `0.45` = 45%) |
| `Discount Category` | Text | Bucketed discount tier |
| `Pos. Reviews` | Integer | Number of positive reviews |
| `Review` | Integer | Net review score |
| `Rating` | Float | Product rating (scale: 2.0 – 5.0) |
| `Rating Category` | Text | Bucketed rating tier |

---

## Key Statistics

| Metric | Value |
|---|---|
| Total Products | 115 |
| Price Range | KES 38 – KES 3,750 |
| Average Discount | ~36.8% |
| Highest Discount Tier | High Discount (62 products) |

### Discount Category Breakdown
| Category | Count |
|---|---|
| High Discount | 62 |
| Medium Discount | 32 |
| Low Discount | 18 |

### Rating Category Breakdown
| Category | Count |
|---|---|
| Excellent | 23 |
| Average | 22 |
| Poor | 12 |

---

##  Possible Use Cases

- **Price & Discount Analysis** — Understand how Jumia sellers structure discounts across product categories
- **Customer Sentiment** — Explore the relationship between review volume and rating quality
- **Product Ranking** — Identify top and bottom performers by engagement and rating
- **E-commerce Research** — Use as a baseline dataset for African e-commerce market studies
- **Data Visualization Practice** — Pre-built charts make it suitable for learning Excel dashboarding

---

##  Tools Used

- **Microsoft Excel** — Data cleaning, analysis, pivot charts, and dashboard design
- **Jumia Kenya** — Data source (e-commerce platform)

---

##  Getting Started

1. Clone or download the repository
2. Open `_Excel_jumia_Data_set.xlsx` in Microsoft Excel (2016 or later recommended)
3. Navigate to the **`DashBoard`** sheet for the visual overview
4. Explore individual chart sheets for focused analysis

```bash
git clone https://github.com/your-username/jumia-dataset.git
cd jumia-dataset
```

---

##  Notes

- Prices are in **Kenyan Shillings (KES)**
- Some rows have missing values in `old price`, `Pos. Reviews`, and `Review` columns (~2–3 missing entries)
- Rating scale appears to run from **2.0 to 5.0** based on the dataset
- Discount column is stored as a decimal — multiply by 100 for percentage display

---

##  License

This dataset is shared for **educational and analytical purposes only**. Product data belongs to their respective sellers on the Jumia platform.

---

## Author

> Built and maintained by **[Gloria Ngigi]**  
> Feel free to fork, star, or open an issue if you have suggestions!
