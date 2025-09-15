# 🛒 Mahadev E-commerce Sales Dashboard (Power BI)

![Dashboard Preview](ECOMMERCE%20SALES%20DASHBOARD.png)

---

## 📌 Project Overview
This repository contains an **E-commerce Sales Dashboard** built in **Power BI** to analyze and monitor online sales performance. It provides insights into revenue, profit, quantity sold, average order value (AOV), product categories, payment modes, and regional sales performance.

The dashboard enables business teams to identify high-performing areas, track seasonal trends, and make data-driven decisions to improve sales.

---

## 🎯 Objectives
- Track **sales metrics** including Amount, Profit, Quantity, and AOV.
- Understand sales performance by **state, category, sub-category, and payment modes**.
- Monitor **monthly profit trends** and **quarterly performance**.
- Provide interactive filtering by **State** and **Quarter**.

---

## 🧮 Key Metrics in the Dashboard

| Metric            | Description |
|-------------------|-------------|
| **Sum of Amount** | Total revenue generated (438K) |
| **Sum of Profit** | Total profit generated (37K) |
| **Sum of Quantity** | Total quantity sold (5615) |
| **Sum of AOV**    | Average order value (121.01K) |

---

## 📈 Visuals Included

### 1. Top-State (Bar Chart)
- Shows total sales (amount) by top states.
- Maharashtra, Madhya Pradesh, Uttar Pradesh, Delhi, Gujarat.

### 2. Quantity by Category (Donut Chart)
- Categories: Clothing 63%, Electronics 21%, Furniture 17%.
- Identifies which product categories dominate sales volume.

### 3. Profit by Month (Column Chart)
- Tracks profit across months January to December.
- Highlights seasonal peaks and negative months (losses).

### 4. Top-State by Quantity (Bar Chart)
- Shows total quantity sold by state.
- Hariv…, Madh…, Mada…, Shiv…, Vish…

### 5. Quantity by Payment Modes (Donut Chart)
- Payment modes: COD 46%, UPI 22%, Debit 13%, Credit Card 11%, EMI 8%.
- Identifies customer preferences for payment methods.

### 6. Sum of Profit by Sub-Category (Horizontal Bar Chart)
- Sub-categories: Printers, Bookcases, Saree, Accessories, Tables.
- Shows profit contribution across sub-categories.

---

## 🎚️ Filters and Slicers
- **Quarter Selector**: Q1, Q2, Q3, Q4, or All.
- **State Selector**: Filter data by state.

---

## 🗂️ Data Sources
The `.pbit` file allows you to connect to your own E-commerce dataset. Typically, you need a dataset with the following fields:

| Column Name    | Description |
|----------------|-------------|
| OrderID        | Unique order ID |
| State          | Customer state |
| Category       | Product category |
| Sub-Category   | Product sub-category |
| Payment Mode   | Payment method (COD, UPI, etc.) |
| Order Date     | Date of order |
| Amount         | Total sales amount |
| Profit         | Profit from order |
| Quantity       | Quantity sold |

---

## ⚙️ How to Use This Dashboard

### Step 1: Download and Open
- Download the file **`ECOMMERCE SALES DASHBOARD.pbit`**.
- Open it with **Power BI Desktop**.

### Step 2: Connect to Your Data Source
- When prompted, provide the location of your e-commerce dataset (Excel, CSV, or database).
- Map the fields accordingly.

### Step 3: Refresh Data
- Click **Refresh** in Power BI to load the data into the dashboard visuals.

### Step 4: Interact with Filters
- Use slicers to filter by State, Quarter, Category, or Payment Modes.

---

## 🛠️ Technical Details
- **Software**: Power BI Desktop (latest version recommended).
- **File Type**: `.pbit` (Power BI template file).
- **Data Model**: Contains prebuilt measures and visuals (DAX measures for Sum of Amount, Profit, AOV, etc.).
- **Custom Visuals**: Standard Power BI visuals (bar chart, donut chart, card visuals, and column chart).

---

## 🧑‍💻 Example DAX Measures

```DAX
-- Total Amount
Total Amount = SUM(SalesData[Amount])

-- Total Profit
Total Profit = SUM(SalesData[Profit])

-- Total Quantity
Total Quantity = SUM(SalesData[Quantity])

-- Average Order Value (AOV)
Average Order Value = DIVIDE([Total Amount], [Total Quantity], 0)
