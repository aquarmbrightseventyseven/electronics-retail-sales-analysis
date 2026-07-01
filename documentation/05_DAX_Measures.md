# 05 — DAX measures

All 9 measures are documented below, grouped by category.

---

## Revenue & orders

### `Total Revenue`
**Table:** Sales_Data  
**Purpose:** Total revenue across all order line items.

```dax
Total Revenue = SUM(Sales_Data[Amount])
```

**Value (unfiltered):** $34,492,035.97

---

### `Avg Revenue`
**Table:** Sales_Data  
**Purpose:** Average revenue per order.

```dax
Avg Revenue = [Total Revenue] / [Total Orders]
```

**Value (unfiltered):** $193.30

---

### `Total Orders`
**Table:** Sales_Data  
**Purpose:** Count of distinct orders.

```dax
Total Orders = DISTINCTCOUNT(Sales_Data[Order ID])
```

**Value (unfiltered):** 178,437

---

## Product volume

### `Total Product Sold`
**Table:** Sales_Data  
**Purpose:** Total units sold across all line items.

```dax
Total Product Sold = SUM(Sales_Data[Quantity Ordered])
```

**Value (unfiltered):** 209,079

---

### `Avg Product Sold Per Order`
**Table:** Sales_Data  
**Purpose:** Average number of units per order.

```dax
Avg Product Sold Per Order = [Total Product Sold] / [Total Orders]
```

**Value (unfiltered):** 1.17

---

## Dynamic titles (slicer-aware labels)

### `Month List`
**Table:** Sales_Data  
**Purpose:** Returns the selected month name(s) or "Monthly" if no filter is active.

```dax
Month List =
IF(
    ISFILTERED(Sales_Data[Month Name]),
    CONCATENATEX(
        VALUES(Sales_Data[Month Name]),
        Sales_Data[Month Name],
        ", "
    ),
    "Monthly"
)
```

---

### `Title`
**Table:** Sales_Data  
**Purpose:** Dynamic chart title: "[Month] Trend for Total Order" or "Monthly Trend for Total Order".

```dax
Title = [Month List] & " Trend for Total Order"
```

---

### `Location List`
**Table:** Sales_Data  
**Purpose:** Returns the selected city name(s) or "City" if no filter is active.

```dax
Location List =
IF(
    ISFILTERED(Sales_Data[City]),
    CONCATENATEX(
        VALUES(Sales_Data[City]),
        Sales_Data[City],
        ", "
    ),
    "City"
)
```

---

### `Location Title`
**Table:** Sales_Data  
**Purpose:** Dynamic chart title: "Sales by [City]" or "Sales by City".

```dax
Location Title = "Sales by " & [Location List]
```

---

## Measure summary table

| Measure | Table | Category | Format | Value (unfiltered) |
|---------|-------|----------|--------|---------------------|
| Total Revenue | Sales_Data | Revenue | Currency | $34,492,035.97 |
| Avg Revenue | Sales_Data | Revenue | Currency | $193.30 |
| Total Orders | Sales_Data | Orders | Integer | 178,437 |
| Total Product Sold | Sales_Data | Volume | Integer | 209,079 |
| Avg Product Sold Per Order | Sales_Data | Volume | Decimal | 1.17 |
| Month List | Sales_Data | Dynamic title | Text | — |
| Title | Sales_Data | Dynamic title | Text | — |
| Location List | Sales_Data | Dynamic title | Text | — |
| Location Title | Sales_Data | Dynamic title | Text | — |
