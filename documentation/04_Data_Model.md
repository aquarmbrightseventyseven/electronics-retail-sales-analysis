# 04 — Data model

## Schema type

The model is a simplified star schema. `Sales_Data` is the central fact table at the product-line-item grain. `Order` is a dimension/summary table at the order grain. Two auto-generated date tables support time intelligence on `Order Date`.

---

## Tables

### Fact table

#### `Sales_Data`
One row per product line item within an order.

| Column | Data type | Description |
|--------|-----------|--------------|
| Order ID | Integer | Order identifier (join key to `Order`) |
| Product | Text | Product name |
| Quantity Ordered | Integer | Units of this product in the line item |
| Price Each | Decimal | Unit price |
| Order Date | Date/Time | Timestamp of the order |
| Purchase Address | Text | Full delivery address |
| City | Text | Extracted city + state (e.g. "Boston (MA)") |
| Amount | Decimal | Quantity Ordered × Price Each |
| Hour | Integer | Hour of day order was placed (0–23) |
| Month | Integer | Month number (1–12) |
| Month Name | Text | Month name (e.g. "January") |
| Quarter | Text | Quarter label (e.g. "Qtr 1") |
| Day Num | Integer | Day of week number |
| Day Name | Text | Day name (e.g. "Monday") |
| Order Day | Text | 3-letter day abbreviation (calculated) |
| Name of Month | Text | 3-letter month abbreviation (calculated) |

---

### Dimension table

#### `Order`
One row per unique order.

| Column | Data type | Description |
|--------|-----------|--------------|
| Order ID | Integer | Order identifier (join key) |
| Count | Integer | Number of line items in the order |
| Product Listing | Text | Calculated: comma-separated list of all products in the order |

---

### System tables (auto-generated, hidden)

| Table | Description |
|-------|--------------|
| `DateTableTemplate_*` | Power BI's default date table template |
| `LocalDateTable_*` | Auto-generated local date table linked to `Sales_Data[Order Date]` |

Both contain standard date hierarchy columns: Date, Year, MonthNo, Month, QuarterNo, Quarter, Day.

---

## Relationships

| From table (many) | From column | To table (one) | To column | Direction |
|--------------------|-------------|------------------|-----------|-----------|
| Sales_Data | Order ID | Order | Order ID | One-direction |

---

## Model diagram (text representation)

```
[Order] ←──────────── [Sales_Data] 
  (Order ID)          (fact table,
                        one-direction)
```
