# Power Query ETL Transformation Summary

1. **Unpivoting Budget Data:**
   - Raw budget source delivered target amounts in wide monthly columns (`Jan_2023`, `Feb_2023`).
   - Applied **Unpivot Other Columns** in Power Query to transform data into an unpivoted, normalized `BudgetDate` attribute.

2. **Data Cleansing & Type Standardization:**
   - Replaced nulls in customer demographics with `"Unknown"`.
   - Explicitly cast revenue and budget numbers to `Fixed Decimal Number` (Currency) for exact calculations.

3. **Date Table Creation:**
   - Generated a continuous `DimDate` dimension covering all order and budget target periods.
   - Set up month-start relationships to cleanly join `FactSales` (daily grain) and `FactBudget` (monthly grain).
