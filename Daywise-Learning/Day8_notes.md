# Day 8 – Dynamic KPI Dashboard (MTD, QTD, YTD Switcher)

## 📊 Objective
To build an interactive KPI dashboard where users can dynamically toggle between 
Month-to-Date (MTD), Quarter-to-Date (QTD), and Year-to-Date (YTD) metrics 
using a disconnected slicer.

## 🧠 Concepts Used
- Disconnected table (KPI_Selector)
- SELECTEDVALUE() and SWITCH() DAX
- Dynamic measure visualization
- Modern dashboard design (blue & white theme)

## 🧮 Key DAX
```DAX
Selected KPI Sales =
VAR SelectedType = SELECTEDVALUE(KPI_Selector[KPI_Type])
RETURN
SWITCH(
    TRUE(),
    SelectedType = "MTD", [MTD_Sales],
    SelectedType = "QTD", [QTD_Sales],
    SelectedType = "YTD", [YTD_Sales],
    [Total_Sales]
)
