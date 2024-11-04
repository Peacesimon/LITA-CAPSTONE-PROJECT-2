# LITA-CAPSTONE-PROJECT-2

## Project Overview
This project involves analyzing customer data to gain insights and inform business decisions. The dataset includes the following fields:

- CustomerID
- Customer Name
- Region 
- Subscription Type
- Subscription Start
- Subscription End
- Canceled (boolean)
- Revenue

## Objectives
The key objectives for this analysis are:

1. Understand the distribution and trends of customer subscriptions by region, type, and duration.
2. Identify any patterns or factors that contribute to customer churn (canceled subscriptions).
3. Analyze the relationship between subscription details and revenue generated.
4. Provide recommendations to the business based on the insights uncovered.

## Data Collection
The customer data was provided in a CSV file. The file was imported into a Pandas DataFrame for analysis. Some key steps in the data collection process include:

- Ensuring all necessary fields were present and had the appropriate data types.
- Checking for any missing values and determining how to handle them.
- Verifying the data quality and consistency, looking for any obvious errors or irregularities.

## Exploratory Data Analysis

### Customer and Subscription Breakdown
* Analyzed the distribution of customers by region, showing the top regions by number of customers.
* Looked at the breakdown of subscription types, including the percentage of customers on each type.
* Calculated the average subscription duration and identified the longest and shortest subscriptions.

### Churn Analysis
* Determined the overall churn rate by calculating the percentage of canceled subscriptions.
* Investigated whether there were any correlations between churn and factors like region, subscription type, or subscription duration.
* Identified the regions and subscription types with the highest churn rates.

### Revenue Analysis
* Summed the total revenue across all customers.
* Calculated the average revenue per customer and per subscription.
* Examined the relationship between subscription details (type, duration) and revenue generated.

### Key Findings
* The West region had the highest number of customers, but also the highest churn rate.
* Monthly subscriptions had a much higher churn rate compared to annual subscriptions.
* Customers with longer subscription durations tended to generate more revenue.

## Recommendations
Based on the insights gathered, some key recommendations include:

1. Investigate ways to reduce churn in the West region and for monthly subscriptions, such as offering incentives for longer commitments.
2. Explore opportunities to convert more customers to annual subscriptions, as these appear to be more profitable.
3. Consider targeted marketing or retention efforts for customers approaching the end of their subscription term.
4. Further analyze the factors driving higher-value customers to inform acquisition and upselling strategies.
