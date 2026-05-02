# 🛒 Customer Insight Engine
### End-to-End E-Commerce Customer Behaviour Analysis
## 📌 Project Overview

This project performs a full data analytics pipeline on a **retail e-commerce dataset** of 5,000 customers and 30 unique products. Starting from a raw CSV file, the data is cleaned using Python, queried with SQL Server, and visualised in an interactive Power BI dashboard — answering 12 real business questions along the way.

> **Business Problem:** How can a retail company understand customer purchasing behaviour to increase revenue, improve retention, and optimise marketing strategies?


---

## 🗂️ Dataset

| Property | Detail |
|---|---|
| Type | Retail / E-commerce |
| Records | 5,000 customers |
| Features | 17 columns |
| Level | Customer Transaction |

**Key columns:** `Customer ID`, `Age`, `Gender`, `Item Purchased`, `Category`, `Purchase Amount`, `Location`, `Season`, `Review Rating`, `Subscription Status`, `Discount Applied`, `Payment Method`, `Frequency of Purchases`

---

## 🔧 Tools & Pipeline

```
Raw CSV  ──►  Python (EDA & Cleaning)  ──►  SQL Server (Analysis)  ──►  Power BI (Dashboard)
```

### 🐍 Step 1 — Python & Pandas
- Loaded dataset into a structured DataFrame
- Fixed category inconsistencies using a mapping dictionary
- Applied domain-aware missing value imputation:
  - Electronics/Accessories → `"Not Applicable"`
  - Clothing → filled with **mode**
  - Review Rating → filled with **product-level mean**
  - Previous Purchases → filled with `0`
- Removed duplicate records identified via `Customer ID`
- Standardised all column names to `lowercase_snake_case`
- Exported clean data to SQL Server via `pyodbc` + `SQLAlchemy`

### 🗄️ Step 2 — SQL Server
Wrote **12 business queries** covering:

| # | Question |
|---|---|
| Q1 | Which category generates the highest revenue? |
| Q2 | Are discounts actually increasing purchase value? |
| Q3 | Total revenue by gender? |
| Q4 | Which discount users spent above the average purchase amount? |
| Q5 | Top 5 products by average review rating? |
| Q6 | Bottom 5 products by average review rating? |
| Q7 | Average purchase: Standard vs Express shipping? |
| Q8 | Do subscribed customers spend more? |
| Q9 | Top 5 products by discount usage %? |
| Q10 | Segment customers into New, Returning, and Loyal? |
| Q11 | Top 3 most purchased products per category? |
| Q12 | Revenue contribution by age group? |

### 📊 Step 3 — Power BI Dashboard
Built a **2-page interactive dashboard** with slicers for Category, Gender, Subscription Status, and Discount Applied.

**Page 1 — Overview**
- Revenue by Gender, Category, Season
- Shipping Type comparison
- Revenue by Age Distribution
- Payment Method breakdown

**Page 2 — Product & Location Deep Dive**
- Top & Bottom 5 Items by Rating and Revenue
- Top & Bottom 5 Locations by Revenue

---

## 📈 Key Findings

| Insight | Finding |
|---|---|
| 🏆 Top Category | Clothing leads at $0.37M (37.2% of revenue) |
| 👥 Top Age Group | 51+ customers drive 40.17% of total revenue |
| 📍 Top City | New York at $187.12K, followed by LA at $159.99K |
| 💳 Top Payment | Debit Card dominates at $253K |
| ⭐ Highest Rated | Jewelry (3.76), Pants (3.72), Blouse (3.68) |
| 💰 Highest Revenue Item | Headphones at $138K |
| 📉 Lowest Revenue Item | Jeans at $7.55K |
| 🌸 Peak Season | Spring, Winter & Summer all at $0.24M — Fall drops to $0.06M |

---

## 📊 Dashboard Preview

> **Page 1 — Customer Overview**

<img width="1340" height="709" alt="Screenshot 2026-05-02 145413" src="https://github.com/user-attachments/assets/09b723ad-a9a6-4efa-8118-173b71c8ce18" />


> **Page 2 — Product & Location Analysis**

<img width="1322" height="711" alt="Screenshot 2026-05-02 145433" src="https://github.com/user-attachments/assets/bc88b80b-c41a-424d-9c24-c0ee15aa70b6" />

---

## 👤 Author

**Your Name**
- LinkedIn: [parbhaat2077](https://linkedin.com/in/yourlinkedin)

