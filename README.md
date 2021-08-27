# Predicting-Churn-for-Bank-Customer-using-Artificial-Neural-Network

![Churn](https://user-images.githubusercontent.com/87844891/131072128-f060d8e0-e814-47ed-95c0-ac6e1bf14948.png)                            

In any customer-based business, retaining the customer is the most valuable asset for the organization. They emphasize the higher costs associated with attracting new customers than retaining existing customers and the fact that long-term customers tend to produce more profits. So many competitive organizations have realized that a key strategy for survival within the industry is to retain existing customers. And this leads to the importance of churn management. Customer churn (also known as customer attrition) occurs when a customer stops using a company's products or services.

Why is customer churn management essential for business?

- To identify issues with its services (for example, bad product/service quality, poor customer service, the wrong target demographic, etc.)

- To make proper strategic decisions that will lead to improved customer satisfaction and, as a result, higher customer retention.

# About the dataset
For this kernel, I chose a dataset from Bank as Banks are no exception in this churning rule. There are columns of information about the bank customers and also their status of retention in the bank.

# Objective of this project

1. To understand and predict customer churn for a bank by performing Exploratory Data Analysis (EDA) 
   -to identify and visualize the factors contributing to customer churn. 
   
2. To build an ANN model to predict whether a customer will churn or not. 

3. To evaluate the prediction model on how accurate the prediction is.

# Libraries that needed
- NumPy, pandas, TensorFlow, Matplotlib, Seaborn. 

# Data exploration
-Started with importing the dataset and viewing the dataset
This data frame has 14 features/attributes and 10K customers/instances.

![row](https://user-images.githubusercontent.com/87844891/131079889-18694c86-e933-4744-9ad1-4ca20bcc6663.png)

-RowNumber 

-CustomerId

-Surname 

-CreditScore (that depicts a consumer's creditworthiness)

-Geography (demographic of the customer)

-Gender

-Age

-Tenure (the number of years they have been in the bank)

-Balance (the amount of money they have on their account)

-Number of Products (the number of products they use from the bank) 

-Has Card (1= has a credit card. 0= no credit card)

-IsActiveMember (1= active member. 0= inactive member)

-EstimatedSalary 

-Exited (whether the customer has churned (0 = No, one = Yes) 

I checked the data type and dropped the RowNumber, CustomerId, and Surname columns as it doesn't give any significant value for analysis. Also checked for the missing value in the dataset, and there is no missing value

![44](https://user-images.githubusercontent.com/87844891/131080619-eb486a8d-b8b1-46ff-a3b5-7e2d6d0ab581.png)

Next, used the describe() method gives a statistical summary of the numerical features:

![33](https://user-images.githubusercontent.com/87844891/131080746-2d0a2c46-62a3-4ea5-be18-678fc4f76b14.png)

This gives important insights like:

- The age of customers ranges from 18 to 92, with a mean value approximately equal to 40

- The mean (and median) tenure is five years, so the majority of customers is loyal (tenure > 3), and
Approximately 50% of customers are active.

# Exploratory Data Analysis (EDA)

First, I analyzed our dependent variable or target variable of this dataset (EXITED)

![image](https://user-images.githubusercontent.com/87844891/131081202-8c208fb2-600e-43a7-b73e-3908191601bb.png)

This pie chart shows:
- The bank managed to retain 80% of its customer; while
- 20% of customers have exited from the bank
Even though the number of exited customers is smaller than the retained customers, this can ruin the bank's image in the long run. 

Secondly, I plotted a bar chart for Non-continuous variables like Geography, Gender, Has Credit card, and Is active.

![image](https://user-images.githubusercontent.com/87844891/131082551-cb224117-c83d-4a29-a903-d8baee966a4d.png)

From this analysis, I can see that. 

- Customers from France and Germany have the same and high amount of customers exiting from the bank compared to Spain

- Female customers have exited more from the bank that male customers

- Customer that has Credit card has exited more than the customers that does not credit card

- Inactive members left the bank most compared to the active members 

Thirdly, I analysed the Continuos varibles like CreditScore, Age, Tenure, Balance, Number of Products and Estimated salary using Boxplot

![image](https://user-images.githubusercontent.com/87844891/131085322-06ade812-0ef4-49aa-a804-d142a05a04d6.png)

From this analysis, I note the following: 

- There is no substantial variation in credit score distribution between retained and exited customers.

- Customers in the older age groups are churning at a higher rate than those in the younger age groups, implying a difference in service preferences. 

- Concerning the tenure, the clients on either end (spent little time with the bank or a lot of time with the bank) are more likely to churn than those of average tenure.

- The customer with pretty large balance is exiting compared to those who have small balance

- The salary does not cause any differences to the amount of customers exited and retained



Lastly, I analyzed the correlations between the variables

![image](https://user-images.githubusercontent.com/87844891/131086940-cea91d02-f0ad-482b-a7e2-ab4328b1749b.png)

- And there is no significant correlation between the variables


