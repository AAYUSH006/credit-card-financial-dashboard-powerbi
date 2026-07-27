# Data Dictionary

## Overview

This project uses two datasets to analyze credit card customer behavior and financial performance.

- **credit_card.csv** – Contains transaction-level and financial information related to customers' credit card usage.
- **customer.csv** – Contains customer demographic, socioeconomic, and profile information.

The two datasets are linked using the **Client_Num** field, which serves as the unique customer identifier.

---

# Dataset 1: credit_card.csv

**Description:**  
This dataset contains financial and transactional information for each credit card customer, including revenue, transaction activity, spending behavior, and credit utilization.

| Column Name | Data Type | Description | Example |
|------------|-----------|-------------|---------|
| Client_Num | Integer | Unique identifier assigned to each customer. Used as the primary key for joining datasets. | 708082083 |
| Card_Category | Text | Type of credit card issued to the customer. | Blue |
| Annual_Fees | Integer | Annual fee charged for the credit card. | 200 |
| Activation_30_Days | Boolean (0/1) | Indicates whether the customer activated the card within 30 days of issuance. | 0 |
| Customer_Acq_Cost | Integer | Cost incurred by the bank to acquire the customer. | 87 |
| Week_Start_Date | Date | Start date of the reporting week. | 01-01-2023 |
| Week_Num | Text | Reporting week identifier. | Week-1 |
| Qtr | Text | Financial quarter corresponding to the transaction period. | Q1 |
| current_year | Integer | Reporting year. | 2023 |
| Credit_Limit | Decimal | Maximum credit limit assigned to the customer. | 3544 |
| Total_Revolving_Bal | Decimal | Outstanding revolving balance carried by the customer. | 1661 |
| Total_Trans_Amt | Decimal | Total monetary value of all credit card transactions. | 15149 |
| Total_Trans_Vol | Integer | Total number of transactions performed. | 111 |
| Avg_Utilization_Ratio | Decimal | Ratio of credit utilized against the available credit limit. | 0.469 |
| Use Chip | Text | Mode used to complete the transaction. | Chip |
| Exp Type | Text | Customer spending category or expenditure type. | Travel |
| Interest_Earned | Decimal | Interest revenue generated from the customer. | 4393.21 |
| Delinquent_Acc | Boolean (0/1) | Indicates whether the customer has a delinquent account. | 0 |

---

# Dataset 2: customer.csv

**Description:**  
This dataset contains demographic, financial, and customer profile information used for customer segmentation and behavioral analysis.

| Column Name | Data Type | Description | Example |
|------------|-----------|-------------|---------|
| Client_Num | Integer | Unique customer identifier. Used to join with the transaction dataset. | 708082083 |
| Customer_Age | Integer | Age of the customer in years. | 24 |
| Gender | Text | Gender of the customer. | F |
| Dependent_Count | Integer | Number of dependents associated with the customer. | 1 |
| Education_Level | Text | Highest education level attained by the customer. | Uneducated |
| Marital_Status | Text | Current marital status of the customer. | Single |
| state_cd | Text | State code representing the customer's residence. | FL |
| Zipcode | Integer | Postal ZIP code of the customer's residence. | 91750 |
| Car_Owner | Boolean (Yes/No) | Indicates whether the customer owns a car. | No |
| House_Owner | Boolean (Yes/No) | Indicates whether the customer owns a house. | Yes |
| Personal_loan | Boolean (Yes/No) | Indicates whether the customer currently has a personal loan. | No |
| contact | Text | Customer's preferred contact channel. | Unknown |
| Customer_Job | Text | Occupation of the customer. | Businessman |
| Income | Decimal | Annual income of the customer. | 202326 |
| Cust_Satisfaction_Score | Integer | Customer satisfaction rating assigned by the bank. | 3 |

---

# Data Relationship

The datasets are related using the **Client_Num** field.

| Parent Table | Child Table | Relationship | Cardinality |
|--------------|------------|--------------|-------------|
| customer.csv | credit_card.csv | Client_Num | One-to-Many* |

> **Note:** In this project, each transaction record is associated with a customer through the `Client_Num` field. This relationship enables demographic analysis alongside financial and transaction metrics.

---

# Key Business Metrics Available

The datasets support analysis of several important business KPIs, including:

- Total Revenue
- Total Transaction Amount
- Total Transaction Volume
- Interest Earned
- Customer Acquisition Cost (CAC)
- Average Credit Utilization
- Customer Satisfaction Score (CSS)
- Annual Fees
- Income Distribution
- Revenue by Card Category
- Revenue by Customer Segment
- Revenue by Expenditure Type
- Revenue by Transaction Mode
- Quarterly Revenue Trends

---

# Data Usage

These datasets are used to build an interactive Power BI dashboard that enables:

- Customer segmentation analysis
- Revenue performance monitoring
- Credit card usage analysis
- Transaction trend analysis
- Spending behavior analysis
- Credit utilization monitoring
- Customer profitability analysis
- Executive-level financial reporting


## Data Model

The dashboard follows a Star Schema data model where:

- customer.csv acts as the Customer Dimension.
- credit_card.csv acts as the Fact Table.
- The relationship is established using Client_Num.

Refer to **Documentation/Data_Model.md** for the complete schema and relationship diagram.
