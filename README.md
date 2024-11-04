# LITA-CAPSTONE-PROJECT-2 
---
## Project Title: Customer Data Analysis
---
### Introduction
This project used 

## Project Overview
---

### Data Collected
---
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
---
The key objectives for this analysis are:
1. Understand the distribution and trends of customer subscriptions by region, type, and duration.
2. Identify any patterns or factors that contribute to customer churn (canceled subscriptions).
3. Analyze the relationship between subscription details and revenue generated.
4. Provide recommendations to the business based on the insights uncovered.

### Tools Used
- Microsoft Excel [Download Here](https://www.microsoft.com)
  1. For Data Cleaning
  2. For Analysing
  3. For Visualization
     
- SQL- Structured Query Language for querying of data
- Power BI (for creating a report)
- GITHUB for portfolio Building

### Methodology
---
  1. Data Cleaning and preparation
  2. Exploratory Data Analysis
  3. Formula Used
  4. Visualization of Key Metrics
     
### Data Cleaning and Preparation
---
In the initial cleaning phase of the data cleaning and preparation, we perform the follwing actions;
 1. Data Loading and Inspection
 2. Data cleaning and removing of duplicate columns

## Exploratory Data Analysis
* Analyzed the distribution of customers by region, showing the top regions by number of customers.
* Looked at the breakdown of subscription types, including the percentage of customers on each type.
* Calculated the average subscription duration and identified the longest and shortest subscriptions.
* Determined the overall cancellation count by calculating the percentage of canceled subscriptions.
* Identified the regions and subscription types with the highest cancellation count
* Summed the total revenue across all customers.
* Calculated the average revenue per customer and per subscription.
* Examined the relationship between subscription details (type, duration) and revenue generated.


## SQL ( Querying the Data)
The folowing queries were used to answer the quetions raised in the Exploratory data Analysis
#### Total Number of customers from each Region

```SQL
SELECT Region, COUNT(CustomerID) AS TotalCustomers
FROM [dbo].[CustomerData$]
GROUP BY Region
```
#### Expected Result
![image](https://github.com/user-attachments/assets/add63e4c-2ca3-487c-82b2-74e1a1f05760)

### Most Popular subscription Type by Number of Customers
```SQL
SELECT TOP 1 (SubscriptionType), COUNT(CustomerID) AS NumberOfCustomers
FROM [dbo].[CustomerData$]
GROUP BY SubscriptionType
ORDER BY NumberOfCustomers DESC
```
#### Expected  Outcome
![image](https://github.com/user-attachments/assets/aae0b857-c7cd-4ae3-8208-42e1afb33c7e)

The result show Basic is the most popular subscription with 16,675 number of customers


### Customers who cancelled their subscription within 6 month
```SQL
SELECT CustomerID, CustomerName, SubscriptionStart, SubscriptionEnd,canceled
from CustomerData$
where canceled = 1
and datediff(month, subscriptionEnd,
SubscriptionStart) <= 6
```
#### Expected Result
![image](https://github.com/user-attachments/assets/cf70dd06-304d-4146-ade3-cee5e4f6948e)


### Average Subscription duration for all customers
```SQL
SELECT AVG (DATEDIFF(day, SubscriptionStart, SubscriptionEnd)) 
AS avg_subscription_duration
FROM CustomerData$
```
#### Expected Result
![image](https://github.com/user-attachments/assets/8ba52aa9-1941-4e1e-a095-a31814ce776b)

The avearge subscription for all customers is 365

### Total Revenue by Subscription Type
```SQL
SELECT SubscriptionType, sum (Revenue) as Total_Revenue
FROM [dbo].[CustomerData$]
GROUP BY Subscriptiontype
```
Expected Result
![image](https://github.com/user-attachments/assets/6bd38d52-041b-44a0-a960-df22c4968dc2)









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
