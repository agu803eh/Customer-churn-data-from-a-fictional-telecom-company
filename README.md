Customer Churn Analysis: Fictional Telecom Company
Project Overview
This project focuses on analyzing customer churn data from a fictional telecom company in California. The dataset comprises detailed information on 7,043 customers, covering demographics, location, service subscriptions, billing details, and their churn status. The primary objective is to understand the drivers behind customer churn and provide actionable recommendations to improve customer retention.

Problem Statement
The core business problem addressed is the high rate of customer attrition. The analysis aims to answer critical questions:

How many customers joined recently, and how many have churned?
What are the distinguishing characteristics of churned, stayed, and newly joined customers?
What are the key factors and patterns most strongly associated with customer churn?
Is the company losing its high-value customers, and if so, why?
Analysis Approach
The analysis was conducted in several systematic steps:

Initial Data Exploration: Loaded the /content/telecom_customer_churn.csv dataset into a pandas DataFrame, examining its structure, data types, column names, and identifying missing values.
Customer Cohort Analysis: Quantified the number of customers who joined in the last quarter (tenure <= 3 months) and the total number of churned customers.
Customer Characteristics Analysis: Investigated the demographics, subscribed services, and billing details for customers who have churned, stayed, and recently joined. This involved comparing numerical statistics and categorical value counts across these groups.
Churn Driver Identification: Analyzed the 'Churn Category' and 'Churn Reason' columns for churned customers to identify the most frequent causes of departure.
High-Value Customer Churn Analysis: Defined 'high-value' customers based on the 75th percentile of 'Total Revenue'. Subsequently, analyzed the churn rate and specific reasons for churn among this critical customer segment.
Key Insights Visualization: Generated various visualizations (count plots, histograms) to illustrate the distribution of customer statuses, top churn categories and reasons, tenure comparisons, and contract type preferences across different customer groups.
Key Findings
Overall Churn: A total of 1869 customers have churned from the company, while 1051 customers joined in the last quarter.
Churn Drivers: The leading reasons for churn are predominantly related to competition (e.g., better devices, better offers, more data/speed) and customer dissatisfaction (e.g., attitude of support person, product/service dissatisfaction).
Contract Type: Customers on 'Month-to-Month' contracts are significantly more likely to churn (1655 out of 1869 churners) compared to those with longer-term contracts. Similarly, 1003 out of 1051 recently joined customers are also on 'Month-to-Month' contracts.
Tenure: Churned customers have a markedly shorter average tenure (approx. 18 months) compared to stayed customers (approx. 41 months).
High-Value Customer Churn: 261 high-value customers (defined as those with 'Total Revenue' above $4801.15) have churned. Their churn reasons mirror the overall trends, with competitor offers and customer service issues being prominent.
Data Anomalies: Noticed anomalous negative values in 'Monthly Charge' (-10.0, -1.0) which warrant further investigation.
Recommendations & Actions
Retention for 'Month-to-Month' Customers: Implement targeted loyalty programs, attractive long-term contract options, or exclusive benefits to incentivize 'Month-to-Month' customers, especially new ones, to commit to longer contracts.
Competitive Strategy Enhancement: Actively monitor competitor offerings (device quality, data plans, pricing) and adjust company strategies to remain competitive. Consider improving device upgrade programs or introducing more appealing bundles.
Customer Service Improvement: Invest in comprehensive training for customer support staff, focusing on soft skills and effective problem resolution. Establish feedback loops to continuously improve the quality of customer interactions.
Investigate 'Monthly Charge' Anomalies: Address the negative values in the 'Monthly Charge' column to ensure data accuracy and prevent potential misinterpretations in financial analysis.
Challenges Faced
Missing Data: Significant missing values in 'Offer', 'Churn Category', and 'Churn Reason' columns limited the depth of analysis for certain attributes.
Data Anomalies: Negative 'Monthly Charge' values required noting, as their underlying cause was not immediately apparent and could affect calculations.
API Usage: Minor SyntaxError and FutureWarning from seaborn library regarding palette without hue were resolved during execution.
