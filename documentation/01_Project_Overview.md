# 01 — Project overview

## Background

This project delivers a Power BI dashboard for an electronics retail business that sells products such as laptops, monitors, phones, and headphones across 10 U.S. cities. The business captures order-level transaction data — including product, quantity, price, order timestamp, and delivery address — and needed a way to understand revenue performance, product mix, and demand patterns across the year.

## Objectives

- Track total revenue, order volume, and product sales over time
- Identify top and bottom performing products by revenue
- Understand revenue distribution across cities
- Reveal hourly and daily demand patterns to inform staffing/inventory decisions
- Track month-over-month and seasonal revenue trends

## Scope

| In scope | Out of scope |
|----------|-------------|
| Order-level transaction data (single year) | Customer-level CRM / loyalty data |
| Revenue, quantity, and pricing analysis | Cost of goods sold / margin analysis |
| City-level and time-of-day breakdowns | Marketing spend / channel attribution |
| Product-level performance | Inventory and supply chain data |

## Deliverables

- An interactive Power BI dashboard
- A data model with a fact table (`Sales_Data`), an `Order` dimension table, and supporting date tables
- 9 DAX measures covering revenue, order volume, and dynamic titles
- This documentation suite

## Key numbers at a glance

| Metric | Value |
|--------|-------|
| Total revenue | $34,492,035.97 |
| Total orders | 178,437 |
| Average revenue per order | $193.30 |
| Total products sold | 209,079 |
| Average products sold per order | 1.17 |
| Cities covered | 10 |
| Distinct products | 19 (10 shown in top-revenue ranking) |

## Tools and technologies

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Data modelling, DAX authoring, dashboard design |
| Power Query (M) | Data ingestion and transformation |
| DAX | Calculated measures |
| GitHub | Version control and documentation |

## File details

| Property | Value |
|----------|-------|
| File name | `Sales_Analysis.pbix` |
| Model size | ~22.6 MB |
| Compatibility level | 1600 |
| Storage mode | Import |
| Connection | localhost (Power BI Desktop) |
| Last processed | 27 April 2026 |
