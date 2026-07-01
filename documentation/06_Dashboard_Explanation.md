# 06 — Dashboard explanation

The dashboard is titled **"2019/2020 Sales Report"** and consists of two pages, navigated via the panel on the left side of each page.

---

## Header (both pages)

A purple header bar appears on both pages and contains:

- **Title:** 2019/2020 Sales Report
- **Order Area dropdown** — filters by city (default: All)
- **Order Month dropdown** — filters by month (default: All)

---

## KPI strip (both pages)

Five headline cards sit below the header on both pages:

| Card | Measure | Value |
|------|---------|-------|
| Total Orders | `Total Orders` | 178,437 |
| Total Product Sold | `Total Product Sold` | 209,079 |
| Avg Product Sold Per Order | `Avg Product Sold Per Order` | 1.17 |
| Total Revenue | `Total Revenue` | 34.49M |
| Avg Revenue | `Avg Revenue` | 193.30 |


---

## Page 1 — Home

This page covers overall sales performance across time and geography.

### Navigator panel (left)
Two navigation buttons — **Home** (current page) and **Best/Worst Sellers** — plus two narrative callout boxes:

**Busiest Days & Time**
- Orders are highest on **weekdays and afternoons**
- Maximum monthly orders occur in **April, October, and December**

**Sales Performance**
- **Location:** San Francisco (CA) contributes the maximum sales
- **Product:** AAA Batteries (4-pack) contributes the maximum sales (by quantity)

### Sales by Hour (column chart)
Order volume across the 24-hour clock. Demand builds steadily from early morning, peaks around **10 AM–1 PM** and again near **6–7 PM**, with troughs overnight (0–6 AM).

### Monthly Trend for Total Order (line chart)
Dynamic title driven by the `Title` measure. Shows order count by month, January through December:

| Month | Orders |
|-------|--------|
| January | 9.7K |
| February | 12.0K |
| March | 15.2K |
| April | 18.3K (local peak) |
| May | 16.6K |
| June | 13.6K |
| July | 14.3K |
| August | 12.0K |
| September | 11.6K |
| October | 20.3K |
| November | 17.6K |
| December | 25.0K (peak) |

Confirms the narrative callout: April, October, and December are the strongest months, with December the clear annual peak.

### Revenue by Quarter (bar chart)
| Quarter | Revenue |
|---------|---------|
| Q4 | 11.55M |
| Q2 | 9.12M |
| Q3 | 6.99M |
| Q1 | 6.83M |

Q4 is the strongest quarter by a wide margin, consistent with the October–December order surge.

### Percentage of Sales by Quarter (donut chart)
| Quarter | Share |
|---------|-------|
| Q4 | 33.49% |
| Q2 | 26.44% |
| Q3 | 20.26% |
| Q1 | 19.81% |

### Sales by City (bar chart)
Dynamic title driven by `Location Title`. Revenue by city, ranked highest to lowest:

| City | Revenue |
|------|---------|
| San Francisco (CA) | 8.26M |
| Los Angeles (CA) | 5.45M |
| New York City (NY) | 4.66M |
| Boston (MA) | 3.66M |
| Atlanta (GA) | 2.80M |
| Dallas (TX) | 2.77M |
| Seattle (WA) | 2.75M |
| Portland (OR) | 1.87M |
| Austin (TX) | 1.82M |
| Portland (ME) | 0.45M |

### Daily Trend for Total Order (column chart)
Order count by day of week:

| Day | Orders |
|-----|--------|
| Sunday | 26,551 |
| Monday | 26,547 |
| Tuesday | 27,175 (peak) |
| Wednesday | 26,477 |
| Thursday | 26,461 |
| Friday | 26,247 |
| Saturday | 26,492 |

Day-of-week order volume is remarkably flat — Tuesday is the highest but the spread across all seven days is under 4%.

---

## Page 2 — Best / Worst Sellers

This page ranks products by revenue, order count, and quantity sold.

### Navigator panel (left)
- **Home** — navigates to Page 1
- **Best/Worst Sellers** — current page (highlighted)

Two narrative callout boxes:

**Best Sellers**
- **Revenue:** Macbook Pro Laptop contributes the maximum revenue
- **Quantity:** AAA Batteries (4-pack) contributes the maximum sales (units)
- **Total Orders:** USB-C Charging Cable contributes the maximum order count

**Worst Sellers**
- **Revenue:** 27in FHD Monitor contributes the minimum revenue
- **Quantity:** LG Dryer contributes the minimum quantity sold
- **Total Orders:** LG Dryer contributes the minimum order count

### Top 10 Product by Revenue (bar chart)
| Rank | Product | Revenue |
|------|---------|---------|
| 1 | Macbook Pro Laptop | 8.0M |
| 2 | iPhone | 4.8M |
| 3 | ThinkPad Laptop | 4.1M |
| 4 | Google Phone | 3.3M |
| 5 | 27in 4K Gaming Monitor | 2.4M |
| 6 | 34in Ultrawide Monitor | 2.4M |
| 7 | Apple Airpods Headphones | 2.3M |
| 8 | Flatscreen TV | 1.4M |
| 9 | Bose SoundSport Headphones | 1.3M |
| 10 | 27in FHD Monitor | 1.1M |

### Top 10 Product by Order (bar chart)
| Rank | Product | Orders |
|------|---------|--------|
| 1 | USB-C Charging Cable | 21.9K |
| 2 | Lightning Charging Cable | 21.7K |
| 3 | AAA Batteries (4-pack) | 20.6K |
| 4 | AA Batteries (4-pack) | 20.6K |
| 5 | Wired Headphones | 18.9K |
| 6 | Apple Airpods Headphones | 15.5K |
| 7 | Bose SoundSport Headphones | 13.3K |
| 8 | 27in FHD Monitor | 7.5K |
| 9 | iPhone | 6.8K |
| 10 | 27in 4K Gaming Monitor | 6.2K |

### Bottom 10 Product by Revenue (bar chart)
| Rank | Product | Revenue |
|------|---------|---------|
| 1 (lowest) | 27in FHD Monitor | 1.13M |
| 2 | Vareebadd Phone | 0.83M |
| 3 | 20in Monitor | 0.45M |
| 4 | LG Washing Machine | 0.40M |
| 5 | LG Dryer | 0.39M |
| 6 | Lightning Charging Cable | 0.35M |
| 7 | USB-C Charging Cable | 0.29M |
| 8 | Wired Headphones | 0.25M |
| 9 | AA Batteries (4-pack) | 0.11M |
| 10 | AAA Batteries (4-pack) | 0.09M |

> Note: several products (27in FHD Monitor, Lightning/USB-C Charging Cable, Wired Headphones, AA/AAA Batteries) appear in **both** the top and bottom 10 lists across different ranking dimensions — high order count and high quantity sold, but low revenue per unit. This is expected for low-cost, high-volume accessory items.

### Bottom 10 Product by Order (bar chart)
| Rank | Product | Orders |
|------|---------|--------|
| 1 (lowest) | 27in 4K Gaming Monitor | 6.2K |
| 2 | 34in Ultrawide Monitor | 6.2K |
| 3 | Google Phone | 5.5K |
| 4 | Flatscreen TV | 4.8K |
| 5 | Macbook Pro Laptop | 4.7K |
| 6 | ThinkPad Laptop | 4.1K |
| 7 | 20in Monitor | 4.1K |
| 8 | Vareebadd Phone | 2.1K |
| 9 | LG Washing Machine | 0.7K |
| 10 | LG Dryer | 0.6K |

### Top 10 Product by Quantity (bar chart)
| Rank | Product | Quantity |
|------|---------|----------|
| 1 | AAA Batteries (4-pack) | 31.02K |
| 2 | AA Batteries (4-pack) | 27.64K |
| 3 | USB-C Charging Cable | 23.98K |
| 4 | Lightning Charging Cable | 23.22K |
| 5 | Wired Headphones | 20.56K |
| 6 | Apple Airpods Headphones | 15.66K |
| 7 | Bose SoundSport Headphones | 13.46K |
| 8 | 27in FHD Monitor | 7.55K |
| 9 | iPhone | 6.85K |
| 10 | 27in 4K Gaming Monitor | 6.24K |

### Bottom 10 Product by Quantity (bar chart)
| Rank | Product | Quantity |
|------|---------|----------|
| 1 (lowest) | 27in 4K Gaming Monitor | 6.24K |
| 2 | 34in Ultrawide Monitor | 6.20K |
| 3 | Google Phone | 5.53K |
| 4 | Flatscreen TV | 4.82K |
| 5 | Macbook Pro Laptop | 4.73K |
| 6 | ThinkPad Laptop | 4.13K |
| 7 | 20in Monitor | 4.13K |
| 8 | Vareebadd Phone | 2.07K |
| 9 | LG Washing Machine | 0.67K |
| 10 | LG Dryer | 0.65K |

---

## Filters

| Filter | Field | Location |
|--------|-------|----------|
| Order Area | `Sales_Data[City]` | Header dropdown — both pages |
| Order Month | `Sales_Data[Month Name]` | Header dropdown — both pages |

Dynamic title measures (`Title`, `Location Title`) automatically update chart titles when filters are applied.

