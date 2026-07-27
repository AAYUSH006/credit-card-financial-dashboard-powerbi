# DAX Measures & Calculated Columns

# Overview

This dashboard uses **Data Analysis Expressions (DAX)** to create both calculated columns and measures that support customer segmentation, financial KPIs, and time-based analysis.

The DAX logic enables dynamic reporting, customer classification, and week-over-week revenue analysis.

---

# DAX Components Used

The project includes two types of DAX objects:

- **Calculated Columns** – Used to categorize and enrich the dataset before visualization.
- **Measures** – Used to calculate dynamic business metrics that respond to report filters and slicers.

---

# Calculated Columns

## 1. Age Group

### Business Purpose

Categorizes customers into predefined age groups to simplify demographic analysis and customer segmentation.

### DAX

```DAX
AgeGroup =
SWITCH(
    TRUE(),
    'customer'[Customer_Age] < 30, "20-30",
    'customer'[Customer_Age] >= 30 && 'customer'[Customer_Age] < 40, "30-40",
    'customer'[Customer_Age] >= 40 && 'customer'[Customer_Age] < 50, "40-50",
    'customer'[Customer_Age] >= 50 && 'customer'[Customer_Age] < 60, "50-60",
    'customer'[Customer_Age] >= 60, "60+",
    "Unknown"
)
```

### Used In

- Revenue by Age Group
- Customer Segmentation
- Customer Report

---

## 2. Income Group

### Business Purpose

Groups customers into income brackets to analyze revenue contribution by earning capacity.

### DAX

```DAX
IncomeGroup =
SWITCH(
    TRUE(),
    'customer'[Income] < 35000, "Low",
    'customer'[Income] >= 35000 && 'customer'[Income] < 70000, "Mid",
    'customer'[Income] >= 70000, "High",
    "Unknown"
)
```

### Used In

- Revenue by Salary Group
- Customer Segmentation
- Customer Report

---

## 3. Week Number

### Business Purpose

Extracts the calendar week from the transaction date to support weekly reporting and trend analysis.

### DAX

```DAX
Week_Num2 =
WEEKNUM(credit_card[Week_Start_Date])
```

### Used In

- Weekly Revenue Analysis
- Week-over-Week Comparison

---

## 4. Revenue

### Business Purpose

Creates a business-defined Revenue metric by combining annual fees, transaction amount, and interest earned.

### DAX

```DAX
Revenue =
credit_card[Annual_Fees]
+ credit_card[Total_Trans_Amt]
+ credit_card[Interest_Earned]
```

### Business Formula

Revenue = Annual Fees + Transaction Amount + Interest Earned

### Used In

- KPI Card
- Revenue Trend
- Customer Report
- Transaction Report

---

# Measures

## 1. Current Week Revenue

### Business Purpose

Calculates revenue generated during the latest available reporting week.

### DAX

```DAX
Current_Week_Revenue =
CALCULATE(
    SUM(credit_card[Revenue]),
    FILTER(
        ALL(credit_card),
        credit_card[Week_Num2] =
        MAX(credit_card[Week_Num2])
    )
)
```

### Used In

- Weekly KPI
- Executive Dashboard
- Trend Analysis

---

## 2. Previous Week Revenue

### Business Purpose

Calculates revenue generated during the previous reporting week for comparison purposes.

### DAX

```DAX
Previous_Week_Revenue =
CALCULATE(
    SUM(credit_card[Revenue]),
    FILTER(
        ALL(credit_card),
        credit_card[Week_Num2] =
        MAX(credit_card[Week_Num2]) - 1
    )
)
```

### Used In

- Week-over-Week Analysis
- Revenue Comparison

---

# Business Logic Summary

| DAX Object | Purpose |
|------------|---------|
| AgeGroup | Customer age segmentation |
| IncomeGroup | Income-based customer classification |
| Week_Num2 | Weekly reporting |
| Revenue | Business revenue calculation |
| Current_Week_Revenue | Latest week's revenue |
| Previous_Week_Revenue | Previous week's revenue |

---

# DAX Concepts Demonstrated

This project demonstrates practical use of several core DAX concepts:

- SWITCH()
- TRUE() pattern
- WEEKNUM()
- CALCULATE()
- FILTER()
- ALL()
- SUM()
- MAX()
- Calculated Columns
- Measures
- Context Transition
- Dynamic Filter Context

---

# Business Impact

The DAX calculations enable stakeholders to:

- Segment customers into meaningful age and income groups.
- Monitor revenue performance over time.
- Compare current and previous week revenue.
- Analyze customer profitability.
- Build dynamic and interactive reports that respond to slicers and filters.

---

# Best Practices Followed

- Used calculated columns for reusable categorical attributes.
- Used measures for dynamic aggregations.
- Created descriptive DAX names.
- Leveraged CALCULATE() and FILTER() for context-aware analysis.
- Kept business logic centralized within the data model.

---

# Summary

The dashboard combines calculated columns and measures to transform raw transactional data into actionable business insights. Customer segmentation, custom revenue calculations, and week-over-week comparisons provide a strong analytical foundation for executive reporting and business decision-making.
