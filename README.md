# 💳 Credit Card Financial Dashboard | Power BI

<p align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)

![DAX](https://img.shields.io/badge/DAX-Measures-blue)

![Power Query](https://img.shields.io/badge/Power%20Query-ETL-success)

![Data Modeling](https://img.shields.io/badge/Data%20Model-Star%20Schema-orange)

![Business Intelligence](https://img.shields.io/badge/Business-Intelligence-purple)

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

</p>

---

# 📖 Project Overview

This project presents an **interactive Credit Card Financial Dashboard** built using **Microsoft Power BI** to analyze customer behavior, transaction patterns, and overall financial performance.

The solution combines customer demographic information with transaction-level data to provide executives and business stakeholders with actionable insights into revenue generation, customer segmentation, spending behavior, and portfolio performance.

The dashboard demonstrates the complete Business Intelligence workflow, including:

- Data Preparation
- Data Modeling
- DAX Development
- Dashboard Design
- Business Analysis
- Executive Reporting
- Strategic Recommendations

---

# 📸 Dashboard Preview

## Customer Report

<p align="center">
<img src="Reports/Customer_Report.png" width="95%">
</p>

---

## Transaction Report

<p align="center">
<img src="Reports/Transaction_Report.png" width="95%">
</p>

---

# 🎯 Business Problem

Financial institutions generate large volumes of customer and transaction data every day.

Without centralized reporting, it becomes difficult to answer critical business questions such as:

- Which customers generate the highest revenue?
- Which states contribute the most business?
- Which card category performs best?
- How is revenue changing over time?
- Which customer segments should be targeted?
- How healthy is the customer portfolio?

This dashboard addresses these challenges through interactive visualizations and business-focused analytics.

---

# 🎯 Project Objectives

The primary objectives of this project are:

- Build an executive-level financial dashboard.
- Analyze customer demographics.
- Monitor revenue and transaction performance.
- Evaluate customer acquisition and activation.
- Identify high-value customer segments.
- Support strategic business decision-making.
- Demonstrate end-to-end Power BI development skills.

---

# 📂 Dataset Information

The project uses two datasets.

| Dataset | Description |
|----------|-------------|
| customer.csv | Customer demographic information |
| credit_card.csv | Credit card transaction and financial data |

Both datasets are linked using **Client_Num**, enabling integrated customer and transaction analysis.

---

# 🛠 Technology Stack

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Star Schema Data Modeling
- CSV Data Sources
- Microsoft Excel (Data Validation)
- Git & GitHub

---

# 📊 Dashboard Features

## Customer Report

- Revenue Analysis
- Customer Segmentation
- Income Analysis
- Occupation Analysis
- Customer Satisfaction
- Geographic Performance
- Education Analysis
- Marital Status Analysis

---

## Transaction Report

- Revenue Tracking
- Transaction Analysis
- Quarterly Trends
- Card Category Performance
- Expenditure Analysis
- Transaction Mode Analysis
- Customer Acquisition Cost
- Interest Analysis

---

# 📈 Key Performance Indicators (KPIs)

The dashboard tracks:

- Total Revenue
- Interest Earned
- Transaction Amount
- Transaction Count
- Customer Count
- Activation Rate
- Delinquency Rate
- Customer Satisfaction Score

---

# 🧠 Data Model

The dashboard follows a **Star Schema** design.

```
Customer Dimension
        │
        │
        ▼
Transaction Fact Table
```

This structure improves model performance, simplifies relationships, and supports efficient DAX calculations.

For more details, see:

📄 Documentation/02_Data_Model.md

---

# ⚡ DAX Highlights

The project uses DAX for:

### Calculated Columns

- Age Group
- Income Group
- Revenue
- Week Number

### Measures

- Current Week Revenue
- Previous Week Revenue

Key DAX functions include:

- CALCULATE()
- FILTER()
- SWITCH()
- SUM()
- WEEKNUM()
- MAX()
- ALL()

---

# 📌 Business Insights

Key findings from the dashboard include:

- Revenue increased **28.8% Week-over-Week**
- Transaction Amount increased **35%**
- Customer Count increased **12.8%**
- Blue & Silver Cards account for **93.5%** of all transactions.
- Texas, New York, and California contribute **68.8%** of total revenue.
- High-income customers generate the highest revenue.
- Customers aged **40–50 years** are the most profitable customer segment.
- Swipe remains the dominant transaction method.

For detailed analysis:

📄 Documentation/05_Business_Insights.md

---

# 🚀 Business Recommendations

Based on dashboard findings:

- Expand Premium Card Adoption
- Target High-Value Customers
- Increase Customer Activation
- Promote Digital Payments
- Reduce Delinquency Risk
- Strengthen Regional Marketing
- Improve Customer Retention
- Enhance Executive KPI Monitoring

More details:

📄 Documentation/06_Business_Recommendations.md

---

# 📁 Repository Structure

```
Credit-Card-Financial-Dashboard-PowerBI/
│
├── Dashboard/
│   ├── Credit Card Financial Dashboard.pbix
│   └── Dashboard.pdf
│
├── Dataset/
│   ├── customer.csv
│   ├── credit_card.csv
│   └── Data_Dictionary.md
│
├── Reports/
│   ├── Customer_Report.png
│   ├── Transaction_Report.png
│   └── Architecture.png
│
├── Documentation/
│   ├── 01_Business_Requirements.md
│   ├── 02_Data_Model.md
│   ├── 03_DAX_Measures.md
│   ├── 04_Dashboard_Design.md
│   ├── 05_Business_Insights.md
│   ├── 06_Business_Recommendations.md
│   └── 07_Lessons_Learned.md
│
├── LICENSE
└── README.md
```

---

# ▶️ How to Use

1. Clone this repository.
2. Open the `.pbix` file using **Microsoft Power BI Desktop**.
3. Explore the interactive dashboard.
4. Review the documentation for implementation details and business insights.

---

# 📚 Documentation

| Document | Description |
|----------|-------------|
| Business Requirements | Defines project objectives and analytical requirements |
| Data Model | Explains relationships and schema design |
| DAX Measures | Documents calculated columns and measures |
| Dashboard Design | Explains layout and visualization choices |
| Business Insights | Summarizes key findings |
| Business Recommendations | Provides strategic recommendations |
| Lessons Learned | Reflects on project learnings and future enhancements |

---

# 🔮 Future Enhancements

Potential improvements include:

- Calendar Table
- Year-over-Year Analysis
- Month-over-Month Analysis
- Drill-through Reports
- Dynamic Report Titles
- Custom Tooltips
- Row-Level Security (RLS)
- Bookmarks & Navigation
- Field Parameters
- Incremental Refresh

---

# 👨‍💻 Author

**Aayush Agarwal**

Aspiring Data Analyst | SQL | Python | Power BI

If you found this project interesting, feel free to ⭐ this repository.

---

# 📜 License

This project is licensed under the MIT License.
