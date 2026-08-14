# 💳 Credit Card Fraud Analysis

### SQL + Power BI | Fraud Detection • Risk Analysis • Data Visualization

An end-to-end data analytics project focused on identifying **fraudulent transaction patterns, measuring financial impact, and prioritizing high-value fraudulent transactions** using SQL and Power BI.

---

## 🎯 Project Objective

The goal of this project is to analyze financial transactions and answer three key questions:

> 🔍 **Where is fraud happening?**
> 💰 **What is the financial impact?**
> 🚨 **Which fraudulent transactions should be investigated first?**

---

## 🛠️ Tools Used

| Tool            | Purpose                       |
| --------------- | ----------------------------- |
| 🗄️ **MySQL**   | Data analysis and SQL queries |
| 📊 **Power BI** | Interactive dashboard         |
| 🧮 **DAX**      | KPIs and calculated measures  |
| 🐙 **GitHub**   | Project documentation         |

---

# 📊 Power BI Dashboard

The dashboard follows a simple analytical journey:

### **Overview → Investigation & Risk Analysis**

---

## 📄 Page 1 — Credit Card Fraud Analysis

**Purpose:** Get a complete overview of fraudulent activity and identify major patterns.

### 📌 Key KPIs

| Metric                   |       Value |
| ------------------------ | ----------: |
| Total Transactions       |   **6.36M** |
| Total Transaction Amount |   **1.14T** |
| Fraudulent Transactions  |      **8K** |
| Fraud Rate               |   **0.13%** |
| Fraud Amount             | **12.06bn** |

### 🔎 What the page analyzes

* 📈 **Fraud Per Hour** — fraudulent activity across transaction steps
* 🔄 **Fraud Cases by Transaction Type**
* 💰 **Transaction-Type Amount Analysis**
* 🍩 **Fraud vs Genuine Transactions**

> **Page 1 answers:**
> **“What is happening with fraud overall?”**

### 🖼️ Dashboard Preview

Page 1 - Credit Card Fraud Analysis

---

# 🚨 Page 2 — Fraud Investigation & Risk Analysis

**Purpose:** Move from overall fraud monitoring to **detailed risk investigation**.

### 📌 Key KPIs

| Metric                  |       Value |
| ----------------------- | ----------: |
| Fraudulent Transactions |      **8K** |
| Fraud Amount            | **12.06bn** |
| Average Fraud Amount    |   **1.47M** |
| Highest Fraud Amount    |  **10.00M** |

### 🔎 What the page analyzes

* 💰 **Fraud Amount by Transaction Type**
* 📊 **Fraud Cases by Transaction Type**
* 🚨 **High-Value Fraudulent Transactions**
* 🎛️ **Payment Type filtering**
* 🔢 **Step-level filtering**

The **High-Value Fraudulent Transactions** table focuses on the **Top 20 fraudulent transactions by transaction amount**, helping identify transactions that may require closer investigation.

> **Page 2 answers:**
> **“Which fraudulent transactions require closer investigation?”**

### 🖼️ Dashboard Preview

Page 2 - Fraud Investigation & Risk Analysis
---

# 🔄 Dashboard Flow

```text
                TRANSACTION DATA
                       │
                       ▼
        ┌───────────────────────────┐
        │ PAGE 1 — OVERVIEW         │
        │                           │
        │ Fraud Volume              │
        │ Fraud Rate                │
        │ Fraud Trends              │
        │ Transaction Types         │
        └─────────────┬─────────────┘
                      │
                      ▼
             IDENTIFY PATTERNS
                      │
                      ▼
        ┌───────────────────────────┐
        │ PAGE 2 — INVESTIGATION    │
        │                           │
        │ Fraud Amount              │
        │ Average / Highest Fraud   │
        │ High-Value Transactions   │
        │ Risk Prioritization       │
        └─────────────┬─────────────┘
                      │
                      ▼
              INVESTIGATION
```

### Why two pages?

**Page 1 = Monitor & Understand**

Provides the overall fraud picture and highlights important patterns.

**Page 2 = Investigate & Prioritize**

Drills down into the financial impact and identifies high-value fraudulent transactions.

This creates a clear progression:

**Overview → Pattern Identification → Investigation → Risk Prioritization**

---

# 🔍 SQL Analysis

SQL was used as the analytical foundation of the project.

### Key analysis performed

* Transaction volume analysis
* Transaction amount analysis
* Fraudulent transaction identification
* Fraud rate calculation
* Fraud amount analysis
* Fraud analysis by transaction type
* Fraud trend analysis across transaction steps
* High-value fraudulent transaction identification
* Risk-focused analysis

The SQL analysis was then transformed into **Power BI KPIs and visualizations**.

---

# 💡 Key Business Insights

The analysis helps identify:

### 💰 Financial Impact

The dashboard measures the overall monetary impact of fraudulent transactions.

### 🔄 Fraud Patterns

Transaction types and transaction steps can be analyzed to identify areas with higher fraud activity.

### 🚨 High-Value Risk

The investigation page highlights the highest-value fraudulent transactions so that investigation efforts can be prioritized.

### 📊 Fraud Monitoring

The dashboard provides a quick comparison between fraudulent and genuine transactions.

---

# 🛡️ Business Recommendations

Based on the analysis, organizations can:

* Prioritize investigation of **high-value fraudulent transactions**
* Increase monitoring of transaction types showing higher fraud exposure
* Monitor unusual activity across transaction steps
* Introduce automated alerts for suspicious high-value transactions
* Combine transaction-level analysis with customer/account behavior for stronger fraud detection

---

# 🧠 Skills Demonstrated

**Technical**
`SQL` · `MySQL` · `Power BI` · `DAX` · `Data Visualization`

**Analytical**
`Fraud Analysis` · `Risk Analysis` · `Trend Analysis` · `Transaction Analysis` · `KPI Development`

**Business**
`Risk Prioritization` · `Business Insights` · `Data-Driven Recommendations`

---

# 📁 Project Structure

```text
Credit-Card-Fraud-Analysis/
│
├── Dataset/
│   └── paysim.csv
│
├── SQL/
│   └── Fraud_Analysis.sql
│
├── Power BI/
│   └── Fraud_Analysis_Dashboard.pbix
│
├── Screenshots/
│   ├── Page_1_Credit_Card_Fraud_Analysis.png
│   └── Page_2_Fraud_Investigation_Risk_Analysis.png
│
└── README.md
```

---

# 🚀 Project Workflow

**Raw Data**
↓
**Data Preparation**
↓
**SQL Analysis**
↓
**Fraud Pattern Identification**
↓
**Risk & High-Value Transaction Analysis**
↓
**Power BI Dashboard**
↓
**Business Insights & Recommendations**

---

## ⭐ Conclusion

This project demonstrates an end-to-end approach to **fraud analytics**, combining SQL-based analysis with Power BI visualization.

The dashboard moves from:

> **“What is happening?” → “Why does it matter?” → “What should we investigate?”**

This makes the analysis useful for **fraud monitoring, financial risk analysis, and investigation prioritization**.

