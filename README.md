# SpicyFood🍜: Exploring Customer Segmentation with a Tableau Dashboard

<img width="1438" height="768" alt="Dashboard" src="https://github.com/user-attachments/assets/733766bb-50db-40db-8622-d2ee0ed565f6" />

## Table of Contents
- [Background](#background)
- [Project Objective](#project-objective)
- [Data Collection](#data-collection)
- [Live Tableau Dashboard](#live-tableau-dashboard)
- [Business Metrics Overview](#business-metrics-overview)
- [Summary of Insights](#summary-of-insights)
- [Recommended Retention Strategies](#recommended-retention-strategies)
- [MySQL](#mysql)

## Background
SpicyFood, a fictional FoodTech company, aims to strengthen its customer engagement and retention strategies by gaining a deeper understanding of customer behavior. With a growing user base and increasing competition, identifying high-value customers and tailoring marketing efforts accordingly has become a key business priority.

To support this goal, a Customer Segmentation Dashboard was developed using Tableau, applying RFM (Recency, Frequency, Monetary) analysis to derive actionable insights from customer purchase data.

Let’s first take a look at what Recency, Frequency, and Monetary are:
- **(Recency) R** — How recent was the last purchase of a customer?
- **(Frequency) F** — How often does a customer make a transaction?
- **(Monetary) M** — How much money does a customer spend on a purchase?

## Project Objective
The objective of this project is to segment customers based on their purchasing patterns using RFM analysis, enabling SpicyFood to:
- Identify and retain valuable customers
- Personalize marketing campaigns
- Reduce customer churn
- Optimize marketing spend
- Improve overall customer lifetime value (CLV)

This segmentation helps categorize customers into groups, such as Champions, Loyal Customers, At-Risk, and others, providing clear direction for strategic business decisions.

## Data Collection
The dataset includes essential details like Customer ID, Purchase Frequency, Bill Amount, Recency, and other relevant attributes.

The dataset used for this analysis includes the following fields:

- **Customer ID:** Unique identifier for each customer.
- **Purchase Frequency:** The number of purchases a customer makes.
- **Bill Amount:** Total monetary value spent by the customer.
- **Recent Purchase Date:** The customer’s latest purchase date.
- **Rank_Recency:** Ranking based on the recency of purchases.
- **Rank_Frequency:** Ranking based on purchase frequency.
- **Rank_Spending:** Ranking based on the total spending amount.
- **Average of Rank:** Average rank across recency, frequency, and spending.
- **Overall Rank:** Combined rank for RFM segmentation.
- **Customer Tiers:** Segmented customer groups based on RFM scores.
- **Gender:** Gender of the customer.
- **Age:** Age of the customer.

## Live Tableau Dashboard
The final Tableau dashboard provides an interactive and visually compelling representation of key insights, enabling SpicyFood management to:
- Identify and target high-value customers.
- Re-engage at-risk customers to minimize churn.
- Strengthen retention strategies for long-term customer loyalty.
- Optimize marketing campaigns for better engagement and ROI.

[Link to the live Tableau dashboard](https://public.tableau.com/views/Kshitija_SpicyFood_Dashboard1_6/Dashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Business Metrics Overview

<img width="1258" height="102" alt="image" src="https://github.com/user-attachments/assets/8c2d5305-73e4-41af-a2b2-85d58d192e2e" />

- **Total Unique Number of Customers:** 35
- **Total Revenue:** Customers have made purchases totaling Rs. 179,500.
- **Total Orders:** The total number of orders placed is 107.
- **Unique Customer Base:** SpicyFood serves 35 unique customers, highlighting its niche market.
- **Average Purchase Value:** On average, each customer spends Rs. 5,129 per transaction.

## Summary of Insights

### 1️⃣ Customer Segmentation Breakdown

<img width="757" height="292" alt="image" src="https://github.com/user-attachments/assets/b7e5ce7c-35ff-4a3c-8011-eba56ca40411" />

As we already know, customers are segmented into five different categories: **Champions, Loyal Customers, Potential Loyalists, Promising, and At Risk.**

#### 1. Customer Tier: Champions

<img width="540" height="278" alt="image" src="https://github.com/user-attachments/assets/5006c5a8-0cba-4809-aed5-7b86eef4413f" />

- These customers make up 22% of the customer base and contribute to the majority of revenue.

- They are frequent buyers with high spending and recent purchases, making them ideal for loyalty programs or exclusive offers.

#### 2. Customer Tier: Loyal Customers

<img width="732" height="311" alt="image" src="https://github.com/user-attachments/assets/ac83ef8f-fa06-4ec7-ba31-7bd91573d1ed" />

- This group consistently makes repeat purchases and represents a significant portion of long-term revenue.
- Retaining them through rewards or early access to products can strengthen their loyalty even further.

#### 3. Customer Tier: Potential Loyalist

<img width="692" height="342" alt="image" src="https://github.com/user-attachments/assets/50d60f50-746a-4290-9fc7-1d1a8e1e77b3" />

- Customers in this group show high potential to become Champions.
- Strategies such as personalized marketing or small incentives (e.g., free shipping or discounts) could encourage them to purchase more frequently.

#### 4. Customer Tier: Promising

<img width="657" height="322" alt="image" src="https://github.com/user-attachments/assets/f0ceaf85-ec33-4f73-846f-5d6d8ef0bbff" />

- These are new or occasional buyers with medium spending levels.
- Engaging them through follow-ups, product recommendations, or introductory offers can drive higher retention.

#### 5. Customer Tier: At Risk

<img width="573" height="260" alt="image" src="https://github.com/user-attachments/assets/c8ffab17-3530-4df8-a57d-35942c37a40f" />

- This segment includes customers with low recent activity but medium or high spending in the past.
- Re-engagement campaigns, such as email reminders, exclusive discounts, or personalized offers, could win them back.


### 2️⃣ Customer Spending Patterns

<img width="746" height="321" alt="image" src="https://github.com/user-attachments/assets/68eea7b0-18e5-4413-8a26-8054fb4d51fe" />

- Loyal Customers and Champions have the highest spending levels, and their purchase frequency shows consistent growth.

### 3️⃣ Customer Demographic Pattern

<img width="746" height="322" alt="image" src="https://github.com/user-attachments/assets/d9dee92a-9b06-4935-bfbc-07f00064f77f" />

- Champions, Loyal Customers, and Potential Loyal Customers are predominantly Teenagers, indicating a strong purchasing power in this demographic.
- Male customers slightly dominate the Champion segment, while females are more prevalent in the Potential Loyalist and Promising groups.

## Recommended Retention Strategies

- **Champions:** SpicyFood should enhance their loyalty by offering VIP programs, exclusive deals, and early access to new products.
- **At-Risk Customers:** Implement reactivation campaigns with targeted discounts and reminders of past positive experiences to encourage repeat purchases.
- **Promising Customers:** Build trust and engagement through personalized recommendations and welcome campaigns to nurture long-term relationships.

## MySQL 
```sql
`USE spicyfood;

SELECT * FROM spicyfood_data;

-- Total Unique Customers count
SELECT DISTINCT(COUNT(*)) AS Total_Customers FROM spicyfood_data;

-- Total bill amount
SELECT SUM(`Bill Amount`) AS Total_Purchase FROM spicyfood_data;

-- Total Number of Orders
SELECT SUM(`Purchase Frequency`) AS Number_of_Orders FROM spicyfood_data;

-- Average Purchase Amount
SELECT ROUND(AVG(`Bill Amount`)) AS Avg_Purchase_Amount FROM spicyfood_data;

-- Unique Customer Tiers
SELECT DISTINCT `Customer Tiers` FROM spicyfood_data;

-- Select Customer ID, Purchase Frequency, Bill Amount and Recent Purchase Date with a Customer Tier "Champions"
SELECT `Customer ID`, `Purchase Frequency`, `Bill Amount`, `Recent Purchase Date`
FROM spicyfood_data 
WHERE `Customer Tiers` = 'Champions';

-- Select Customer ID, Purchase Frequency, Bill Amount and Recent Purchase Date with a Customer Tier "Loyal Customer"
SELECT `Customer ID`, `Purchase Frequency`, `Bill Amount`, `Recent Purchase Date`
FROM spicyfood_data 
WHERE `Customer Tiers` = 'Loyal Customer';

-- find the percentage of customers in each Customer Tier
SELECT 
    `Customer Tiers`, 
    COUNT(*) AS Customer_Count,
    ROUND((COUNT(*) * 100.0 / (SELECT COUNT(DISTINCT `Customer ID`) FROM spicyfood_data)), 2) AS Percentage
FROM spicyfood_data
GROUP BY `Customer Tiers`
ORDER BY Percentage DESC;

--  retrieve customers sorted by their overall rank
SELECT `Customer ID`, `Overall Rank`
FROM spicyfood_data
ORDER BY `Overall Rank`;

-- Select customers who have recently purchased and their total spend
SELECT `Customer ID`, SUM(`Rank_Spending`) AS Total_Spend
FROM spicyfood_data
WHERE `Recent Purchase Date` = (SELECT MAX(`Recent Purchase Date`) FROM spicyfood_data)
GROUP BY `Customer ID`;


-- Gender distribution by Customer Tiers
SELECT 
    `Customer Tiers`, 
    Gender, 
    COUNT(*) AS Customer_Count, 
    ROUND((COUNT(*) * 100.0 / SUM(COUNT(*)) OVER (PARTITION BY `Customer Tiers`)), 2) AS Percentage
FROM spicyfood_data
GROUP BY `Customer Tiers`, Gender
ORDER BY `Customer Tiers`, Percentage DESC;
```
