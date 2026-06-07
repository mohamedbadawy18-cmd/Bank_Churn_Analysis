# 🏦 Customer Churn Analysis — UK Bank
> Identifying the root causes behind a 20.4% churn rate across 1,000 customers

---

## 📌 Project Overview

| | |
|---|---|
| **Industry** | Banking & Financial Services |
| **Region** | United Kingdom |
| **Type** | Virtual Training Project |
| **Tools** | Excel / Power BI |
| **Deliverable** | EDA Report + Visualizations + Recommendations |

---

## 🎯 Business Problem

A UK-based bank was experiencing a **20.4% customer churn rate** — significantly above acceptable benchmarks. The bank needed to understand:

1. Which customer segments are most at risk of leaving?
2. What is the role of customer service quality in driving churn?
3. Does the digital channel (Mobile vs. Web) affect customer loyalty?

---

## 📊 Dataset

- **Size:** 1,000 customers
- **Key features analyzed:**
  - Customer Demographics (Income Level)
  - Customer Service Interactions (Type + Resolution Status)
  - Online Activity / Service Usage (Mobile App, Online Banking, Website)

---

## 🔍 Methodology

### Phase 1 — EDA & Preprocessing

**Data Cleaning:**
- Imputed missing values in income and service log fields
- Applied One-Hot Encoding to categorical variables (`Income_Level`, `Service_Usage`)
- Detected and handled outliers in transaction and interaction counts
- Normalized numerical features for model readiness

**Exploratory Analysis:**
- Segmented churn by income level, complaint type, and resolution status
- Calculated churn rates per segment to identify highest-risk groups
- Mapped service channel usage against churn behavior

---

## 💡 Key Findings

| # | Finding | Data |
|---|---|---|
| 1 | **Overall churn rate** | 204 out of 1,000 customers churned **(20.4%)** |
| 2 | **Unresolved complaints = churn** | Customers with unsolved issues churn at **47%** — nearly double the average |
| 3 | **Resolution rate is insufficient** | Only **52.2%** of complaints are resolved |
| 4 | **Worst complaint category** | **"Feedback"** has the highest number of unresolved cases |
| 5 | **Most at-risk income group** | **Low-income** customers represent the highest churn volume |
| 6 | **48% of complaints go unresolved** | Unresolved issues are the primary driver of departure |

---

## 📈 Visualizations

**Chart 1 — Complaints by Type & Resolution Status** *(Clustered Bar)*
- Shows that Feedback > Complaint > Inquiry in terms of unresolved volume
- Feedback category is the critical failure point

**Chart 2 — Churn by Income Level** *(Bar Chart)*
- Low-income customers churn the most, followed by High, then Medium

**Chart 3 — Churn by Service Channel** *(Donut Chart)*
- Online Banking: **38.73%** of churned customers
- Website: **34.31%**
- Mobile App: **26.96%**

---

## ✅ Recommendations

Based on the analysis, three actions were recommended to the bank:

### 1. 🔧 Fix the Feedback Resolution Pipeline
The "Feedback" category has the highest unresolved rate. The bank should assign dedicated agents to feedback cases and set a maximum resolution SLA (e.g., 48 hours).

### 2. 💰 Prioritize Low-Income Customer Retention
Design targeted retention offers for low-income segments — simpler products, lower fees, and proactive outreach when complaint activity increases.

### 3. 📱 Investigate Online Banking Experience
With 38.73% of churned customers using Online Banking, there may be UX friction or service gaps in the web platform that are going unaddressed.

---

## 📁 Repository Structure

```
├── README.md                        ← Project overview (you are here)
├── The_Final_Report.pdf             ← Full EDA report with all visualizations
```

---

## 🛠 Tools Used

- **Microsoft Excel** — Data cleaning, segmentation, pivot analysis
- **Power BI** — Interactive dashboards and visual storytelling

---

## 👤 About

This project was completed as part of a structured virtual training program with a UK-based bank.
The analysis was delivered as a formal Phase 1 report covering EDA, preprocessing, and business recommendations.

📧 [mohamedbadawisayed@gmail.com] | 💼 [www.linkedin.com/in/mohamed-badawi28]
