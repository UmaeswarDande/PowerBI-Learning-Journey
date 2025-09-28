# Day 4 – Pivot/Unpivot, Conditional, Index, Staging Pattern & Intro DAX

## ✅ Key Learnings
- **Unpivoted Data**: Converted monthly sales columns (Jan–Apr) into normalized rows (`Month`, `Sales`).
- **Conditional Column**: Created `Performance` band:
  - Sales >= 150 → High
  - Sales >= 120 → Medium
  - Else → Low
- **Index Column**: Added row index for ordering and unique IDs.
- **Staging Pattern**:
  - `Stg_Day4_Sales` → clean master query, load disabled.
  - `Day4_Sales_Unpivoted` → reference from staging (used in visuals).
  - `Day4_Sales_Duplicate` → independent copy for testing.
- **DAX Measures** (created in Modeling tab):
  ```DAX
  Total Sales = SUM('Day4_Sales_Unpivoted'[Sales])

  High Sales Count =
  CALCULATE(
      COUNTROWS('Day4_Sales_Unpivoted'),
      'Day4_Sales_Unpivoted'[Performance] = "High"
  )

  Average Sales = AVERAGE('Day4_Sales_Unpivoted'[Sales])


📸 Visuals

Matrix (Region × Month)


Clustered Column (Month × Product)


Bar Chart (Performance vs Total Sales)


📂 Files

datasets/Day4_SalesPivot.csv

Daywise-Learning/Day4_PowerQuery.pbix

Daywise-Learning/Day4_PowerQuery.md

images/Day4_Matrix.png

images/Day4_MonthByProduct.png

images/Day4_PerformanceBar.png