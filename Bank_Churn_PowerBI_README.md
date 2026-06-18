# 🏦 Customer Churn Analysis — Power BI Dashboard
> A multi-table Star Schema analysis identifying churn drivers across 1,000 bank customers

---

## 📌 Project Overview

| | |
|---|---|
| **Industry** | Banking & Financial Services |
| **Tools** | Power BI · DAX · Star Schema Data Modeling |
| **Dashboard Pages** | 4 pages — Executive Overview · Customer Service · Digital Behavior · Recommendations |
| **Data Model** | 5-table Star Schema (1 Fact + 4 Dimensions) |
| **Type** | Portfolio Project (rebuild of original Excel case study) |

---

## 🎯 Business Problem

A bank with 1,000 customers needed to understand the drivers behind a 20.4% churn rate across multiple dimensions — demographics, service interactions, digital channel usage, and spending behavior — to design targeted retention strategies.

---

## 🗂 Data Model — Star Schema

This project was rebuilt from a flat Excel case study into a proper relational model:

```
                Transaction_History (Fact)
                         ↓
        ┌────── Customer_Demographics (Dim) ──────┐
        ↓                  ↓                       ↓
   Churn_Status      Customer_Service        Online_Activity
```

| Table | Role | Rows | Key Fields |
|---|---|---|---|
| `Customer_Demographics` | Dimension (hub) | 1,000 | Age, Gender, Marital_Status, Income_Level |
| `Transaction_History` | **Fact** | 5,054 | Amount_Spent, Product_Category, Transaction_Date |
| `Customer_Service` | Dimension | 1,000 | Interaction_Type, Resolution_Status |
| `Online_Activity` | Dimension | 1,000 | Service_Usage, Login_Frequency |
| `Churn_Status` | Dimension | 1,000 | Churn_Status (0/1) |

All dimension tables relate to `Customer_Demographics` via `Customer_ID`.

---

## 💡 Key Findings

| # | Finding | Data |
|---|---|---|
| 1 | **Overall churn rate** | 204 / 1,000 customers churned **(20.4%)** |
| 2 | **Mobile App has the highest channel churn** | **23.1%** vs Online Banking 20.1% vs Website 17.8% |
| 3 | **Married customers churn the most** | **23.0%** vs Single 20.5% vs Widowed 19.6% vs Divorced 18.5% |
| 4 | **Low-income segment is highest risk** | **22.2%** vs Medium 19.9% vs High 19.2% |
| 5 | **Feedback complaints go unresolved most** | Feedback interactions show the highest unresolved volume |
| 6 | **Engaged users churn less** | Avg login frequency — Stayed: **26.5** vs Churned: **23.6** |
| 7 | **Spending is similar across both groups** | Stayed: **$250.8** avg vs Churned: **$247.5** avg — churn isn't purely value-driven |
| 8 | **Groceries is the top category by spend** | Avg transaction: **$256.01**, ahead of Clothing and Books |

---

## 📈 Dashboard Pages

### Page 1 — Executive Overview
KPI cards (Total Customers, Churned Customers, Churn Rate, Avg Spend Churned) + Donut chart (Churned vs Active) + Churn Rate by Marital Status + Churn Rate by Income Level + Churn Rate by Gender
Slicers: Gender · Churn_Status · Income_Level

### Page 2 — Customer Service Analysis
Detail table (Interaction Type × Resolution Status × Churn Rate) + Churn Rate by Interaction Type + Churn Rate by Resolution Status (Resolved vs Unresolved)
Slicers: Gender · Resolution_Status · Interaction_Type

### Page 3 — Digital Behavior
KPI cards per channel (Mobile, Online Banking, Website churn rates) + Avg Login Frequency by Churned Status + Churn Rate by Service Usage + Average Spend by Product Category

### Page 4 — Recommendations
Avg Spend comparison (Stayed vs Churned) + Total Revenue Lost + 3 targeted retention recommendations

---

## ✅ Retention Recommendations

### 1. 📱 Fix the Mobile App Experience
Mobile App users churn at **23.1%** — the highest across all digital channels. A UX audit is recommended to identify and resolve friction points in the mobile journey.

### 2. 💍 Target Married Customers with Loyalty Offers
The married segment shows **23.0%** churn — the highest by marital status. A loyalty programme tailored to this group's financial needs (e.g., joint accounts, family banking perks) could improve retention.

### 3. 💬 Resolve Feedback Complaints Faster
The "Feedback" interaction type carries the highest unresolved case volume of all interaction types. A dedicated resolution team with clear SLAs is recommended.

---

## 📁 Repository Structure

```
├── README.md                          ← You are here
├── Bank_Churn_Dashboard.pbix           ← Power BI dashboard file
└── data/
    └── Dataset.xlsx                    ← 5-sheet source (Star Schema source tables)
```

---

## 🛠 Tools Used

- **Power BI** — Data modeling (Star Schema), DAX measures, 4-page interactive dashboard
- **DAX** — Custom measures for churn rate, segment-level filtering, and revenue impact

---

## 👤 About

This project is a rebuild of an earlier flat-file churn analysis, redesigned around a proper **Star Schema** data model with a Transaction fact table and four supporting dimension tables — reflecting how churn analysis is structured in production BI environments.

📧 [Your Email] | 💼 [Your LinkedIn URL] | 🐙 [Your GitHub URL]
