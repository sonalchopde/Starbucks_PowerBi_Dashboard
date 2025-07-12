# Starbucks_PowerBi_Dashboard
# ☕ Starbucks Sales Analysis Dashboard | Power BI Project

## 📊 Project Overview

This project showcases a **Sales Analysis Dashboard** built using **Power BI** and **DAX**, based on real-world-style data from Starbucks. It aims to provide valuable business insights like total sales, quantity sold, revenue by category (e.g., Coffee), and average order value.

---

## 🧰 Tools & Technologies

- Power BI  
- DAX (Data Analysis Expressions)  
- Power Query  
- Data Modeling (Star Schema)  

---

## 📁 Datasets Used

1. **Orders** – Contains order ID, product ID, quantity, price, etc.  
2. **Products** – Contains product details like name, category, etc.

---

## 🔧 Key Features

- **Data Cleaning & Transformation** using Power Query Editor  
- **Star Schema Modeling**: Linked fact and dimension tables  
- **Dynamic Measures** created using DAX  
- **Interactive Dashboard** with filters, slicers, KPIs, and visuals

---

## 📐 DAX Measures Created

```dax
Total Quantity = SUM(Orders[Quantity])

Total Revenue = SUMX(Orders, Orders[Quantity] * Orders[Price])

Product Categories = DISTINCTCOUNT(Products[Category])

Average Order Value = DIVIDE([Total Revenue], DISTINCTCOUNT(Orders[Order ID]))

Coffee Revenue = CALCULATE([Total Revenue], Products[Category] = "Coffee")
