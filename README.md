# Contoso - Sales Analysis

## Overview
Analysis of customer behaviour, retention and lifetime value for an e-commerce company to improve customer retention and maximise revenue. 

## Business Questions

1. **Customer Segmentation:** Who are our most valuable customers?
2. **Cohort Analysis:** How do different customer groups generate revenue?
3. **Retention Analysis:** Which customers haven't purchased recently?

## Analysis Approach

### 1. Customer Segmentation Analysis

    - Categorised customers based on total lifetime value (LTV)
    - Assigned customers to High, Mid, and Low-value segments
    - Calculated key metrics: total revenue

Query: [1_customer_segmentation.sql](/1_customer_segmentation.sql)

**Visualisation:**

![Customer Segmentation: Total LTV Distribution](/images/1_customer_segmentation.png)

**Key Findings:**
- High Value segment (25% of customers) drives 66% of revenue (c. $135M)
- Mid Value segment (50% of customers) generates 32% of revenue (c. $66M)
- Low Value segement (25% of customers) accounts for 2% of revenue (c. $4M)

**Business Insights:**
- High Value (66% of revenue): 
    - Offer premium membership program to 12,372 VIP customers, as losing one customer significantly impacts revenue
- Mid Value (32% of revenue): 
    - Create upgrade paths through personalised promotions, with potential revenue increase opportunity from $66.6M to $135.4M
- Low Value (2.1% of revenue): 
    - Design re-engagement campaigns and price-sensitive promotions to increase purchase frequency

### 2. Cohort Analysis
- Tracked revenue and customer count per cohort
- Cohorts were grouped by year of first purchase
- Analysed customer retention at a cohort level

Query: [2_cohort_analysis.sql](/2_cohort_analysis.sql)

**Visualisation:**

![Cohort Analysis](/images/2_cohort_analysis.png)

**Key Findings:**
- Revenue per customer shows an alarming decreasing trend over time
    - 2022-2024 cohorts are consistently performing worse than earlier cohorts
    - NOTE: Although net revenue is increasing, this is likely due to a larger customer base. which is not reflective of customer value

**Business Insights:**
- Value extracted from customers is decreasing over time and needs further investigation. 
- In 2023 we saw a drop in number of customers acquired, which is concerning. 
- With both lowering LTV and decreasing customer acquisition, the company is facing a potential revenue decline. 


### 3. Retention Analysis

    - Identified customers at risk of churning
    - Analysed last purchase patterns
    - Calculated customer-specific metrics

Query: [3_customer_retention.sql](/3_retention_analysis.sql)

**Visualisation:**

![3_customer_retention](/images/3_customer_retention.png)

**Key Findings:**
- Cohort churn stabilises at c.90% after 2-3 years, indicating a predictable long-term retention pattern. 
- Rentention rates are consistently low (8-10%) across all cohorts, suggesting retention issues are systemic rather than specific to certain years.
- Newer cohorts (2022-2023) show similar churn trajectories, signaling that without intervention future cohorts will follow the same pattern. 

**Business Insights:**
- Strengthen early engagement strategies to target the first 1-2 years with onboarding incentives, loyalty rewards and personalised offers to improve long-term retention. 
- Re-engage high-value churned customers by focusing on targeted win-back campaigns rather than broad retention efforts, as reactivating valuable customers may yield higher ROI. 
- Predict & preempt churn risk and use customer-specific warning indicators to proactively intervene with at-risk customers before they lapse. 

## Strategic Recommendations

1. **Customer Value Optimisations:** (Customer Segmentation)
- Launch VIP program for 12,372 high value customers (66% revenue)
-Create personalised upgrade paths for mid value segment ($66.6M - $135.4M opportunity)
- Design price-sensitive promotions for low value segment to increase purchase frequency

2. **Cohort Performance Strategy:** (Customer Revenue by Cohort)
- Target 2022-2024 cohorts with personalised re-engagement offers
- Implement loyalty/subscription programs to stabilise revenue fluctuations
- Apply successful strategies from high spending 2016-2018 cohorts to newer customers

3. **Retention & Churn Prevention:** (Customer Retention)
- Strengthen first 1-2 year engagement with onbvoarding incentives and loyalty rewards
- Focus on targeted win-back campaigns for high value churned customers
- Implement proactive intervention system for at-risk customers before they lapse

## Technical Details
- **Database:** PostgreSQL
- **Analysis Tools:** PostgresSQL
- **Visualisation:** ChatGPT/Python