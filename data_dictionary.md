# Data Dictionary

Dataset: sheet `BlinkIT Grocery Data` in `Supermarket_Sales_Analysis_Dashboard.xlsx` (8,523 records).

| Column | Type | Description |
|---|---|---|
| `Item Fat Content` | Text | Fat content of the item. Raw values are `Low Fat`, `LF`, `low fat`, `Regular`, `reg`; cleaned to `Low Fat` and `Regular` |
| `Item Identifier` | Text | Unique product ID |
| `Item Type` | Text | Product category (16 categories, e.g. Fruits and Vegetables, Snack Foods, Dairy) |
| `Outlet Establishment Year` | Integer | Year the outlet was established |
| `Outlet Identifier` | Text | Unique outlet ID (10 outlets, e.g. `OUT035`) |
| `Outlet Location Type` | Text | Location tier of the outlet: Tier 1, Tier 2, or Tier 3 |
| `Outlet Size` | Text | Size of the outlet: Small, Medium, or High |
| `Outlet Type` | Text | Grocery Store, Supermarket Type1, Supermarket Type2, or Supermarket Type3 |
| `Item Visibility` | Number | Share of display area allocated to the item in the outlet. 526 records have a value of 0 |
| `Item Weight` | Number | Weight of the item. 1,463 values are missing |
| `Sales` | Number | Sales value of the item record |
| `Rating` | Number | Customer rating of the item (1 to 5) |

## Notes

- Each record is one item in one outlet, so "average sales per record" is the average sales value of an item-outlet record.
- No currency is specified in the source data, so sales figures are shown without a currency symbol.
