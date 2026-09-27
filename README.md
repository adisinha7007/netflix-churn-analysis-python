# netflix-churn-analysis-python
Python-based Netflix customer churn analysis using pandas, exploratory data analysis, segmentation, and data-driven insights to identify factors associated with customer churn.

# Netflix Customer Churn Analysis — Python

## Project Overview

This project analyzes customer churn using Python and exploratory data analysis (EDA).

The dataset was obtained from Kaggle and contains **5,000 customer records and 14 columns**. The objective of the analysis was to understand which customer characteristics and behavioral patterns are associated with churn and identify areas that could be investigated further.

## Business Questions

The analysis focuses on three questions:

1. What customer characteristics and behavioral patterns are associated with churn?
2. Which customer segments show different observed churn rates?
3. Which patterns should be investigated further to understand potential churn drivers?

## Dataset

The dataset contains customer-level information such as:

* Age
* Subscription type
* Watch hours
* Days since last login
* Region
* Monthly fee
* Payment method
* Number of profiles
* Device
* Favorite genre
* Gender
* Churn status

The dataset contains **no missing values**, and the columns have appropriate data types for analysis.

The dataset was sourced from **Kaggle**.

## Analysis Approach

The analysis was performed in the following stages:

### 1. Initial Data Exploration

I first examined the overall distribution of churned and non-churned customers.

The dataset contained almost equal numbers of churned and non-churned customers.

### 2. Customer Distribution Analysis

I systematically inspected churn across different customer attributes, including:

* Subscription type
* Age
* Gender
* Region
* Device
* Payment method
* Number of profiles
* Favorite genre

### 3. Feature Grouping

To make behavioral patterns easier to compare across customer segments, I created groups for selected numerical variables.

* **Watch hours:** grouped using quartiles
* **Last login days:** grouped into login-recency segments

These groups were then used to compare observed churn rates across different customer segments.

### 4. Churn Analysis

The analysis included:

* Churn by subscription type
* Churn by watch-hour group
* Churn by subscription type and watch-hour group
* Churn by login-recency group
* Churn by subscription type and login-recency group
* Churn by region and login-recency group
* Churn by age group and subscription type
* Churn by payment method
* Churn by number of profiles
* Churn by device
* Churn by favorite genre
* Churn by gender

Cross-tabulation was used to examine how churn patterns changed across combinations of customer characteristics.

## Key Findings

### Stronger Observed Differences

**Login Recency**

Customers in the **At-risk** login group showed substantially higher observed churn than more active customers. This pattern was also visible across different regions.

**Watch Hours**

Higher watch-hour groups showed lower observed churn rates. The pattern was consistent across subscription types.

**Number of Profiles**

Customers with **4–5 profiles** showed lower observed churn than customers with 1–3 profiles.

**Payment Method**

Customers using **Crypto and Gift Cards** showed somewhat higher observed churn compared with some other payment methods.

**Subscription Type**

Basic subscription customers showed higher observed churn than Premium and Standard customers in the overall comparison.

### Weaker Observed Differences

The following variables showed relatively smaller differences in observed churn rates:

* Device
* Gender
* Region
* Age
* Favorite genre

These variables did not show the same magnitude of difference as login recency or watch-hour groups in this dataset.

## Visualizations

The notebook contains visualizations throughout the analysis to compare churn rates across customer segments and highlight the main behavioral patterns.

## Limitations

* This is a **descriptive EDA project**, so the analysis identifies associations and observed patterns rather than causation.
* No statistical significance tests were performed.
* No predictive model was developed.
* The findings are based on the available dataset and may not generalize to the broader Netflix customer population.
* Observed differences should not be interpreted as evidence that changing a particular customer characteristic would directly cause churn to increase or decrease.

## Conclusion

The analysis found that **login recency and watch-hour groups showed the strongest observed differences in churn**.

These patterns could be investigated further to understand whether changes in customer engagement and login behavior can help identify customers who may be at higher risk of churn.

Further analysis could include statistical testing and predictive modeling to determine whether these variables provide useful predictive signals for customer churn.

## Tools & Techniques

* Python
* Pandas
* Matplotlib / Seaborn
* Jupyter Notebook
* Exploratory Data Analysis (EDA)
* Data quality checks
* Feature grouping / binning
* Cross-tabulation
* Customer segmentation
* Churn-rate analysis

## Project Files

* `Netflix_churn_analysis.ipynb` — Jupyter Notebook containing the complete analysis and visualizations
* `netflix_customer_churn.csv` — Dataset used for the analysis

## Data Source

Dataset sourced from Kaggle.

> **Note:** This project is for analytical and learning purposes. The findings represent patterns observed in the provided dataset and should not be interpreted as causal conclusions.
