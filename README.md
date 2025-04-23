## RFM Analysis using Excel-Customer Segmentation

## Business Objective

**To analyze the usage behavior of savings account holders, identify customer segments, and develop targeted strategies to improve engagement and cross-sell opportunities.**

Segmentation of savings account customers using RFM (Recency, Frequency, Monetary) analysis to identify high-value clients, dormant accounts, and cross-selling opportunities, leading to targeted retention strategies and increased engagement

### **Data Used    (5000 customers)**

- Transaction_ID
- Customer_ID
- Date
- Amount
- Response Rate ( from past email campaign, 0- means, purchase not done, 1-purchase done)

### **Methodology**

- Using **pivot tables**, we find the total transactions per customer, Min(Date) -Start Date, Max(date) - Most recent date, Sum of amounts
- Years with us = Difference of Start date and Most recent date/365
- Frequency= Total transactions/Years with us
- Monetary/yr= Monetary value/Years with us
- R,F,M scores using **excel formula RANK.AVG**
- Calculate RFM scores for each customer by assigning ranks **using IF/IFS**, for example, 0-1000 will be given a score of 5, 1000-2000 will be given score 4 and so on
- Find number of customers in each category and number of positive responses received using **COUNTIFS**
- Response Rate= Number of positive responses/Total responses
- Finding the breakeven point, assuming **cost of sending a mail=1$** and **avg profit per sales=20$** so if more than one in every 20 customers responds positively, then it is profitable. We can **further safeguard** by doubling the threshold , 0.05*2=-0.1, hence target customers having **response rates above 0.1.**

## **Key Insights & Recommendations**

**Combining RFM and response Rate**, response rate for profitability and RFM score to understand customer type for message personalisation.

Based on different industries like E-Commerce ,banking and financial, Saas different marketing campaigns can be implemented on these categories.

For example in financial services industry, say if data pertains to **savings account deposits** of different customers.

### **Champions (35% Response Rate)**

These high RFM customers represent our most valuable segment with the highest response rate. **Award them for their loyalty,** provide wealth management plans, enhanced banking features, dedicated relationship managers

### **Loyal Customers (28% Response Rate)**

With strong RFM scores, these customers respond well to engagement. **Focus on relationship-building** and encourage monthly top-ups, push platinum cards with cash-back offers and lifestyle privileges , cross-sell FD’s, RD’s and credit cards

### **Potential Loyalists(21% Response Rate)**

These are engaged recently and have moderate frequency and value. Reward for consistent deposits, debit card usage drive, like swiping the card 3x and win cashbacks, shared tailored wealth creation plans, have feedback touchpoint

### **At Risk High Value (15% Response Rate)**

Despite high monetary value , these customers show declining engagement. **Implement retention strategies** before they become dormant, send email nudges like encouraging monthly top-ups, build trust, cashbacks for next deposits, offer loyalty points if they deposit monthly for 3 months, limited time FD offers 

### **Recent Customers(12% Response Rate)**

They have just joined and have low frequency/value, they need onboarding and habit building, send welcome campaigns, give them first action rewards, promote auto-sweep, educational series

### **Implementation Impact**

In my project, we applied RFM segmentation to savings account customers and launched targeted campaigns to improve engagement and optimize ROI.

- **Champions**, our highest value segment, had an initial response rate of **35%** from past campaigns. Post-strategy, this improved to **42%**, validating the effectiveness of tailored wealth management offers and loyalty incentives.
- **At-Risk High Value** customers improved from **15% to 27%**, indicating the success of retention strategies like cashback offers and loyalty points.
- **Recent Customers** grew from **12% to 20%** response rate after onboarding nudges and welcome rewards.
- We avoided campaigns to segments with **<5% historical response** to optimize costs.

This approach led to improved engagement, **smarter spending in key segments by 8–12%**, leading to **₹4.15 lakh in incremental deposits** and a **26x blended ROI.**
