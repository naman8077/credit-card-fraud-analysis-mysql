# **💳 CREDIT CARD FRAUD ANALYSIS — MYSQL + POWER BI**

> **Credit card fraud analysis using MySQL, SQL analytics, Power BI, and fraud detection insights.**

An end-to-end data analytics project focused on identifying **fraudulent transaction patterns, measuring financial impact, identifying high-risk behavior, and prioritizing high-value fraudulent transactions** using SQL and Power BI.

---

# **🎯 PROJECT OVERVIEW**

This project focuses on analyzing financial transaction data to identify fraudulent transaction patterns using **MySQL and SQL analytics**.

The analysis uses the **PaySim financial transaction dataset** and examines transaction characteristics such as:

* Transaction type
* Transaction amount
* Sender and receiver balances
* Fraud indicators
* Transaction frequency
* Transaction steps
* High-value transactions

The objective is to transform raw transaction data into meaningful insights that can help financial institutions:

* Understand fraud behavior
* Identify high-risk transactions
* Measure the financial impact of fraud
* Strengthen fraud monitoring
* Prioritize suspicious transactions for investigation
* Support fraud prevention strategies

The project combines **SQL-based analysis with an interactive Power BI dashboard** to provide both analytical and business-focused insights.

---

# **🏢 BUSINESS PROBLEM**

Financial institutions process a large number of transactions every day, making it difficult to manually identify suspicious activity.

Fraudulent transactions may represent only a small proportion of total transactions, but they can result in significant financial losses and reputational damage.

This project addresses the following business questions:

* How frequently does fraud occur compared with genuine transactions?
* Which transaction types are more exposed to fraudulent activity?
* Are fraudulent transactions associated with unusually high transaction amounts?
* Can abnormal sender or receiver balance movements indicate suspicious activity?
* Can repeated transaction behavior or transaction frequency help identify high-risk accounts?
* How can transaction-level analysis be converted into practical fraud-monitoring indicators?
* Which fraudulent transactions should be prioritized for further investigation?

---

# **🎯 PROJECT OBJECTIVES**

* Clean and prepare the transaction data for analysis using MySQL.
* Perform exploratory analysis to understand transaction and fraud patterns.
* Measure fraudulent transaction counts, amounts, and fraud rates.
* Analyze fraud across different transaction types and time periods.
* Identify suspicious transaction and account-level patterns using SQL.
* Analyze transaction amounts and balance movements as potential fraud indicators.
* Identify high-value fraudulent transactions.
* Use advanced SQL concepts such as `CASE` statements, aggregations, subqueries, CTEs, joins, and window functions.
* Generate business insights that can support fraud detection and risk management.
* Design a Power BI dashboard that presents important fraud KPIs, trends, risk indicators, and investigation-level information.

---

# **🗂️ DATASET**

The project uses the **PaySim financial transaction dataset**.

The dataset contains transaction-level information including transaction type, transaction amount, sender and receiver balances, fraud indicators, and transaction steps.

## **Important Dataset Fields**

| Field            | Description                                 |
| ---------------- | ------------------------------------------- |
| `step`           | Time step of the transaction                |
| `type`           | Transaction type                            |
| `amount`         | Transaction amount                          |
| `nameOrig`       | Originating account                         |
| `oldbalanceOrg`  | Original balance of the originating account |
| `newbalanceOrig` | New balance of the originating account      |
| `nameDest`       | Destination account                         |
| `oldbalanceDest` | Original balance of the destination account |
| `newbalanceDest` | New balance of the destination account      |
| `isFraud`        | Fraud indicator                             |
| `isFlaggedFraud` | Flagged fraud indicator                     |

---

# **🛠️ TOOLS & TECHNOLOGIES**

| Tool            | Purpose                                                   |
| --------------- | --------------------------------------------------------- |
| 🗄️ **MySQL**   | Data cleaning, preparation, querying and analysis         |
| 🔍 **SQL**      | Fraud detection, pattern analysis and risk identification |
| 📊 **Power BI** | Interactive dashboard and data visualization              |
| 🧮 **DAX**      | KPIs, calculated measures and high-value risk analysis    |
| 🐙 **GitHub**   | Project documentation and version control                 |

---

# **🔍 SQL ANALYSIS**

SQL was used as the analytical foundation of the project.

The transaction dataset was analyzed to identify patterns associated with fraudulent activity and potential financial risk.

## **📌 Key Analysis Performed**

### **Transaction Analysis**

* Transaction volume
* Total transaction amount
* Transaction distribution by type
* Transaction activity across transaction steps

### **Fraud Analysis**

* Fraudulent transaction count
* Fraud rate
* Total fraud amount
* Fraudulent transaction amounts
* Fraud distribution by transaction type
* Fraud trends across transaction steps

### **Risk & Suspicious Activity Analysis**

* High-value fraudulent transactions
* Unusually large transaction amounts
* Sender balance movements
* Receiver balance movements
* Repeated or unusual transaction activity
* Existing fraud indicators
* Transaction-level risk indicators

---

# **🧮 SQL CONCEPTS USED**

The project applies practical SQL techniques including:

`CASE Statements` · `Aggregations` · `Subqueries` · `CTEs` · `Joins` · `Window Functions`

These concepts were used to convert raw transaction records into useful:

* Fraud-rate metrics
* Transaction-level indicators
* Risk patterns
* Fraud monitoring metrics
* High-value transaction analysis

---

# **💡 KEY FINDINGS**

The SQL analysis highlights several important patterns that can be used to understand fraud risk.

> **Note:** The exact numerical values should be taken from the final query outputs when the project is published.

### **⚖️ Fraudulent transactions form a small share of the overall transaction population**

This makes fraud detection an **imbalanced-data problem**, where identifying meaningful risk signals is more important than simply looking at transaction volume.

### **🔄 Fraud activity is concentrated in particular transaction types**

Fraud is not evenly distributed across all transaction categories. Certain transaction types show comparatively higher exposure to fraudulent activity.

### **💰 Transaction amount is an important risk indicator**

Unusually large or abnormal transactions deserve additional scrutiny because they can represent greater potential financial impact.

### **🏦 Sender and receiver balance movements can provide additional signals**

Changes in sender and receiver balances can reveal inconsistencies or unusual transaction behavior that may be useful as fraud indicators.

### **🔁 Repeated or unusual transaction activity can indicate risk**

Transaction frequency and repeated activity can help identify accounts or transaction patterns that require closer monitoring.

### **🎯 Combining multiple indicators provides stronger fraud analysis**

Combining:

**Transaction Type + Amount + Balance Behavior + Transaction Frequency + Fraud Flags**

provides a stronger basis for identifying suspicious activity than relying on a single indicator.

### **📊 SQL analytics can convert raw transaction records into business metrics**

SQL analysis transforms transaction-level records into fraud-rate, risk-pattern, and monitoring metrics that are easier for business users to interpret.

---

# **📊 DASHBOARD IDEA — FRAUD MONITORING DASHBOARD**

The SQL analysis is converted into an interactive **Power BI fraud-monitoring dashboard**.

The dashboard focuses on:

* KPIs
* Fraud trends
* Transaction-type analysis
* Risk segments
* High-value transactions
* Investigation-level details

Rather than displaying every available column, the dashboard focuses on the information most useful for **fraud monitoring and risk prioritization**.

---

# **📈 EXECUTIVE KPI SECTION**

The dashboard includes key fraud-monitoring KPIs such as:

* Total Transactions
* Total Transaction Amount
* Total Fraudulent Transactions
* Fraud Rate (%)
* Total Fraud Amount
* Average Fraudulent Transaction Amount
* Highest Fraud Amount

These KPIs provide a quick view of the overall fraud situation and financial impact.

---

# **📈 FRAUD TREND ANALYSIS**

The dashboard analyzes fraudulent activity across transaction steps.

Key analysis includes:

* Fraudulent transactions across time/steps
* Fraud activity trends
* Comparison of genuine vs fraudulent transactions
* Transaction-step filtering for investigation

---

# **🔄 TRANSACTION TYPE ANALYSIS**

The dashboard analyzes fraud exposure across transaction types.

Key visuals include:

* Fraud cases by transaction type
* Fraud amount by transaction type
* Fraud-rate analysis by transaction type
* Transaction-type comparison
* Identification of transaction types with comparatively higher fraud exposure

---

# **🚨 RISK & SUSPICIOUS ACTIVITY SECTION**

The dashboard includes investigation-focused analysis such as:

* Top high-value fraudulent transactions
* Accounts with repeated suspicious activity
* Transactions with unusual balance changes
* Transactions flagged by existing fraud indicators
* Detailed transaction-level information for investigation

---

# **🎛️ RECOMMENDED DASHBOARD FILTERS**

Recommended filters include:

* Transaction Type
* Fraud Status
* Time / Step
* Transaction Amount Range
* Flagged Fraud Status

The final dashboard specifically includes **Payment Type** and **Step** filtering on the investigation page.

---

# **📊 POWER BI DASHBOARD**

The final Power BI dashboard uses a two-page analytical approach:

# **Overview → Investigation & Risk Analysis**

The two pages are intentionally designed for different purposes rather than repeating the same analysis.

---

# **📄 PAGE 1 — CREDIT CARD FRAUD ANALYSIS**

### **🎯 Purpose**

Page 1 provides a **high-level overview of fraudulent activity** and identifies major fraud patterns.

It is designed for:

**Monitoring → Understanding → Pattern Identification**

---

## **📌 PAGE 1 — KEY KPIs**

| KPI                          |       Value |
| ---------------------------- | ----------: |
| **Total Transactions**       |   **6.36M** |
| **Total Transaction Amount** |   **1.14T** |
| **Fraudulent Transactions**  |      **8K** |
| **Fraud Rate**               |   **0.13%** |
| **Fraud Amount**             | **12.06bn** |

---

## **🔎 PAGE 1 — DASHBOARD ANALYSIS**

### **📈 Fraud Per Hour**

Shows how fraudulent transaction activity varies across transaction steps.

This helps identify where fraudulent activity is more concentrated.

### **🔄 Fraud Cases by Transaction Type**

Shows the distribution of fraudulent activity across different transaction types.

### **💰 Transaction-Type Amount Analysis**

Provides a monetary view of transaction activity across transaction types.

### **🍩 Fraud vs Genuine Transactions**

Compares fraudulent and genuine transaction volumes and provides an overall view of the fraud proportion.

---

### **💡 PAGE 1 BUSINESS PURPOSE**

Page 1 provides the overall fraud picture and helps stakeholders identify important patterns before moving into detailed investigation.

> **Page 1 answers:**
>
> ### **“What is happening with fraud overall?”**

---

# **🚨 PAGE 2 — FRAUD INVESTIGATION & RISK ANALYSIS**

### **🎯 Purpose**

Page 2 moves from overall fraud monitoring to **detailed investigation and risk prioritization**.

It focuses on financial impact and high-value fraudulent transactions.

---

## **📌 PAGE 2 — KEY KPIs**

| KPI                         |       Value |
| --------------------------- | ----------: |
| **Fraudulent Transactions** |      **8K** |
| **Fraud Amount**            | **12.06bn** |
| **Average Fraud Amount**    |   **1.47M** |
| **Highest Fraud Amount**    |  **10.00M** |

---

## **🔎 PAGE 2 — DASHBOARD ANALYSIS**

### **💰 Fraud Amount by Transaction Type**

Compares the financial impact of fraudulent transactions across transaction types.

### **📊 Fraud Cases by Transaction Type**

Analyzes fraud exposure across transaction types.

### **🚨 High-Value Fraudulent Transactions**

The dashboard includes a detailed table focused on the **Top 20 fraudulent transactions ranked by transaction amount**.

This helps identify transactions that may require closer investigation based on their potential financial impact.

### **🎛️ Payment Type Filtering**

Allows users to filter the investigation based on payment/transaction type.

### **🔢 Step-Level Filtering**

Allows users to investigate selected transaction steps.

---

### **💡 PAGE 2 BUSINESS PURPOSE**

Page 2 focuses on moving from fraud identification to **investigation and risk prioritization**.

> **Page 2 answers:**
>
> ### **“Which fraudulent transactions require closer investigation?”**

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
```

---

# **📌 WHY TWO PAGES?**

The dashboard separates **fraud monitoring from detailed investigation**.

### **📄 Page 1 — Monitor & Understand**

Provides:

* Overall fraud KPIs
* Fraud trends
* Transaction-type patterns
* Fraud vs genuine comparison

### **🚨 Page 2 — Investigate & Prioritize**

Provides:

* Fraud financial impact
* Average fraud amount
* Highest fraud amount
* Transaction-type risk analysis
* High-value fraudulent transactions
* Payment Type filtering
* Step-level investigation

### **Analytical Progression**

**Overview → Pattern Identification → Investigation → Risk Prioritization**

---

# **🚨 HIGH-VALUE RISK ANALYSIS**

The project goes beyond simply identifying fraudulent transactions.

The Page 2 investigation section focuses on identifying the transactions with the greatest monetary value.

A dedicated:

`High-Value Risk Transactions`

table identifies the:

**Top 20 fraudulent transactions by transaction amount.**

### **Investigation Flow**

```text
Fraudulent Transactions
        ↓
Measure Financial Impact
        ↓
Analyze Transaction Types
        ↓
Identify High-Value Transactions
        ↓
Prioritize Investigation
```

This creates a practical connection between **fraud detection and investigation prioritization**.

---

# **💡 BUSINESS INSIGHTS**

The analysis provides several practical business insights.

### **💰 Financial Impact**

The dashboard measures the overall monetary impact associated with fraudulent transactions.

### **🔄 Fraud Patterns**

Transaction types and transaction steps can be analyzed to identify areas with higher fraud activity.

### **🚨 High-Value Risk**

The investigation page highlights the highest-value fraudulent transactions so that investigation efforts can be prioritized.

### **📊 Fraud Monitoring**

The dashboard provides a quick comparison between fraudulent and genuine transactions.

### **🎯 Risk Prioritization**

High-value fraudulent transactions can be prioritized for further investigation based on their potential financial impact.

---

# **🛡️ BUSINESS RECOMMENDATIONS**

Based on the analysis, organizations can consider:

* 🚨 Prioritizing investigation of **high-value fraudulent transactions**
* 🔄 Increasing monitoring of transaction types showing higher fraud exposure
* 📈 Monitoring unusual activity across transaction steps
* 💰 Introducing automated alerts for suspicious high-value transactions
* 🏦 Monitoring abnormal sender and receiver balance movements
* 🔁 Investigating repeated or unusual transaction activity
* 🎯 Combining multiple risk indicators rather than relying on a single fraud signal
* 📊 Using interactive dashboards to support faster fraud-monitoring decisions

---

# **🧠 SKILLS DEMONSTRATED**

## **💻 Technical Skills**

`SQL` · `MySQL` · `Power BI` · `DAX` · `Data Cleaning` · `Data Visualization` · `Dashboard Development`

## **📊 Analytical Skills**

`Fraud Analysis` · `Risk Analysis` · `Trend Analysis` · `Transaction Analysis` · `Exploratory Data Analysis` · `KPI Development` · `High-Value Transaction Analysis` · `Pattern Identification`

## **💼 Business Skills**

`Risk Identification` · `Risk Prioritization` · `Financial Impact Analysis` · `Business Insights` · `Data-Driven Recommendations` · `Fraud Monitoring`

---

# **🚀 PROJECT WORKFLOW**

```text
Raw Transaction Data
        ↓
Data Cleaning & Preparation
        ↓
SQL Exploration & Analysis
        ↓
Fraud Pattern Identification
        ↓
Risk & High-Value Transaction Analysis
        ↓
Power BI Dashboard
        ↓
Business Insights
        ↓
Recommendations
```

---

# **📈 ANALYTICAL APPROACH**

## **Step 1 — Data Preparation**

Clean and prepare the transaction dataset using MySQL.

## **Step 2 — Exploratory Analysis**

Understand transaction volumes, transaction types, amounts, balances, and fraud indicators.

## **Step 3 — Fraud Analysis**

Measure fraudulent transactions, fraud rate, fraud amount, and fraud distribution.

## **Step 4 — Pattern Identification**

Analyze transaction types, transaction steps, balance movements, and repeated activity.

## **Step 5 — Risk Analysis**

Identify high-value and potentially suspicious transactions.

## **Step 6 — Dashboard Development**

Convert analytical results into interactive Power BI KPIs and visualizations.

## **Step 7 — Business Insights**

Interpret the results and translate them into practical fraud-monitoring and risk-management recommendations.

---

# **📁 PROJECT STRUCTURE**

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

# **🖼️ POWER BI DASHBOARD PREVIEW**

## **Page 1 — Credit Card Fraud Analysis**

Add the Page 1 screenshot here:

```markdown
![Page 1 - Credit Card Fraud Analysis](Screenshots/Page_1_Credit_Card_Fraud_Analysis.png)
```

## **Page 2 — Fraud Investigation & Risk Analysis**

Add the Page 2 screenshot here:

```markdown
![Page 2 - Fraud Investigation & Risk Analysis](Screenshots/Page_2_Fraud_Investigation_Risk_Analysis.png)
```

---

# **⭐ CONCLUSION**

This project demonstrates how **MySQL and SQL analytics can be used to analyze financial transactions and identify patterns associated with fraudulent activity**.

By combining:

* Data cleaning
* Exploratory analysis
* Aggregations
* Conditional logic
* CTEs
* Joins
* Window functions
* Fraud-rate analysis
* Risk analysis
* High-value transaction analysis

the project converts a large transaction dataset into useful fraud-monitoring and risk-management insights.

The analysis is further strengthened by connecting the SQL results to an interactive **Power BI dashboard**.

The dashboard follows an:

# **Overview → Investigation**

approach.

**Page 1** provides the high-level fraud picture, including KPIs, trends, transaction-type analysis, and fraud-versus-genuine comparison.

**Page 2** drills down into financial impact, fraud amounts, transaction-type risk, and the **Top 20 High-Value Fraudulent Transactions**.

Overall, the project demonstrates practical **SQL, MySQL, Power BI, DAX, data analysis, fraud detection, risk analysis, data visualization, and business problem-solving skills** relevant to Data Analyst and Business Analyst roles.

---

# **👤 PROJECT HIGHLIGHT**

> **From raw transaction data → SQL analysis → fraud patterns → Power BI visualization → risk prioritization → actionable business insights.**
