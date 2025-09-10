# Day 2 – Power Query Basics 🔄

## ✅ What I Did
- Loaded dataset: `datasets/Day2_SalesData.csv`
- Trimmed extra spaces from Customer and Region
- Changed data types:
  - OrderDate → Date (using locale for consistency)
  - Sales & Profit → Decimal Number
- Removed rows with null values (Customer or Profit)
- Removed duplicate rows
- Verified clean table with correct data

## 📊 Output (Clean Table Sample)
| OrderID | OrderDate   | Customer           | Region | Sales | Profit |
|---------|-------------|-------------------|--------|-------|--------|
| 101     | 2025-01-01  | John Smith        | North  | 100   | 30     |
| 102     | 2025-01-02  | Jane Doe          | South  | 150   | 40     |
| 104     | 2025-01-03  | John Smith        | North  | 200   | 50     |
| 107     | 2025-01-05  | Anna-Marie O'Neil | South  | 250   | 60     |
| 108     | 2025-06-01  | Bob Brown         | East   | 180   | 20     |

## 📂 Files in Repo
- datasets/Day2_SalesData.csv
- Daywise-Learning/Day2_PowerQuery.pbix
- Daywise-Learning/Day2_PowerQuery.md
