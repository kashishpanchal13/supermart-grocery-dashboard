# Supermarket Sales Analysis Dashboard

An interactive Excel dashboard that turns a raw supermarket sales dataset into clear KPIs, category and outlet comparisons, and statistical insights, helping management identify top performers and areas that need improvement.

## Business Context

A supermarket company's sales data existed only as a raw dataset, which made it hard to identify best-selling products, compare outlet performance, and understand sales patterns. This project analyzes that data in Excel and presents the results in an interactive dashboard for management.

## Dataset

- **File:** `Supermarket_Sales_Analysis_Dashboard.xlsx` (sheet: `BlinkIT Grocery Data`)
- **Size:** 8,523 records, 12 columns
- **Covers:** 16 product categories and 10 outlets across 4 outlet types and 3 location tiers

See the [data dictionary](docs/data_dictionary.md) for column descriptions.

## Objectives and Key Findings

### 1. Overall Sales Performance

| Metric | Value |
|---|---|
| Total sales revenue | 1,201,681 |
| Average sales per record | 140.99 |
| Average item visibility | 0.0661 (6.6%) |

### 2. Product Category and Sales Comparison

- **Top 4 categories contribute 50.6% of total sales**; all remaining 12 categories contribute 49.4%. The top four are Fruits and Vegetables (14.8%), Snack Foods (14.6%), Household (11.3%), and Frozen Foods (9.9%).
- **Highest-selling category:** Fruits and Vegetables (178,124). **Lowest:** Seafood (9,078).
- **By outlet type:** Supermarket Type1 leads with 787,550 (65.5%), followed by Grocery Store 151,939 (12.6%), Supermarket Type2 131,478 (10.9%), and Supermarket Type3 130,715 (10.9%). Type1 leads mainly because it has 6 of the 10 outlets; per-outlet sales are nearly equal for all supermarket outlets (about 130,000 to 133,000).

### 3. Outlet Performance and Sales Relationships

- **Low Fat vs Regular:** Low Fat items account for 64.6% of sales (776,320) and Regular for 35.4% (425,362). The roughly 2:1 split holds in every outlet.
- **Top and bottom outlets:** OUT035 is the top outlet (133,104). The two Grocery Stores, OUT010 (78,132) and OUT019 (73,808), have the lowest sales.
- **Visibility vs sales:** there is **no meaningful relationship** (correlation of about -0.001). Average sales stay flat at roughly 138 to 145 across all visibility levels, so higher shelf visibility does not translate into higher sales in this data.
- **Category mix by outlet type:** the mix is very similar across outlet types. Fruits and Vegetables and Snack Foods make up about 29 to 31% of sales everywhere. Meat has a larger share in Grocery Stores and Type3 (6.0%) than in Type1 (4.6%).

### 4. Statistical Analysis of Sales

| Statistic | Value |
|---|---|
| Average | 140.99 |
| Median | 143.01 |
| Minimum | 31.29 |
| Maximum | 266.89 |
| Standard deviation | 62.28 |
| Variance | 3,878.18 |
| Coefficient of variation | 44.2% |

- **Variation:** sales values are widely spread (standard deviation is about 44% of the mean), but the distribution is fairly symmetric since the mean and median are close.
- **Unusual values:** using the IQR method (Q1 = 93.83, Q3 = 185.64, bounds -43.90 to 323.37), **no records are outliers**.
- **Average sales differences:**
  - By category: highest for Household (149.42), Dairy (148.50), and Starchy Foods (147.84); lowest for Baking Goods (126.38), Health and Hygiene (130.82), and Soft Drinks (131.49).
  - By outlet type: nearly identical, between 139.80 and 141.68.
  - By location tier: nearly identical, between 140.87 and 141.17. Tier 3 has the highest total sales (472,133, 39.3%) simply because it has the most records.

## Recommendations

- **Protect the core categories.** Fruits and Vegetables, Snack Foods, Household, and Frozen Foods drive half of sales, so keep them well stocked.
- **Review low-volume categories** such as Seafood, Breakfast, and Starchy Foods, either to grow them or to reduce shelf space.
- **Focus on increasing sales per outlet** at the two Grocery Stores, which sell about 40% less than the supermarket outlets.
- **Rethink visibility-based promotion.** Since visibility shows no link to sales, extra shelf space alone is unlikely to lift revenue.
- **Check low-average categories** (Baking Goods, Health and Hygiene, Soft Drinks) for pricing or assortment issues.

## Data Cleaning

- Standardized `Item Fat Content` from 5 labels (`Low Fat`, `LF`, `low fat`, `Regular`, `reg`) to 2 (`Low Fat`, `Regular`).
- Found 1,463 missing `Item Weight` values (17.2%); not used in the analysis.
- Found 526 records (6.2%) with an `Item Visibility` of 0, which likely means missing data rather than truly zero visibility; kept in the analysis.
- Checked for duplicate records: none found.

## Tech Stack

- **Microsoft Excel**: PivotTables, PivotCharts, Slicers, conditional formatting
- **Formulas used:** `SUM`, `AVERAGE`, `MEDIAN`, `MIN`, `MAX`, `STDEV.S`, `VAR.S`, `QUARTILE`, `CORREL`, `SUMIFS`

## Project Structure

```
supermarket-sales-analysis-dashboard/
├── dashboard/
│   └── Supermarket_Sales_Analysis_Dashboard.xlsx
├── docs/
│   ├── data_dictionary.md
│   └── Supermarket_Sales_Analysis_Req.pdf   # Project requirements
├── screenshots/                              # Dashboard images
└── README.md
```

## How to Use

1. Download or clone the repository:
   ```bash
   git clone https://github.com/<your-username>/supermarket-sales-analysis-dashboard.git
   ```
2. Open `dashboard/Supermarket_Sales_Analysis_Dashboard.xlsx` in Microsoft Excel.
3. Use the slicers to filter by category, outlet type, and location.

## Screenshots

```md
![Dashboard Overview](screenshots/overview.png)
```

## Author

**Your Name**
GitHub: [@your-username](https://github.com/your-username)

## License

This project is for educational purposes.
