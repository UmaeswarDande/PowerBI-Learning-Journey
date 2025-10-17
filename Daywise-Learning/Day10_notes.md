# Day 10 — Pareto & Top N Customer Analysis (80/20 Rule)

## Goal
Create an interactive Top-N analysis showing the customers that generate the most sales and profits. Provide a parameter to select Top N dynamically.

## Files included
- `Day10_Pareto_TopN.pbix`
- `measures/TopN_measures.dax`
- `docs/screenshots/` (images)

## Steps performed
1. **Data & Model**
   - Confirmed fact table: `FactSales` and dimension `DimCustomer`.
   - Ensured relationship: `FactSales[CustomerID] -> DimCustomer[CustomerID]` (many:1).

2. **Create Top-N parameter (What-if)**
   - Modeling → New parameter (or create table `TopNParam`).
   - Example: `TopNParam` with field `TopNParam Value`.
   - Add slicer to report using `TopNParam Value`.

3. **Ranking measure**
   ```sql
   Sales_Rank = RANKX(ALL(DimCustomer[CustomerName]), [Total_Sales], , DESC, DENSE)
