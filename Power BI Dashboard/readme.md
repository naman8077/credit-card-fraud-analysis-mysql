💳 Credit Card Fraud Analysis --- MySQL + Power BI

End-to-end data analytics project for identifying fraudulent
transaction patterns, measuring financial impact, and prioritizing
high-value transactions for investigation.

🎯 Project at a Glance

This project analyzes the PaySim financial transaction dataset using
MySQL, SQL analytics, Power BI, and DAX.

The analysis moves from raw transaction data to business-focused fraud
insights:

Raw Data → SQL Analysis → Fraud Patterns → Risk Analysis → Power BI
Dashboard → Business Recommendations

The project answers three key questions:

🔍 Where is fraud happening?
💰 What is the financial impact?
🚨 Which fraudulent transactions should be investigated first?

🏢 Business Problem

Financial institutions process a large number of transactions every day,
making manual identification of suspicious activity difficult.

Although fraudulent transactions represent a small proportion of the
overall transaction population, they can create significant financial
losses and reputational risk.

This project analyzes transaction characteristics such as:

Transaction type

Transaction amount

Sender and receiver balances

Fraud indicators

Transaction steps

Transaction frequency

The objective is to convert these transaction-level records into
fraud-monitoring indicators and actionable risk insights.

🗂️ Dataset

The project uses the PaySim financial transaction dataset.

Important fields

Field              Description

step             Transaction time step
type             Transaction type
amount           Transaction amount
nameOrig         Originating account
oldbalanceOrg    Original sender balance
newbalanceOrig   Sender balance after transaction
nameDest         Destination account
oldbalanceDest   Original receiver balance
newbalanceDest   Receiver balance after transaction
isFraud          Fraud indicator
isFlaggedFraud   Existing fraud flag

🛠️ Tools & Technologies

Tool              Purpose

🗄️ MySQL      Data preparation, querying and analysis
🔍 SQL        Fraud pattern and risk analysis
📊 Power BI   Interactive fraud dashboard
🧮 DAX        KPIs, calculated measures and risk table
🐙 GitHub     Project documentation and version control

🔍 SQL Analysis

SQL forms the analytical foundation of the project.

Key analysis performed

Transaction volume analysis

Transaction amount analysis

Fraudulent transaction identification

Fraud rate calculation

Fraud amount analysis

Fraud analysis by transaction type

Fraud trends across transaction steps

Sender and receiver balance analysis

High-value fraudulent transaction identification

Risk-focused transaction analysis

Transaction-frequency and repeated-activity analysis

SQL concepts used

The project applies practical SQL techniques including:

CASE Statements · Aggregations · Subqueries · CTEs · Joins ·
Window Functions

These techniques transform raw transaction records into meaningful fraud
and risk indicators.

📊 Power BI Dashboard

The Power BI dashboard follows a simple analytical journey:

Overview → Investigation & Risk Analysis

📄 Page 1 --- Credit Card Fraud Analysis

🎯 Purpose

Page 1 provides a high-level view of fraudulent activity, helping
users understand the overall fraud situation and identify major
patterns.

📌 Dashboard KPIs

KPI                                Value

Total Transactions             6.36M
Total Transaction Amount       1.14T
Fraudulent Transactions           8K
Fraud Rate                     0.13%
Fraud Amount                 12.06bn

🔎 Analysis

📈 Fraud Per Hour
Shows how fraudulent transaction activity varies across transaction
steps.

🔄 Fraud Cases by Transaction Type
Highlights transaction types associated with fraudulent activity.

💰 Transaction-Type Amount Analysis
Provides a monetary view of transaction activity across transaction
types.

🍩 Fraud vs Genuine Transactions
Compares fraudulent and genuine transaction volumes.

Page 1 answers:
### "What is happening with fraud overall?"

🖼️ Dashboard Preview

Add your Page 1 screenshot here:

Screenshots/Page_1_Credit_Card_Fraud_Analysis.png

🚨 Page 2 --- Fraud Investigation & Risk Analysis

🎯 Purpose

Page 2 moves from overall fraud monitoring to detailed investigation
and risk prioritization.

📌 Dashboard KPIs

KPI                               Value

Fraudulent Transactions          8K
Fraud Amount                12.06bn
Average Fraud Amount          1.47M
Highest Fraud Amount         10.00M

🔎 Analysis

💰 Fraud Amount by Transaction Type
Compares the financial impact of fraud across transaction types.

📊 Fraud Cases by Transaction Type
Analyzes fraud exposure across transaction types.

🚨 High-Value Fraudulent Transactions
Displays the highest-value fraudulent transactions for closer
investigation.

🎛️ Payment Type Filter
Allows users to focus the investigation on selected payment types.

🔢 Step Filter
Allows users to investigate selected transaction steps.

🚨 High-Value Risk Analysis

A dedicated High-Value Risk Transactions table is created using DAX to
identify the Top 20 fraudulent transactions ranked by transaction
amount.

This helps move the analysis from simply identifying fraud to
prioritizing transactions based on financial impact.

Page 2 answers:
### "Which fraudulent transactions require closer investigation?"

🖼️ Dashboard Preview

Add your Page 2 screenshot here:

Screenshots/Page_2_Fraud_Investigation_Risk_Analysis.png

🔄 Dashboard Flow

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

Why two pages?

Page 1 --- Monitor & Understand
Provides the overall fraud picture and identifies important patterns.

Page 2 --- Investigate & Prioritize
Drills down into financial impact and high-value fraudulent
transactions.

The analytical progression

Overview → Pattern Identification → Investigation → Risk
Prioritization

💡 Key Findings & Insights

The SQL analysis and dashboard highlight several important fraud-risk
patterns.

1. ⚖️ Fraud is an imbalanced-data problem

Fraudulent transactions represent a small share of the overall
transaction population, making it important to focus on risk
indicators rather than transaction volume alone.

2. 🔄 Fraud is concentrated in particular transaction types

Fraud activity is not evenly distributed across all transaction
categories. Transaction-type analysis can therefore help identify
areas requiring additional monitoring.

3. 💰 Transaction amount is an important risk indicator

Unusually large or abnormal transactions deserve additional scrutiny
because transaction value can significantly increase the potential
financial impact of fraud.

4. 🏦 Balance movements can provide additional signals

Changes in sender and receiver balances can reveal unusual or
inconsistent transaction behavior that may be useful when evaluating
fraud risk.

5. 🔁 Repeated or unusual activity can indicate risk

Transaction frequency and repeated activity can help identify accounts
or transaction patterns that may require closer monitoring.

6. 🎯 Multiple indicators provide stronger analysis

Combining:

Transaction Type + Amount + Balance Behavior + Transaction Frequency +
Fraud Flags

provides a stronger basis for identifying suspicious activity than
relying on a single indicator.

🛡️ Business Recommendations

Based on the analysis, organizations can consider:

🚨 Prioritizing investigation of high-value fraudulent
transactions

🔄 Increasing monitoring of transaction types with higher fraud
exposure

📈 Monitoring unusual activity across transaction steps

💰 Creating automated alerts for suspicious high-value transactions

🏦 Monitoring abnormal sender/receiver balance movements

🔁 Investigating repeated or unusual transaction activity

🎯 Combining multiple risk indicators rather than relying on a
single fraud signal

📊 Using interactive dashboards to support faster fraud-monitoring
decisions

🧠 Skills Demonstrated

💻 Technical Skills

SQL · MySQL · Power BI · DAX · Data Cleaning ·
Data Visualization

📊 Analytical Skills

Fraud Analysis · Risk Analysis · Trend Analysis ·
Transaction Analysis · KPI Development ·
High-Value Transaction Analysis

💼 Business Skills

Risk Identification · Risk Prioritization · Business Insights ·
Data-Driven Recommendations

📁 Project Structure

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

🚀 Project Workflow

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

⭐ Conclusion

This project demonstrates how MySQL, SQL analytics, Power BI, and
DAX can be combined to transform a large financial transaction dataset
into practical fraud-monitoring insights.

The analysis progresses from:

Raw Transaction Data → Fraud Patterns → Financial Impact → Risk
Prioritization → Investigation

The Power BI dashboard complements the SQL analysis by providing an
interactive view of both overall fraud activity and high-value
fraudulent transactions.

Overall, the project demonstrates practical skills in SQL, data
analysis, fraud detection, risk analysis, data visualization, and
business problem-solving.
