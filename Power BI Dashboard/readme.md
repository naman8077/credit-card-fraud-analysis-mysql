# **Power BI Dashboard -- Step-by-Step Creation Guide**

# *Credit Card Fraud Analysis Project*

This guide documents how to create the two Power BI dashboard pages used
in the project:

Page 1 -- Credit Card Fraud Analysis

Page 2 -- Fraud Investigation & Risk Analysis

The steps are based on the final dashboard layout and the DAX
measures/table used in the project.

Part 1 --- Page 1: Credit Card Fraud Analysis

# **Step 1: Create the DAX measures**

Before building the Page 1 visuals, create these measures from the
Dataset table.

1. Average Fraud Amount

Average Fraud Amount =
CALCULATE(
    AVERAGE('Dataset'[amount]),
    'Dataset'[isFraud] = 1
)

2. Fraud Amount

Fraud Amount =
CALCULATE(
    SUM('Dataset'[amount]),
    'Dataset'[isFraud] = 1
)

3. Fraud Rate

Fraud Rate =
DIVIDE(
    [Fraudulent Transactions],
    [Total Transactions],
    0
)

4. Fraud Rate by Type

Fraud Rate by Type =
DIVIDE(
    [Fraudulent Transactions],
    [Total Transactions],
    0
)

5. Fraudulent Transactions

Fraudulent Transactions =
CALCULATE(
    COUNTROWS('Dataset'),
    'Dataset'[isFraud] = 1
)

6. Highest Fraud Amount

Highest Fraud Amount =
CALCULATE(
    MAX('Dataset'[amount]),
    'Dataset'[isFraud] = 1
)

7. Total Transaction Amount

Total Transaction Amount =
SUM('Dataset'[amount])

8. Total Transactions

Total Transactions =
COUNTROWS('Dataset')

9. Transaction Status

Transaction Status =
IF(
    'Dataset'[isFraud] = 1,
    "Fraud",
    "Genuine"
)

These are the measures used for the dashboard calculations.

Step 2: Create the Page 1 title

Add a Text box.

Enter: Credit Card Fraud Analysis

Place it at the top of the report.

Make the title bold and large.

Center-align it.

Step 3: Create the five KPI cards

Create five Card visuals and arrange them in one row.

Card 1 --- Total Transactions

Visual: Card

Field: Total Transactions

Card 2 --- Total Transaction Amount

Visual: Card

Field: Total Transaction Amount

Card 3 --- Fraudulent Transactions

Visual: Card

Field: Fraudulent Transactions

Card 4 --- Fraud Rate

Visual: Card

Field: Fraud Rate

Format as percentage.

Card 5 --- Fraud Amount

Visual: Card

Field: Fraud Amount

Place all five cards directly below the title.

Step 4: Create the Fraud Per Hour visual

Insert a Line chart.

Put step on the X-axis.

Use the fraudulent transaction count on the Y-axis.

Filter the visual to fraudulent transactions (isFraud = 1).

Set the title to: Fraud Per Hour

Resize the visual so it spans most of the page width.

The purpose is to show how fraudulent activity changes across
transaction steps.

Step 5: Create the first Fraud Cases by Transaction Type visual

Insert a Bar chart.

Add the transaction type field (type / Payment Type) to the
category axis.

Add fraudulent transaction count to Values.

Filter to fraudulent transactions.

Set the title to: Fraud Cases by Transaction Type

Position it in the bottom-left area.

Step 6: Create the transaction-type amount visual

Insert a Bar chart.

Add transaction type / payment type to the category axis.

Add the relevant transaction amount measure to Values.

Apply the required fraud filter if using the fraud amount measure.

Set the title according to the final dashboard layout.

Place it next to the first transaction-type chart.

Step 7: Create Fraud vs Genuine Transactions

Insert a Donut chart.

Add Transaction Status to the Legend.

Add transaction count to Values.

Transaction Status separates transactions into:

Fraud

Genuine

Set the title to: Fraud vs Genuine Transactions

Place it on the bottom-right.

Step 8: Format Page 1

Arrange the page in this order:

                 Credit Card Fraud Analysis
                         │
 ┌──────────┬──────────┬──────────┬──────────┬──────────┐
 │ Total    │ Total    │ Fraud    │ Fraud    │ Fraud    │
 │ Trans.   │ Amount   │ Trans.   │ Rate     │ Amount   │
 └──────────┴──────────┴──────────┴──────────┴──────────┘
                         │
                 Fraud Per Hour
                         │
 ┌────────────────┬────────────────┬────────────────┐
 │ Fraud Cases by │ Transaction-   │ Fraud vs       │
 │ Transaction    │ Type Amount     │ Genuine        │
 │ Type           │ Analysis       │ Transactions   │
 └────────────────┴────────────────┴────────────────┘

Keep fonts, headings, spacing and visual formatting consistent.

# **Part 2 --- Page 2: Fraud Investigation & Risk Analysis**

Step 1: Create the High-Value Risk Transactions table

For Page 2, create a New Table using:

High-Value Risk Transactions =
TOPN(
    20,
    FILTER(
        'Dataset',
        'Dataset'[isFraud] = 1
    ),
    'Dataset'[amount],
    DESC
)

This filters the dataset to fraudulent transactions and keeps the top
20 transactions by amount.

Step 2: Create the Page 2 title

Add a Text box.

Enter: Fraud Investigation & Risk Analysis

Make it bold and large.

Center-align it.

Keep the title style consistent with Page 1.

Step 3: Create the four KPI cards

Create four Card visuals.

Card 1 --- Fraudulent Transactions

Field: Fraudulent Transactions

Card 2 --- Fraud Amount

Field: Fraud Amount

Card 3 --- Average Fraud Amount

Field: Average Fraud Amount

Card 4 --- Highest Fraud Amount

Field: Highest Fraud Amount

Arrange the four cards in one row below the title.

Step 4: Create Fraud Amount by Transaction Type

Insert a Bar chart.

Add transaction type to the category axis.

Add Fraud Amount to Values.

Filter to fraudulent transactions where required.

Set the title to: Fraud Amount by Transaction Type

Place it on the left side of Page 2.

Step 5: Create Fraud Cases by Transaction Type

Insert another Bar chart.

Add transaction type to the category axis.

Add the fraud case/rate measure used in the final dashboard.

Filter to fraudulent transactions where required.

Set the title to: Fraud Cases by Transaction Type

Place it below the first chart on the left.

Step 6: Create the High-Value Fraudulent Transactions table

Select the High-Value Risk Transactions calculated table.

Insert a Table visual.

Add these fields:

step

Payment Type / type

amount

nameOrig

nameDest

isFlaggedFraud

Sort amount in descending order.

Set the title to: High-Value Fraudulent Transactions

Position the table in the center of the page.

The table is intended to make the highest-value fraudulent transactions
easy to review.

Step 7: Add the Payment Type filter

Insert a Slicer.

Add Payment Type / transaction type.

Configure it as a tile/button-style slicer if desired.

Place it on the right side of the page.

The final dashboard allows selection of payment types such as:

CASH_OUT

TRANSFER

Step 8: Add the Step filter

Insert another Slicer.

Add the step field.

Use a tile/button-style layout if desired.

Place it below the Payment Type slicer.

This allows users to investigate selected transaction steps.

Step 9: Format Page 2

Arrange the page approximately as:

              Fraud Investigation & Risk Analysis
                              │
       ┌──────────┬──────────┬──────────┬──────────┐
       │ Fraud    │ Fraud    │ Average  │ Highest  │
       │ Trans.   │ Amount   │ Fraud    │ Fraud    │
       │          │          │ Amount   │ Amount   │
       └──────────┴──────────┴──────────┴──────────┘
                              │
 ┌──────────────────┬─────────────────────────┬──────────────┐
 │ Fraud Amount by  │ High-Value Fraudulent   │ Payment Type │
 │ Transaction Type │ Transactions             │              │
 │                  │                         │              │
 │ Fraud Cases by   │ step / Payment Type     │ Step         │
 │ Transaction Type │ amount / nameOrig       │              │
 │                  │ nameDest / isFlagged... │              │
 └──────────────────┴─────────────────────────┴──────────────┘

Part 3 --- Final Dashboard Logic

The two pages should work together rather than repeat the same analysis.

Page 1 --- Overview

Purpose: Monitor and understand overall fraud activity.

Overall Transaction Data
        ↓
Fraud KPIs
        ↓
Fraud Trends
        ↓
Transaction-Type Patterns
        ↓
Fraud vs Genuine

Page 2 --- Investigation

Purpose: Investigate and prioritize high-value fraudulent
transactions.

Fraudulent Transactions
        ↓
Financial Impact
        ↓
Average / Highest Fraud Amount
        ↓
Transaction-Type Risk
        ↓
Top 20 High-Value Fraudulent Transactions
        ↓
Investigation Priority

Page 1 vs Page 2

                      Page 1                  Page 2

Focus               Overall fraud analysis  Fraud investigation

Purpose             Identify patterns       Prioritize risk

Main view           Summary and trends      Detailed transaction
analysis

KPIs                5                       4

Fraud trend         Yes                     No

Transaction-type      Yes                     Yes
analysis

High-value            No                      Yes
transaction table

Payment Type filter No                      Yes

Step filter         No                      Yes

Final Dashboard Flow

Page 1 --- Overview & Pattern Identification

↓

Identify Fraud Trends and Transaction-Type Patterns

↓

Page 2 --- Investigation & Risk Prioritization

↓

Identify Top High-Value Fraudulent Transactions

↓

Prioritize Further Investigation
