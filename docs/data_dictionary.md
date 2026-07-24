# Data Dictionary - Global Retail Sales Data Model

## Table: `FactSales`
Stores transactional e-commerce and retail sales order line items.

| Column Name | Data Type | Key Type | Description |
|---|---|---|---|
| `SalesOrderNumber` | Text | Primary Key | Unique order identifier |
| `OrderDate` | Date | Foreign Key | Date of order placement (links to `DimDate`) |
| `CustomerKey` | Integer | Foreign Key | Links to `DimCustomer` |
| `ProductKey` | Integer | Foreign Key | Links to `DimProduct` |
| `TerritoryKey` | Integer | Foreign Key | Links to `DimTerritory` |
| `SalesAmount` | Currency | Measure | Total net revenue for line item |
| `OrderQuantity` | Integer | Measure | Quantity of items purchased |

## Table: `FactBudget`
Stores monthly budgeted revenue targets by region and category.

| Column Name | Data Type | Key Type | Description |
|---|---|---|---|
| `BudgetDate` | Date | Foreign Key | First day of target month (links to `DimDate`) |
| `TerritoryKey` | Integer | Foreign Key | Links to `DimTerritory` |
| `ProductCategoryKey` | Integer | Foreign Key | Links to `DimProductCategory` |
| `BudgetAmount` | Currency | Measure | Target revenue allocation |
