# 02 — Business requirements

## Stakeholder questions

### Revenue & orders
- What is the total revenue and order count across the year?
- How does revenue trend month over month?
- What is the average revenue per order and average products sold per order?

### Product performance
- Which products generate the most and least revenue?
- Which products sell the highest quantity?
- Is there a mismatch between units sold and revenue generated (i.e. low-cost high-volume vs high-cost low-volume items)?

### Geography
- How does revenue break down across the 10 cities?
- Which cities are the strongest and weakest markets?

### Time patterns
- What time of day generates the most orders and revenue?
- Which days of the week are busiest?
- Are there seasonal spikes across the 12 months?

---

## KPIs and actual values

| KPI | Measure | Value |
|-----|---------|-------|
| Total revenue | `Total Revenue` | $34,492,035.97 |
| Total orders | `Total Orders` | 178,437 |
| Average revenue per order | `Avg Revenue` | $193.30 |
| Total product sold | `Total Product Sold` | 209,079 |
| Average products per order | `Avg Product Sold Per Order` | 1.17 |

---

## Report audience

| Audience | Primary interest |
|----------|----------------|
| Commercial / revenue team | Revenue by month, product, and city |
| Inventory / merchandising team | Top and bottom selling products |
| Operations team | Hourly and daily order volume patterns |
| Senior leadership | Headline KPIs and city-level performance |

---

## Filtering requirements

The dashboard supports dynamic filtering with titles that update automatically:

| Filter | Field | Driven by |
|--------|-------|-----------|
| Month | `Sales_Data[Month Name]` | `Month List`, `Title` |
| City | `Sales_Data[City]` | `Location List`, `Location Title` |

Dynamic title measures (`Title`, `Location Title`) update chart headers automatically based on active filter selections.
