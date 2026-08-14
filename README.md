# **💳 CREDIT CARD FRAUD ANALYSIS — MYSQL + POWER BI**

> **End-to-end data analytics project for identifying fraudulent transaction patterns, measuring financial impact, and prioritizing high-value transactions for investigation.**

---

## **🎯 PROJECT AT A GLANCE**

This project analyzes the **PaySim financial transaction dataset** using **MySQL, SQL analytics, Power BI, and DAX**.

The analysis moves from raw transaction data to business-focused fraud insights:

**Raw Data → SQL Analysis → Fraud Patterns → Risk Analysis → Power BI Dashboard → Business Recommendations**

### **The project answers three key questions:**

🔍 **Where is fraud happening?**  
💰 **What is the financial impact?**  
🚨 **Which fraudulent transactions should be investigated first?**

---

## **🏢 BUSINESS PROBLEM**

Financial institutions process a large number of transactions every day, making manual identification of suspicious activity difficult.

Although fraudulent transactions represent a small proportion of the overall transaction population, they can create significant financial losses and reputational risk.

This project analyzes transaction characteristics such as:

- Transaction type
- Transaction amount
- Sender and receiver balances
- Fraud indicators
- Transaction steps
- Transaction frequency

The objective is to convert these transaction-level records into **fraud-monitoring indicators and actionable risk insights**.

---

## **🗂️ DATASET**

The project uses the **PaySim financial transaction dataset**.

### **Important Fields**

| Field | Description |
|---|---|
| `step` | Transaction time step |
| `type` | Transaction type |
| `amount` | Transaction amount |
| `nameOrig` | Originating account |
| `oldbalanceOrg` | Original sender balance |
| `newbalanceOrig` | Sender balance after transaction |
| `nameDest` | Destination account |
| `oldbalanceDest` | Original receiver balance |
| `newbalanceDest` | Receiver balance after transaction |
| `isFraud` | Fraud indicator |
| `isFlaggedFraud` | Existing fraud flag |

---

## **🛠️ TOOLS & TECHNOLOGIES**

| Tool | Purpose |
|---|---|
| 🗄️ **MySQL** | Data preparation, querying and analysis |
| 🔍 **SQL** | Fraud pattern and risk analysis |
| 📊 **Power BI** | Interactive fraud dashboard |
| 🧮 **DAX** | KPIs, calculated measures and risk table |
| 🐙 **GitHub** | Project documentation and version control |

---

## **🔍 SQL ANALYSIS**

SQL forms the analytical foundation of the project.

### **Key Analysis Performed**

- Transaction volume analysis
- Transaction amount analysis
- Fraudulent transaction identification
- Fraud rate calculation
- Fraud amount analysis
- Fraud analysis by transaction type
- Fraud trends across transaction steps
- Sender and receiver balance analysis
- High-value fraudulent transaction identification
- Risk-focused transaction analysis
- Transaction-frequency and repeated-activity analysis

### **SQL Concepts Used**

The project applies practical SQL techniques including:

`CASE Statements` · `Aggregations` · `Subqueries` · `CTEs` · `Joins` · `Window Functions`

These techniques transform raw transaction records into meaningful fraud and risk indicators.

---

# **📊 POWER BI DASHBOARD**

The Power BI dashboard follows a simple analytical journey:

## **Overview → Investigation & Risk Analysis**

---

## **📄 PAGE 1 — CREDIT CARD FRAUD ANALYSIS**

### **🎯 Purpose**

Page 1 provides a **high-level view of fraudulent activity**, helping users understand the overall fraud situation and identify major patterns.

### **📌 Dashboard KPIs**

| KPI | Value |
|---|---:|
| Total Transactions | **6.36M** |
| Total Transaction Amount | **1.14T** |
| Fraudulent Transactions | **8K** |
| Fraud Rate | **0.13%** |
| Fraud Amount | **12.06bn** |

### **🔎 Analysis**

**📈 Fraud Per Hour**  
Shows how fraudulent transaction activity varies across transaction steps.

**🔄 Fraud Cases by Transaction Type**  
Highlights transaction types associated with fraudulent activity.

**💰 Transaction-Type Amount Analysis**  
Provides a monetary view of transaction activity across transaction types.

**🍩 Fraud vs Genuine Transactions**  
Compares fraudulent and genuine transaction volumes.

> **Page 1 answers:**  
> ### **“What is happening with fraud overall?”**

### **🖼️ Dashboard Preview**

Add your Page 1 screenshot here:

`Screenshots/Page_1_Credit_Card_Fraud_Analysis.png`

---

# **🚨 PAGE 2 — FRAUD INVESTIGATION & RISK ANALYSIS**

### **🎯 Purpose**

Page 2 moves from overall fraud monitoring to **detailed investigation and risk prioritization**.

### **📌 Dashboard KPIs**

| KPI | Value |
|---|---:|
| Fraudulent Transactions | **8K** |
| Fraud Amount | **12.06bn** |
| Average Fraud Amount | **1.47M** |
| Highest Fraud Amount | **10.00M** |

### **🔎 Analysis**

**💰 Fraud Amount by Transaction Type**  
Compares the financial impact of fraud across transaction types.

**📊 Fraud Cases by Transaction Type**  
Analyzes fraud exposure across transaction types.

**🚨 High-Value Fraudulent Transactions**  
Displays the highest-value fraudulent transactions for closer investigation.

**🎛️ Payment Type Filter**  
Allows users to focus the investigation on selected payment types.

**🔢 Step Filter**  
Allows users to investigate selected transaction steps.

### **🚨 High-Value Risk Analysis**

A dedicated `High-Value Risk Transactions` table is created using DAX to identify the **Top 20 fraudulent transactions ranked by transaction amount**.

This helps move the analysis from simply identifying fraud to **prioritizing transactions based on financial impact**.

> **Page 2 answers:**  
> ### **“Which fraudulent transactions require closer investigation?”**

### **🖼️ Dashboard Preview**

Add your Page 2 screenshot here:

`Screenshots/Page_2_Fraud_Investigation_Risk_Analysis.png`

---

# **🔄 DASHBOARD FLOW**

```text
                  TRANSACTION DATA
                         │
                         ▼
          ┌──────────────────────────┐
          │ PAGE 1 — OVERVIEW        │
          │                          │
          │ Fraud Volume             │
          │ Fraud Rate               │
          │ Fraud Trends             │
          │ Transaction Types        │
          │ Fraud vs Genuine         │
          └────────────┬─────────────┘
                       │
                       ▼
              IDENTIFY PATTERNS
                       │
                       ▼
          ┌──────────────────────────┐
          │ PAGE 2 — INVESTIGATION   │
          │                          │
          │ Fraud Amount             │
          │ Average / Highest Fraud  │
          │ High-Value Transactions  │
          │ Risk Prioritization      │
          └────────────┬─────────────┘
                       │
                       ▼
               INVESTIGATION
