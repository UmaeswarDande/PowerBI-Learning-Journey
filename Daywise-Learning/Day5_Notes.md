# Day 5 – Dimensional Modeling and Sales Analysis

## Key Learnings
- Created **Star Schema** with Fact and Dimension tables:
  - FactSales (Sales, Profit, OrderDate, RegionID, ProductID)
  - DimDate (Date, Year, Month, Quarter)
  - DimRegion (RegionID, RegionName)
  - DimProduct (ProductID, ProductName)
- Built relationships:
  - FactSales[OrderDate] → DimDate[Date]
  - FactSales[RegionID] → DimRegion[RegionID]
  - FactSales[ProductID] → DimProduct[ProductID]
- Used **DimDate** for time-based analysis (Year, Quarter, Month).
- Developed multiple visualizations to analyze sales trends and performance.

---

## Visualizations

### 1. Sales Trend by Year & Quarter
Line chart showing sales movement across **dates**, categorized by **year and quarter**.  
📌 File: `Day5_SalesTrend.png`  

### 2. Quarterly Sales Performance
Column chart comparing **total sales by quarter**.  
📌 File: `Day5_QuarterlySales.png`  

### 3. Total Sales by Region
Bar chart showing **regional contribution** to overall sales.  
📌 File: `Day5_SalesByRegion.png`  

### 4. Total Sales by Product
Bar chart analyzing **sales distribution by product type**.  
📌 File: `Day5_SalesByProduct.png`  

---

## Insights
- **Q1 2025** contributed the total sales (≈ 5350).  
- **North region** performed best compared to East and South.  
- **Table** and **Laptop** are the top-performing products.  

---

📂 Files uploaded:
- Day5_Notes.md  
- Day5_SalesTrend.png  
- Day5_QuarterlySales.png  
- Day5_SalesByRegion.png  
- Day5_SalesByProduct.png  
- Day5_Schema.pbix  