# Building_a_Retail_Sales_Data_Agent_on_Databricks-_RetailSales-Insights
This project involved building an AI-powered data agent using Databricks, designed to analyse a retail sales dataset and answer business questions using natural language. The agent, named the Retail Sales Insights Agent, was configured to query structured sales data and return meaningful insights without requiring manual SQL or data analysis skills from the end user.
The objective of this project was to demonstrate how a data agent can be set up on Databricks to interact with a retail dataset, generate SQL queries automatically, validate outputs, and surface actionable business recommendations. The project also aimed to develop practical skills in data agent configuration, prompt engineering, and result validation.
___________________________________________________________________________________________________________________________________________________________________________ 
# Project Objective

This project involved building an AI-powered data agent using Databricks, designed to analyse a retail sales dataset and answer business questions using natural language. The agent — named the Retail Sales Insights Agent — was configured to query structured sales data and return meaningful insights without requiring manual SQL or data analysis skills from the end user.
The objective was to demonstrate how a data agent can be set up on Databricks to:
•	Interact with a retail dataset
•	Generate SQL queries automatically
•	Validate outputs against raw data
•	Surface actionable business recommendations
The project also aimed to develop practical skills in data agent configuration, prompt engineering, and result validation.
____________________________________________________________________________________________________________________________________________________________________________

| Tools            | Purpose                                      |
|------------------|----------------------------------------------|
| Databricks       | Data platform and Genie Space for the agent  |
| PySpark          | Data preparation and exploration             |
| Databricks Genie | AI agent configuration                       |
| GitHub           | Project submission and version control       |
| Microsoft Word   |  Write-up documentation                                             |
| SQL              | Answer validation and data checking          |
            ****  
____________________________________________________________________________________________________________________________________________________________________________

# Dataset Overview

The dataset (retail_sales_data) contains 1,000 retail transactions recorded between January 2023 and January 2024, across three product categories.

| Transaction ID | Date       | Customer ID | Gender | Age | Product Category | Quantity | Price per Unit ($) |
|----------------|-----------|------------|--------|-----|------------------|----------|--------------------|
| 1              | 2026/01/15| CUST001    | Male   | 34  | Electronics      | 2        | 250                |
| 2              | 2026/01/16| CUST002    | Female | 28  | Clothing         | 1        | 75                 |
| 3              | 2026/01/17| CUST003    | Male   | 45  | Beauty           | 3        | 50                 |
| 4              | 2026/01/18| CUST004    | Female | 22  | Electronics      | 1        | 400                |
| 5              | 2026/01/19| CUST005    | Male   | 39  | Clothing         | 4        | 120                |



____________________________________________________________________________________________________________________________________________________________________________
## Steps Followed

### 1. Upload the Dataset
Loaded the retail_sales_data dataset into Databricks and confirmed successful upload.

### 2. Review the Data
Explored the dataset by checking columns, data types, and total row counts to understand its structure.

### 3. Prepare the Table
Cleaned the dataset by addressing any data quality issues and registered it as a table in the Databricks catalog.

### 4. Create the Data Agent
Set up a Genie Space and connected it to the prepared dataset to enable querying.

### 5. Write Agent Instructions
Configured the agent’s behaviour, tone, and response expectations to ensure consistent outputs.

### 6. Test with 10 Questions
Executed 10 queries against the agent and captured both the generated SQL and the results returned.

### 7. Validate 3 Answers
Cross-checked three selected responses by comparing the agent’s outputs with the raw dataset to confirm accuracy.
____________________________________________________________________________________________________________________________________________________________________________
## Agent Instructions

Your name is 'Retail Sales Insights Agent'. You are designed to help me understand
the data loaded for this activity. Do not hallucinate. You are to use the data
uploaded in this schema only. You always use a soft executive tone when responding.
Keep it professional and explanatory to a person who does not understand data analysis.

____________________________________________________________________________________________________________________________________________________________________________
## Sample Questions Tested

1. Which product category generates the most revenue?  
2. What is the total revenue generated?  
3. Which product category is most popular by quantity sold?  
4. Visualize the gender split using a pie chart.  
5. Segment customers by spending level (low, medium, high).  
6. Are there any seasonal trends in product category sales?  
7. What does each gender buy the most?  
8. Generate a monthly sales summary report.  
9. Which month recorded the highest number of sales? Visualize it.  
10. How many women bought products in January?
____________________________________________________________________________________________________________________________________________________________________________

# Key Insights

1. High-value customers drive the majority of revenue  
Just 20% of transactions (202 out of 1,000) account for 63% of total revenue ($286,800 out of $456,000). High-value purchases averaged $1,420 versus $212 for regular transactions, indicating a strong opportunity to target and retain premium customers.

2. Younger customers show the highest propensity for premium purchases  
The 18–24 age group demonstrates a 26.8% high-value purchase rate, outperforming all other age segments. This highlights younger customers as a critical growth segment despite common assumptions about purchasing power.

3. Product categories are remarkably balanced  
Electronics, Clothing, and Beauty each contribute approximately one-third of total revenue (34.4%, 34.1%, and 31.5% respectively). Electronics shows the highest seasonal volatility, while Beauty remains the most stable throughout the year.

4. May is the peak revenue month  
May 2023 recorded the highest revenue ($53,150), the most transactions (105), and the highest number of units sold (259). This was driven by a 57% month-over-month increase in Electronics sales, suggesting strong seasonal demand.

5. Every customer made exactly one purchase  
The dataset contains 1,000 transactions from 1,000 unique customers with no repeat purchases. This indicates either a focus on acquisition or a first-time buyer snapshot, highlighting an opportunity to build retention and loyalty strategies.

____________________________________________________________________________________________________________________________________________________________________________
## Recommendations

1. Increase average basket size  
Some customers purchase low quantities despite moderate transaction frequency. Add “Frequently Bought Together” suggestions, introduce discounts for multi-item purchases, and create bundle offers across categories to encourage higher spend per transaction.

2. Target female customers more deliberately  
With a slight female majority (51%) and strong engagement in Beauty and Clothing categories, tailored marketing campaigns, personalised emails, and loyalty programmes aimed at female shoppers can drive increased revenue and improve customer retention.

3. Reduce one-item transactions  
Although the average quantity per transaction is 2.5, many customers still purchase only one item. Introduce incentives such as “add one more item for a discount” or free shipping thresholds above a minimum basket value to increase both quantity per transaction and overall order value.

____________________________________________________________________________________________________________________________________________________________________________
## Conclusion

The Retail Sales Insights Agent proved to be a valuable tool for transforming raw retail data into actionable business intelligence. Setting up the agent in Databricks was straightforward, and once connected to the dataset, it delivered accurate and efficient responses to a broad range of business queries.

The most challenging aspect was developing precise agent instructions. Vague prompts occasionally resulted in generic outputs, requiring refinement to achieve more specific and data-driven responses. Validating the agent’s outputs against the raw dataset was also time-intensive but necessary to ensure accuracy and reliability.

If approached differently, the agent instructions would be more structured from the beginning, clearly defining column names, expected output formats, and the type of insights required. Additionally, using a larger dataset with timestamps and richer customer demographics would enhance the agent’s ability to identify deeper patterns and trends.

Despite these challenges, the project successfully demonstrated how AI-powered data agents can democratise data analysis, enabling users to access meaningful insights without requiring advanced technical expertise.
