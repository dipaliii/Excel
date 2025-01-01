# Excel Project: Customer Churn Analysis
### Dashboard: Excel is attached in this repository 
## Problem Statement

The objective of this project is to analyze customer churn for a fictitious Telecom provider, **Databel**. The goal is to understand the reasons behind customer churn, or why customers are leaving Databel.

**Dataset Overview:**
- The dataset consists of **29 columns**, with **one row per customer**.
- The dataset represents a snapshot at a specific point in time, with no time dimension involved.

**Key Dimensions and Measures in the Dataset:**
1. **Customer_id**: A unique identifier for each customer.
2. **Churn Label**: Indicates whether a customer churned ("Yes" or "No").
3. Various **demographic** information and data on **premium plans**.

4. **Total Charges**: The sum of all monthly charges billed to a customer.

The analysis will focus on identifying trends, patterns, or correlations that explain why customers are churning from Databel. The metadata sheet provides detailed descriptions of all columns, accessible from the course overview page or through a link in the first hands-on exercise.
### Steps followed 
Step 1 : To prepare the data: check for duplicate rows, converting the raw excel data to tabular format.

Step 2 : Create a measure named "churned" that converts "Churn Label" that indicated yes/no to binomial value that will be useful to calculate Churn Rate. Formula: IF([@[Churn Label]]="Yes", 1, 0)

Step 3 :Create a blank PivotTable of the Customers table and place it in a new Worksheet.
- Rename this worksheet "Customer Pivots" and display the total count of customers and number of churned customers. 
- Add a new calculation with the header "Churn Rate" that divides churned customers by total customers.
Step 4: This step is to investigate the different reasons why customers churned, to create a column chart listing the different reasons why customers churn.
- Start with analyzing the total number of churned customers by Churn Reason, sort the Churn Reason by Churned customers and display the value as % of Grand Total.
- Visualize your analysis with a 2D Bar Chart and title it "Churn Reasons".


![Uploading Churned Reason (Step4).png…](https://github.com/user-attachments/assets/03cc9afd-260d-4440-8839-7db6cab49123/)

Step 5: This step is to identify which churn category is accounting for the highest proportion of churn and understand which priority we should tackle first based on the churn reason.
- The category driving the highest % of churn is Competitor, so we filter the category to only Competitors and visualize it in a donut chart.
  
![Uploading Competitor Churn Analysis (step5).png…](https://github.com/user-attachments/assets/20653248-98e6-41b6-8091-66c5cca2b572)

Step 6: Analyzing the different demographic fields from the Aggregate dataset:
- A new column "Demographic" that categorizes customers into the following categories: "Under 30", "Senior" and "Other".
- Create a Pivot table of Aggregate data and use demographic and add churn rate which will give insights that Customers are considered Senior are the most likely segment to churn at almost 40%. 
Step 7: To analyze the customer age with respect to the churn rate:
- Create a line and clustered column chart that shows the number of customers and churn rate for every age bracket(by creating groups for Age with a split of 10).
- Customers aged between 79-88 only make up a small percentage of our customer base but have the highest churn rate. This might be expected as customers in this age range may pass away, but there may be other factors that are causing our customers to churn.
  
![Uploading Age Group(step7).png…](https://github.com/user-attachments/assets/81539a01-d017-42f1-8dd4-51af9b99b767)

Step 8 : To analyze the relationship between customers' international activity and churn. They are curious about the behavior of customers who call internationally, and if paying for an international plan influences their loyalty.
- Matrix of churn rate by State and whether a customer is on an Intl Plan
- Using Conditional Formatting color scale we can easily spot the state with highest churn rate that has an internal plan
Step 9 : To investigate two important topics related to customers: the contract type, and how many months a person is a customer.
- Create a pivot table to check churn rate against account length and categorize using contract type.
- Customers between the 3 and 4 year mark are much more likely to churn on a One Year contract compared a Two Year. Sales and marketing can use this information to provide offers that would get customers to sign up to 2 year deals.
Step 10 : To investigate two important topics related to customers: the contract type, and how many months a person is a customer.
- Create a pivot table to check churn rate against account length and categorize using contract type.
- Customers between the 3 and 4 year mark are much more likely to churn on a One Year contract compared a Two Year. Sales and marketing can use this information to provide offers that would get customers to sign up to 2 year deals.
Step 11 : To investigate how the Unlimited Data Plan influences the churn rate.
- Create a pivot table to check churn rate against Unlimited Plan and It appears that customers who are on an unlimited plan are more likely to churn. To see if it is related to a certain amount of mobile data (GB) being used, create a new column in Aggregate called Grouped Consumption that classifies the average monthly GB download in the following groups:
	- Less than 5 GB.
	- Between 5 and 10 GB.
	- 10 or more GB.
- To visualize Churn Rate by Unlimited Data Plan and broken out by average consumption levels. Customers who consume the lowest amount of data are actually the most likely to churn at almost 35%.
![Uploading consumption(step11).png…](https://github.com/user-attachments/assets/7947cb67-163f-46c1-8f5d-89bb845077d7)


### Dashboard

Add some context into why our customers are churning with a particular focus on customers who churn as a result of our competitors activities.
This concludes that Customers are not leaving because they are necessarily getting a better service, there are other indicators for why they are leaving.

In the final step of the churn analysis project, it's important to structure the findings in a cohesive and clear manner. Simply presenting a series of visualizations spread across different sheets is not effective. The key is to combine the insights in a way that they flow logically and fit together seamlessly. The goal is to present all the discoveries and conclusions from the analysis using the fewest sheets possible, ensuring that the insights are both comprehensive and easy to understand. This will provide a streamlined and impactful presentation of the churn analysis results.


![Uploading dashboard.png…](https://github.com/user-attachments/assets/b71963b2-467a-42c2-a983-ed9463e85c84)

