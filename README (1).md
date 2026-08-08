# Financial Loan Analytics & Risk Analysis

## Project Overview

This project analyzes a financial loan dataset to understand loan portfolio performance, funding, repayments, and credit risk.

The analysis was performed using Python and focuses on key financial KPIs, Good Loan vs. Bad Loan performance, and lending patterns across different customer and loan characteristics.

## Objectives

- Calculate total and Month-to-Date (MTD) loan applications.
- Calculate total and MTD funded amounts.
- Calculate total and MTD amount received from borrowers.
- Calculate average interest rate and average Debt-to-Income (DTI) ratio.
- Analyze Good Loans and Bad Loans.
- Compare loan performance across different dimensions.
- Identify lending trends using visualizations.

## Key Performance Indicators

### General Loan KPIs

- Total Loan Applications
- MTD Loan Applications
- Total Funded Amount
- MTD Total Funded Amount
- Total Amount Received
- MTD Total Amount Received
- Average Interest Rate
- Average DTI

### Good Loan KPIs

A Good Loan is defined as a loan where `loan_status = "Fully Paid"`.

- Good Loan Applications
- Good Loan Application Percentage
- Good Loan Funded Amount
- Good Loan Total Received Amount

### Bad Loan KPIs

A Bad Loan is defined as a loan where `loan_status = "Charged Off"`.

- Bad Loan Applications
- Bad Loan Application Percentage
- Bad Loan Funded Amount
- Bad Loan Total Received Amount

## Dataset

The dataset contains 38,576 loan records and 24 columns.

Important columns include:

| Column | Description |
|---|---|
| `id` | Loan/application identifier |
| `address_state` | Borrower's state |
| `application_type` | Type of loan application |
| `emp_length` | Employment length |
| `emp_title` | Employment title |
| `grade` | Loan grade |
| `home_ownership` | Home ownership status |
| `issue_date` | Loan issue date |
| `loan_status` | Loan status |
| `purpose` | Purpose of the loan |
| `sub_grade` | Loan sub-grade |
| `term` | Loan repayment term |
| `verification_status` | Verification status |
| `annual_income` | Annual income |
| `dti` | Debt-to-Income ratio |
| `installment` | Loan installment |
| `int_rate` | Interest rate |
| `loan_amount` | Funded/disbursed loan amount |
| `total_acc` | Total credit accounts |
| `total_payment` | Total amount received/payment |

## Analysis Performed

### Loan Applications
Total unique loan applications were calculated using the `id` column. MTD applications were calculated using the latest available month from `issue_date`.

### Funded Amount
The total amount disbursed was calculated using `loan_amount`.

### Amount Received
The total amount received from borrowers was calculated using `total_payment`.

### Average Interest Rate
The average value of `int_rate` was calculated to understand the overall lending cost.

### Average DTI
The average value of `dti` was calculated to understand borrower debt burden.

### Good Loan Analysis
Loans with `loan_status = "Fully Paid"` were analyzed for application count, percentage, funded amount, and amount received.

### Bad Loan Analysis
Loans with `loan_status = "Charged Off"` were analyzed for application count, percentage, funded amount, and amount received.

## Visual Analysis

The project includes analysis for:

- Monthly Trends
- Regional Analysis by State
- Loan Term
- Employee Length
- Loan Purpose
- Home Ownership

The three core metrics used across the Overview analysis are:

1. Total Loan Applications
2. Total Funded Amount
3. Total Amount Received

### Visualizations

- Line charts for monthly trends
- Bar charts for state and employment analysis
- Pie/Donut charts for loan term analysis
- Horizontal bar charts for loan purpose
- Heat maps for home ownership analysis

## Loan Purpose: Debt Consolidation

`debt_consolidation` is one of the loan purposes in the dataset. It represents loans taken to consolidate or repay existing debts.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Workflow

```text
Raw Loan Dataset
       ↓
Data Loading
       ↓
Data Type & Quality Check
       ↓
KPI Calculation
       ↓
Good Loan / Bad Loan Analysis
       ↓
Dimension-wise Analysis
       ↓
Data Visualization
       ↓
Financial & Risk Insights
```

## Example Python Setup

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_excel("financial_loan.xlsx")

print(df.shape)
print(df.dtypes)
print(df.head())
```

## Key Formulas

### Good Loan Percentage

```text
Good Loan Applications / Total Loan Applications × 100
```

### Bad Loan Percentage

```text
Bad Loan Applications / Total Loan Applications × 100
```

### Total Funded Amount

```python
df["loan_amount"].sum()
```

### Total Amount Received

```python
df["total_payment"].sum()
```

### Average Interest Rate

```python
df["int_rate"].mean()
```

### Average DTI

```python
df["dti"].mean()
```

## Project Structure

```text
Financial-Loan-Analytics/
│
├── README.md
├── financial_loan.xlsx
├── Financial_Loan_Analytics.ipynb
│
└── visuals/
    ├── monthly_trends.png
    ├── state_analysis.png
    ├── loan_term.png
    ├── employment_length.png
    ├── loan_purpose.png
    └── home_ownership_heatmap.png
```

## Conclusion

This project provides a structured view of a loan portfolio by combining financial KPIs, repayment performance, loan quality analysis, and customer/loan segmentation.

The analysis helps identify lending trends, understand Good vs. Bad Loan performance, and evaluate the portfolio across loan purpose, geography, employment length, loan term, and home ownership.

## Author

**Udith B. Nambiar**

Data Analytics Project
