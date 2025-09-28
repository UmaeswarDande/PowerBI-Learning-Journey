# Day 3 – Power Query: Group By, Merge, Append 🔄

## ✅ Key Learnings
Today I moved beyond data cleaning (Day 2) into **data modeling and analysis** using Power Query:
- **Group By**: Aggregated Sales, Profit, and OrderCount by Region → created `Region_Summary`.
- **Merge**: Joined `Region_Summary` with `RegionTargets.csv` to bring in target values.
- **Custom Column**: Calculated **Achievement %** = (TotalSales / Target) * 100.
- **Append**: Combined Q1 (`Day2_SalesData`) and Q2 (`Day2_Sales_Q2`) into a single dataset `All_Sales`.
- Ensured correct data types, removed duplicates, and verified combined dataset.

---

## 📊 Visuals
### 1. Region Performance Bar Chart
- Shows TotalSales by Region.
- Tooltip includes Target and Achievement %.

![Region Performance](../images/Day3_RegionPerformance.png)

### 2. Sales Trend Line Chart (Q1 + Q2)
- Displays sales over time across Q1 and Q2.
- Region-wise breakdown for comparison.

![Sales Trend](../images/Day3_AllSalesTrend.png)

### 3. Region Performance Summary Table
- Tabular view of TotalSales, Profit, Target, and Achievement %.
- Highlights which regions are underperforming or exceeding targets.

![Region Summary](../images/Day3_RegionSummary.png)

---

## 📂 Files in Repo
- **datasets/**  
  - Day2_SalesData.csv  
  - Day2_Sales_Q2.csv  
  - RegionTargets.csv  

- **Daywise-Learning/**  
  - Day3_PowerQuery.pbix  
  - Day3_PowerQuery.md  

- **images/**  
  - Day3_RegionPerformance.png  
  - Day3_AllSalesTrend.png  
  - Day3_RegionSummary.png  

---

## 🔮 Next Steps (Day 4)
- Practice **Pivot & Unpivot** transformations.  
- Add **Conditional Columns** & **Index Columns**.  
- Explore **Reference vs Duplicate queries** (staging patterns).  
- Begin with **basic DAX**: Measures vs Calculated Columns.
