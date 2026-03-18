# Customer_credit_analysis
##### *Customer Credit Behavior &amp; Business Insights Analysis*
## Overview

This project analyzes customer credit behavior to identify patterns associated with default risk and generate business insights for decision-making. Using a dataset of credit card clients, the analysis focuses on understanding how financial variables such as credit limit, payment behavior, and past delays influence the likelihood of default.

## Dataset
#### UC Irvine Repository: Default of Credit Card Clients
The dataset used in this project contains information on credit card clients, including demographic characteristics, credit limits, billing amounts, payment history, and default status.

The target variable is a binary indicator:
 **default payment next month**

1 = Default

0 = No default

The dataset includes 30000 instances and 23 explanatory variables, which capture customer financial behavior and credit activity over time.

#### Key Variables
**Customer Profile**

* LIMIT_BAL (X1): Amount of granted credit (includes individual and supplementary/family credit)

* SEX (X2): Gender (1 = male, 2 = female)

* EDUCATION (X3): Education level

* MARRIAGE (X4): Marital status

* AGE (X5): Age of the customer

**Payment History**

* PAY_0 – PAY_6 (X6–X11): Monthly repayment status (April–September 2005)

Payment status encoding:

* -1: Payment made on time

* 1–9: Delay in payment (number of months delayed)

These variables are critical for identifying patterns of financial distress and credit risk.

**Billing Amounts**

* BILL_AMT1 – BILL_AMT6 (X12–X17): Monthly bill statements over the last 6 months

These represent the customer’s outstanding balance over time.

**Payment Amounts**

* PAY_AMT1 – PAY_AMT6 (X18–X23): Payments made in the last 6 months

These variables reflect the customer’s actual repayment behavior.




#### Reference
Yeh, I. (2009). Default of Credit Card Clients [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C55S3H.

## Data Cleaning
Removed irrelevant columns and corrected column names for better readability and analysis.
Checked for missing values and verified that the dataset did not contain significant null data affecting the analysis.
Determination of outliers (in this case they are not eliminated since the behavior corresponds to the normal range)

## Feature Engineering
To better capture customer behavior, new variables were created:

To enhance the analysis, additional variables were created:

* TOTAL_BILL: Total outstanding balance across all months
* TOTAL_PAY: Total payments made
* DEBT_RATIO: Ratio of total debt to credit limit
* %_RATIO_PAID: Proportion of debt paid
* AVG_BILL: Average monthly bill amount.
* MAX_DEL_PAY: Maximum delay recorded across all months.

Converted raw variables into meaningful analytical features.

Created categorical segments (e.g., credit limit, payment behavior, and debt utilization) to facilitate business-oriented analysis.

Prepared the dataset for visualization and behavioral analysis.
