# Global Retail Sales & Budget Intelligence Dashboard

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)](#)

[View Live Portfolio Write-Up & Dashboard](https://benlusic.wixsite.com/bensportfolio/post/global-retail-sales-budget-intelligence-dashboard)

---

## 1. What business question did you answer?
Retail organizations struggle to track daily sales velocity against static monthly budget targets across diverse global product lines and sales territories. This project answers:
* Which sales territories and product categories are exceeding or lagging behind their monthly revenue budgets?
* What is the variance ($ and %) between actual revenue and budgeted targets across different retail regions?
* How are key metrics like Average Order Value (AOV) and Order Quantity driving overall sales performance?

---

## 2. Where did the data come from?
The dataset combines transactional retail sales order records and historical corporate budget allocations based on the standard **AdventureWorks** retail database structure.

---

## 3. Is the data real, public, synthetic, or modified?
**Public & Modified.** Public benchmark benchmark dataset modified and transformed to simulate real-world e-commerce and retail enterprise sales modeling.

---

## 4. How many records and what time period?
* **Sales Transactions:** ~60,000+ line-item transaction records.
* **Budget Targets:** Monthly target grain mapped across territories and product categories over a 3-year historical period.

---

## 5. What tools did you use?
* **Power BI Desktop:** Multi-fact star-schema modeling, interactive report design, and publication.
* **Power Query (M):** Unpivoting monthly budget spreadsheets, cleansing missing values, and establishing date grains.
* **DAX:** Dynamic measure building for budget variance ($/%), YTD performance, and Year-over-Year calculations.

---

## 6. What transformations did you perform?
1. **Unpivoting Budget Matrices:** Transformed cross-tab budget spreadsheets into a normalized tabular format using Power Query.
2. **Grain Alignment:** Standardized transaction dates to daily grain while modeling budget targets at the monthly start date grain (`YYYY-MM-01`).
3. **Data Quality Checks:** Filtered out test transaction keys, handled missing customer values, and enforced strict currency formats.

---

## 7. How did you validate the results?
* **Sum Reconciliation:** Validated that total sum of `FactSales[SalesAmount]` matched source ledger totals exactly.
* **Grain Integrity Check:** Confirmed that monthly aggregated sales calculations lined up accurately against the monthly budget grain without Cartesian duplicating.

---

## 8. What did you find?
* **Regional Outliers:** North American territories consistently met or exceeded sales targets by +8.5%, while European sectors lagged behind target budgets by -12.3%.
* **Product Mix Drivers:** High-end product lines generated lower order volume but drove higher gross margins, keeping revenue close to budget despite lower unit sales.

---

## 9. What decisions could follow?
* **Inventory Allocation:** Reallocate product inventory from lagging territories to high-demand regions to optimize stock availability.
* **Target Calibration:** Adjust next fiscal year's monthly budget targets in territories experiencing macroeconomic contractions.

---

## 10. What are the limitations?
* Budget data is provided at a monthly grain rather than daily, requiring explicit relationship handling in DAX for daily comparison visuals.

---

## 11. How can someone reproduce the work?
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/retail-sales-budget-powerbi.git](https://github.com/your-username/retail-sales-budget-powerbi.git)
