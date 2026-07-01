# 03 — Data preparation

## Source data

The primary source is a single transaction-level table: **`Sales_Data`**. Each row represents one product line item within an order (an order can contain multiple line items/products).

A supporting **`Order`** table aggregates `Sales_Data` to the order level, and Power BI auto-generated date dimension tables support time intelligence.

---

## Tables ingested via Power Query (M)

| Table | Source type | Description |
|-------|------------|--------------|
| `Sales_Data` | M query / import | Core transaction table — one row per product line item |
| `Order` | M query / import (with calculated column) | Order-level rollup: Order ID, line-item Count, and a concatenated Product Listing |
| `DateTableTemplate_*` | Calculated | Power BI auto-generated date table |
| `LocalDateTable_*` | Calculated | Power BI auto-generated local date table linked to `Order Date` |

---

## Key transformations applied

### `Sales_Data`

| Column | Transformation |
|--------|----------------|
| `Order ID` | Source order identifier |
| `Product` | Product name |
| `Quantity Ordered` | Units ordered in this line item |
| `Price Each` | Unit price |
| `Order Date` | Parsed to date/time type |
| `Purchase Address` | Raw delivery address string |
| `City` | Extracted from `Purchase Address` (e.g. "San Francisco (CA)") |
| `Amount` | Calculated: `Quantity Ordered × Price Each` |
| `Hour` | Extracted from `Order Date` time component |
| `Month` | Extracted month number |
| `Month Name` | Extracted text month name |
| `Quarter` | Calculated from month |
| `Day Num` | Extracted numeric day of week |
| `Day Name` | Extracted text day of week |
| `Order Day` | Calculated column: `UPPER(LEFT(Sales_Data[Day Name], 3))` — 3-letter day abbreviation |
| `Name of Month` | Calculated column: `UPPER(LEFT(Sales_Data[Month Name], 3))` — 3-letter month abbreviation |

### `Order`

| Column | Transformation |
|--------|----------------|
| `Order ID` | Order identifier (join key) |
| `Count` | Number of line items in the order |
| `Product Listing` | Calculated column: `CONCATENATEX` of all products in the order, comma-separated |

---

## Data quality notes

- Storage mode is **Import** across all tables — data is a snapshot at refresh time.
- The relationship from `Sales_Data` to `Order` is (Sales_Data → Order).
