# Churn-Analysis-and-Customer-Intelligence
# 📊 Customer Churn Analysis using SQL & Python

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![SQL](https://img.shields.io/badge/SQL-SQLite-green?logo=sqlite)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-purple?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-blue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Visualization-4B8BBE)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio_Project-black?logo=github)

</p>

---

# 📌 Project Overview

Customer churn is one of the most important business metrics for subscription-based companies. Every customer who cancels a subscription represents not only lost revenue but also increased acquisition costs to replace that customer.

This project focuses on analyzing customer behavior, subscription details, and customer support interactions to understand why customers leave and identify opportunities to improve customer retention.

Using Python and SQLite, this project demonstrates an end-to-end analytics workflow that includes:

- Database integration
- Data cleaning
- Feature engineering
- Exploratory Data Analysis (EDA)
- Business KPI calculation
- Data visualization
- Actionable business recommendations

The project is designed to simulate a real-world business scenario where a Data Analyst transforms raw data into meaningful insights that support strategic decision-making.

---

# 🎯 Business Problem

Subscription-based businesses such as streaming platforms, SaaS companies, telecom providers, and online services rely heavily on customer retention.

A high churn rate can lead to:

- Reduced recurring revenue
- Increased customer acquisition costs
- Lower customer lifetime value (CLTV)
- Reduced profitability
- Slower business growth

The primary goal of this project is to analyze customer churn using historical customer, subscription, and support data to answer key business questions.

---

# ❓ Business Questions

This project answers several important business questions:

- What is the overall customer churn rate?
- Which subscription plans experience the highest churn?
- Which customer segments are most likely to churn?
- How much revenue is at risk due to customer churn?
- Do customer support escalations contribute to churn?
- Which regions have the highest churn?
- Which customers should be prioritized for retention campaigns?

---

# 🎯 Project Objectives

The objectives of this project are to:

- Import data from a relational SQLite database
- Perform data cleaning and preprocessing
- Handle missing values and inconsistent data
- Engineer new business features
- Merge multiple relational tables
- Calculate important business KPIs
- Perform exploratory data analysis
- Build informative visualizations
- Identify churn drivers
- Generate actionable business recommendations

---

# 💼 Business Use Case

Imagine you are working as a Data Analyst for an OTT streaming company.

The management team wants answers to questions such as:

- Why are customers cancelling subscriptions?
- Which plans generate the highest churn?
- Which customers are at the highest risk of leaving?
- How much recurring revenue is being lost?
- Which customers should be contacted first by the retention team?

Your responsibility is to analyze customer data and provide insights that help management reduce churn and improve customer retention.

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Programming Language | Python |
| Database | SQLite |
| Data Manipulation | Pandas |
| Numerical Computing | NumPy |
| Visualization | Matplotlib |
| Statistical Visualization | Seaborn |
| Development Environment | Jupyter Notebook |
| Version Control | Git |
| Repository Hosting | GitHub |

---

# 📂 Dataset Description

The project uses a relational SQLite database containing customer information distributed across three tables.

## 1️⃣ Customer Table (`db_customer`)

Contains demographic information about customers.

### Columns

- Customer ID
- Customer Name
- Country
- State
- Gender
- Date of Birth

---

## 2️⃣ Subscription Table (`db_subscription`)

Contains subscription details for every customer.

### Columns

- Subscription Start Date
- Subscription Type
- Renewal Date
- Plan Type
- Contract Type
- Cancellation Date
- Cancellation Reason
- Monthly Charges
- Customer Lifetime Value (CLTV)
- Churn Score

---

## 3️⃣ Support Table (`db_support`)

Contains customer support interactions.

### Columns

- Complaint Date
- Escalation Status
- Customer Satisfaction Score (CSAT)

---

# 🗄 Database Schema

The project integrates data from three relational tables using the **Customer ID** as the primary key.

```text
                 +------------------+
                 |   db_customer    |
                 +------------------+
                 | CustomerID (PK)  |
                 | Name             |
                 | Country          |
                 | State            |
                 | Gender           |
                 | DOB              |
                 +------------------+
                          |
                          |
                          |
                 CustomerID
                          |
                          ▼
                 +----------------------+
                 |  db_subscription     |
                 +----------------------+
                 | CustomerID (PK/FK)   |
                 | Plan Type            |
                 | Contract Type        |
                 | Monthly Charges      |
                 | CLTV                 |
                 | Churn Score          |
                 | Cancellation Date    |
                 +----------------------+
                          |
                          |
                          |
                 CustomerID
                          |
                          ▼
                 +------------------+
                 |   db_support     |
                 +------------------+
                 | CustomerID (FK)  |
                 | Complaint Date   |
                 | Escalations      |
                 | CSAT Score       |
                 +------------------+
```

---

# 🔄 Project Workflow

The project follows a structured end-to-end analytics pipeline.

```text
                 SQLite Database
                        │
                        ▼
              SQL Data Extraction
                        │
                        ▼
              Import into Python
                        │
                        ▼
                Data Cleaning
                        │
                        ▼
            Feature Engineering
                        │
                        ▼
          Merge Relational Tables
                        │
                        ▼
        Exploratory Data Analysis
                        │
                        ▼
          Business KPI Calculation
                        │
                        ▼
             Data Visualization
                        │
                        ▼
          Business Recommendations
```

---

# 📁 Repository Structure

```text
Customer-Churn-Analysis/
│
├── data/
│   ├── customer_churn.db
│   ├── exported_churn_data.csv
│   └── data_dictionary.md
│
├── notebooks/
│   └── Customer_Churn_Analysis.ipynb
│
├── sql/
│   └── database_queries.sql
│
├── src/
│   ├── cleaning.py
│   ├── feature_engineering.py
│   ├── analysis.py
│   ├── visualization.py
│   └── utils.py
│
├── images/
│
├── reports/
│   └── Business_Report.pdf
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# 📈 Project Highlights

✔ End-to-End Data Analytics Project

✔ SQL Database Integration

✔ Multi-Table Data Processing

✔ Data Cleaning & Preprocessing

✔ Feature Engineering

✔ Customer Churn Analysis

✔ Business KPI Development

✔ Exploratory Data Analysis (EDA)

✔ Professional Data Visualizations

✔ Business Intelligence & Decision Support

---

# 🧹 Data Cleaning & Preprocessing

Raw data often contains missing values, inconsistent formats, duplicate records, and incorrect data types. Before performing any analysis, the dataset was cleaned to ensure accuracy and consistency.

The project follows a systematic data preprocessing pipeline.

---

## Step 1: Column Renaming

To improve readability, ambiguous column names were renamed.

| Original Column | New Column |
|-----------------|------------|
| name | customer_name |

### Why?

- Makes the dataset easier to understand.
- Improves code readability.
- Follows standard naming conventions.

---

## Step 2: Remove Unnecessary Columns

The following columns were removed because they contained either irrelevant or unusable information.

### Customer Table

- interests
- pincode

### Support Table

- col_1
- comment

### Why?

- High percentage of missing values.
- No contribution to churn analysis.
- Reduces dataset complexity.

---

## Step 3: Convert Data Types

Date columns were converted from text to datetime format.

### Customer Table

- dob

### Subscription Table

- subscription_start_date
- renewal_date
- cancellation_date

### Support Table

- complaint_date

### Why?

This enables:

- Tenure calculation
- Monthly trend analysis
- Date filtering
- Time-based KPIs

---

## Step 4: Data Standardization

The gender column contained inconsistent values.

### Before

```
Male
Men
Female
Women
```

### After

```
Male
Female
```

### Why?

Standardization prevents duplicate categories during analysis and visualization.

---

## Step 5: Handle Missing Values

Missing values were identified and handled appropriately.

### Country

Missing country values were filled using the corresponding state information.

Example:

```
State → Country Mapping
```

### Why?

This preserves customer records without introducing unnecessary data loss.

---

## Step 6: Remove Duplicate Support Records

Some customers had multiple support interactions.

Instead of removing all duplicates, the project:

- Counted the total complaints per customer.
- Retained the most recent complaint record.
- Created a new feature called **Complaint Count**.

### Business Benefit

This approach preserves both:

- Latest customer interaction
- Total complaint history

which provides richer analytical insights.

---

# ⚡ Feature Engineering

Feature engineering transforms existing data into meaningful business attributes that improve analysis.

Several new features were created during the project.

---

## 1️⃣ Churn Flag

A customer is considered churned if the cancellation date exists.

### Logic

```
Cancellation Date exists

↓

Customer Churned

↓

Churn Flag = 1
```

Otherwise

```
Customer Active

↓

Churn Flag = 0
```

---

## 2️⃣ Complaint Count

Calculated by counting the number of complaints raised by each customer.

### Purpose

Instead of simply knowing whether a customer complained, this feature measures complaint frequency.

---

## 3️⃣ Customer Tenure

Customer tenure measures how long a customer remained subscribed.

### Formula

For churned customers

```
Cancellation Date
−
Subscription Start Date
```

For active customers

```
Today's Date
−
Subscription Start Date
```

### Business Importance

Long-tenure customers usually have:

- Higher loyalty
- Higher CLTV
- Lower acquisition cost

---

## 4️⃣ Churn Risk

Customers were classified into three risk categories using churn score.

| Churn Score | Risk |
|-------------|------|
| < 50 | Low |
| 50–69 | Medium |
| ≥ 70 | High |

### Why?

Business teams can prioritize retention campaigns based on customer risk.

---

## 5️⃣ Cancellation Month

Extracted from the cancellation date.

Used to analyze monthly churn trends.

---

# 📊 Exploratory Data Analysis (EDA)

After preprocessing, exploratory data analysis was performed to understand customer behavior.

The project focuses on answering key business questions using descriptive analytics.

---

## EDA Objectives

- Understand customer churn patterns
- Identify high-risk customers
- Measure revenue impact
- Analyze customer support behavior
- Compare subscription plans
- Discover churn trends over time

---

# 📈 Business KPIs

The project calculates several important business metrics.

---

## 1. Customer Churn Rate

Measures the percentage of customers who cancelled their subscriptions.

### Formula

```
(Number of Churned Customers
/
Total Customers)
×100
```

### Business Value

One of the most important metrics for subscription businesses.

---

## 2. Retention Rate

Measures the percentage of customers who remain active.

### Formula

```
100 − Churn Rate
```

---

## 3. Churn Rate by Plan Type

Calculates churn separately for:

- Basic
- Standard
- Premium

### Business Value

Helps identify which subscription plans need improvement.

---

## 4. Average Revenue Per User (ARPU)

Measures average monthly revenue generated per customer.

### Formula

```
Average(Monthly Charges)
```

### Business Importance

Used to evaluate customer profitability.

---

## 5. Average Customer Tenure

Measures average customer lifetime.

### Formula

```
Average(Tenure Days)
```

### Business Value

Longer tenure indicates stronger customer loyalty.

---

## 6. Revenue at Risk

Calculates monthly recurring revenue associated with churned customers.

### Formula

```
Sum(Monthly Charges)
Where Churn Flag = 1
```

### Business Importance

Estimates the revenue currently being lost due to churn.

---

## 7. Escalation Rate

Measures the proportion of customers whose complaints were escalated.

### Formula

```
Escalated Customers
/
Total Customers
×100
```

---

## 8. Average Complaints per Customer

Measures average complaint frequency.

### Formula

```
Total Complaints
/
Unique Customers
```

---

## 9. Correlation Between Escalations and Churn

Correlation analysis was performed to understand the relationship between customer support escalations and churn.

### Why?

If strong positive correlation exists,

Higher escalations

↓

Higher dissatisfaction

↓

Higher probability of churn

---

# 📊 Summary of KPIs

| KPI | Business Purpose |
|------|------------------|
| Churn Rate | Customer attrition |
| Retention Rate | Customer loyalty |
| Churn by Plan | Product performance |
| ARPU | Revenue generation |
| Average Tenure | Customer loyalty |
| Revenue at Risk | Financial impact |
| Escalation Rate | Support quality |
| Complaint Rate | Customer experience |
| Churn Risk | Customer prioritization |

---

# 📈 Key Metrics Generated

The project calculates:

- Overall Churn Rate
- Retention Rate
- Churn by Plan Type
- Average Revenue Per User (ARPU)
- Average Customer Tenure
- Revenue at Risk
- Escalation Rate
- Average Complaints per Customer
- Correlation between Escalations and Churn
- Customer Risk Segmentation

These metrics provide a comprehensive view of customer behavior, revenue impact, and operational performance, enabling data-driven decision-making.

---

# 📊 Data Visualizations

Visualization plays a vital role in identifying customer behavior patterns and communicating analytical findings to stakeholders. This project includes multiple visualizations to explore churn trends, subscription performance, customer support interactions, and feature relationships.

---

## 1️⃣ Monthly Churn Trend

### Objective

Analyze how customer churn changes over time.

### Visualization

> *<img width="817" height="331" alt="Screenshot 2026-08-01 193833" src="https://github.com/user-attachments/assets/66f49526-8f78-4fa6-a38f-f16bf7b55897" />
*


### Business Insight

- Identifies months with unusually high customer churn.
- Helps investigate external events such as pricing changes, marketing campaigns, or product issues.
- Supports proactive customer retention planning.

---

## 2️⃣ Churn Rate by Subscription Plan

### Objective

Compare churn rates across different subscription plans.

> *<img width="686" height="422" alt="Screenshot 2026-08-01 194048" src="https://github.com/user-attachments/assets/26155357-a582-42da-9de7-cd0c85e95c40" />
*


### Business Insight

- Highlights which subscription plans experience higher customer attrition.
- Enables the business to improve pricing strategies and product offerings.

---

## 3️⃣ Churn Rate by State

### Objective

Identify geographical regions with higher churn rates.

> *<img width="1153" height="465" alt="Screenshot 2026-08-01 194246" src="https://github.com/user-attachments/assets/a716be60-216c-4265-9b8b-7c5106e6ebaf" />
*


### Business Insight

- Detects high-risk regions.
- Supports region-specific marketing and customer engagement strategies.

---

## 4️⃣ Correlation Heatmap

### Objective

Understand relationships between important business variables.

> *<img width="677" height="567" alt="Screenshot 2026-08-01 194401" src="https://github.com/user-attachments/assets/a667f76f-2681-4b58-a203-c0edb4105784" />
*


### Variables Included

- Plan Type
- Contract Type
- Churn Score
- Churn Flag
- Escalations
- Churn Risk

### Business Insight

The heatmap helps identify variables that are strongly associated with customer churn.

---

## 5️⃣ Pair Plot

### Objective

Visualize pairwise relationships between numerical variables.

> *<img width="543" height="521" alt="Screenshot 2026-08-01 194641" src="https://github.com/user-attachments/assets/c251def1-9918-45f5-9926-7dce966489b3" />
*


### Business Insight

Useful for identifying trends, clusters, and relationships among customer metrics.

---

## 6️⃣ Facet Plot (Catplot)

### Objective

Compare monthly charges across different plan types, genders, and churn risk levels.

> *<img width="1212" height="401" alt="Screenshot 2026-08-01 194752" src="https://github.com/user-attachments/assets/a037b050-3d65-4133-8ba9-b2aa996f72d4" />
*


### Business Insight

Provides a multi-dimensional comparison of customer characteristics and subscription behavior.

---

# 📈 Project Results

The analysis produced several business KPIs and customer behavior insights.

## Key Metrics

| Metric | Value |
|---------|-------|
| Overall Churn Rate | 28.57% |
| Retention Rate | 71.43% |
| Average Revenue Per User (ARPU) | 18.85 |
| Average Customer Tenure | 1452 Days |
| Revenue at Risk | 73.94 |
| Escalation Rate | 19.05% |
| Average Complaints per Customer | 0.43 |
| Escalation vs Churn Correlation | 0.77 |

---

# 💡 Business Insights

### 📌 Overall Customer Churn
- Overall Churn Rate: **28.6%**
- Customer Retention Rate: **71.4%**
- Nearly one in three customers has cancelled their subscription, indicating opportunities to improve customer retention.

---

### 📌 Subscription Plan Analysis
- The **Basic** subscription plan contributes the highest number of churned customers.
- Since Basic is the lowest-priced plan, the immediate revenue impact is relatively limited.
- However, reducing churn in this segment can improve customer acquisition efficiency and create opportunities to upgrade customers to higher-value plans.

---

### 📌 Regional Analysis
- Karnataka recorded the highest customer churn.
- This may indicate region-specific issues such as service quality, pricing, customer support, or stronger local competition.

---

### 📌 Monthly Churn Trend
- Customer churn peaked during **September 2024**.
- This suggests that an event during that period (pricing change, product issue, marketing campaign, or competitor activity) may have influenced customer cancellations.

---

### 📌 Revenue Analysis
- Total Revenue: **₹395**
- Revenue Lost Due to Churn: **₹74**
- Revenue Loss Percentage: **18%**
- Customer Lifetime Value Lost: **₹2,047**

Although most churn comes from Basic plan subscribers, reducing churn remains important to protect long-term revenue.

---

### 📌 Contract Analysis
- Monthly Contract Churn: **55.6%**
- Annual Contract Churn: **8.3%**

Customers on monthly contracts are significantly more likely to churn than customers with annual subscriptions.

---

### 📌 Customer Risk Analysis
Customers classified as **High** and **Medium** churn risk should be prioritized for retention campaigns.

Priority should be based on:
- Customer Lifetime Value (CLTV)
- Complaint history
- Escalation frequency
- Subscription plan
### Business Impact

Monitoring complaint frequency can help identify at-risk customers before cancellation.

---

# 📌 Business Recommendations

- Investigate the high churn observed in Karnataka to identify regional service, pricing, or support issues.
- Review the Basic subscription plan to determine whether pricing or feature changes contributed to customer cancellations.
- Analyze the September 2024 churn spike by examining product updates, marketing campaigns, and service incidents.
- Monitor competitor offerings, as cancellation data indicates that at least one customer switched to a competitor.
- Prioritize High and Medium churn-risk customers based on CLTV, complaint history, and escalation frequency.
- Use personalized retention strategies such as emails, SMS campaigns, support follow-ups, loyalty rewards, and targeted discounts.
- Encourage customers to switch from monthly to annual subscription plans to improve retention.

---


# 🎯 Skills Demonstrated

This project demonstrates practical experience in:

- SQL Database Integration
- Python Programming
- Data Cleaning
- Data Wrangling
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Customer Churn Analysis
- Business KPI Development
- Data Visualization
- Business Intelligence
- Customer Segmentation
- Business Storytelling
- Analytical Problem Solving

---


# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

If you have ideas to enhance this project, feel free to fork the repository and submit a pull request.


---

# ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

It motivates me to continue building and sharing data analytics projects.

---

## 📬 Contact

If you'd like to discuss this project, data analytics, or collaboration opportunities, feel free to connect with me on LinkedIn or GitHub.
