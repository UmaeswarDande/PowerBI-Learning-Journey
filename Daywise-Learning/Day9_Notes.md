# 📊 Day 9 – Customer Performance Analysis (Top/Bottom & Retention Insights)

## 🎯 Goal  
Analyze customer performance with slicing by **Year, Quarter, Region**, and **Customer**.  
Show key KPIs, regional trends, and a detailed matrix showing sales contribution by customer and region.

---

## 🧱 Data Model (Star Schema)

**Fact Table:**  
- `FactSales`: OrderID, OrderDate, CustomerID, ProductID, RegionID, Sales, Profit, ProfitMargin  

**Dimension Tables:**  
- `DimDate`: Date, Year, Quarter, Month, etc. *(Marked as date table)*  
- `DimCustomer`: CustomerID, CustomerName, RegionID  
- `DimProduct`: ProductID, ProductName, Category  
- `DimRegion`: RegionID, RegionName  

### 🔗 Relationships
| From Table | From Column | To Table | To Column | Type |
|-------------|-------------|-----------|------------|------|
| FactSales | CustomerID | DimCustomer | CustomerID | Many-to-One |
| FactSales | ProductID | DimProduct | ProductID | Many-to-One |
| FactSales | RegionID | DimRegion | RegionID | Many-to-One |
| FactSales | OrderDate | DimDate | Date | Many-to-One |

✅ *DimDate[Date]* is **marked as the date table**.

---

## 🧮 DAX Measures

### Core Measures
```DAX
Total Sales =
SUM ( FactSales[Sales] )

Order Count =
DISTINCTCOUNT ( FactSales[OrderID] )

Avg Order Value =
DIVIDE ( [Total Sales], [Order Count], 0 )

Sales YTD =
CALCULATE ( [Total Sales], DATESYTD ( DimDate[Date] ) )
