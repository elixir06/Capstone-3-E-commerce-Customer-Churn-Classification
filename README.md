# Capstone-3-E-commerce-Customer-Churn-Classification

### Business Background
---
In the competitive e-commerce industry, retaining customers is crucial for long-term success, as customer churn leads to lost revenue and higher acquisition costs. Our company faces the challenge of stabilizing customer base in the middle of intense competition. By utilizing data analytics and machine learning, we aim to identify at-risk customers and implement targeted retention strategies or optimizing resources alocation.


### Data details
---
Features
-	Tenure: Tenure of a customer in the company.
-	WarehouseToHome: Distance between the warehouse to the customer’s home.
-	NumberOfDeviceRegistered: Total number of deceives is registered on a particular customer.
-	PreferedOrderCat: Preferred order category of a customer in the last month.
-	SatisfactionScore: Satisfactory score of a customer on service.
-	MaritalStatus: Marital status of a customer.
-	NumberOfAddress: Total number of added on a particular customer.
-	Complaint: Any complaint has been raised in the last month.
-	DaySinceLastOrder: Day since last order by customer.
-	CashbackAmount: Average cashback in last month
-	Churn: Churn flag.


### Business Problem
---
Customer churn, the phenomenon where customers stop using a company's products or services, poses a significant risk as it leads to lost revenue and lost any retention efforts. Understanding and predicting churn is crucial for our company to implement effective retention strategies. This involves examining various customer-related features such as tenure, satisfaction scores, complains, cashback amount, etc to understand their impact on churn.

### Machine Learning Objective 
--- 
The objective are as followed : 

- Develop a machine learning model to accurately predict customer churn within the next month, enabling the company to implement targeted retention strategies and reduce churn

- Cost Reduction through predictive analysis by Eliminating Cashback for Predicted Churners


### Data cleaning done :
---
- dropping duplicates (to prevent redundancy)
- filling null values with median (since the data numerical data is not normally distributed)
- keeping the outliers (so that the model will be more resilient to anomalies)

### Model Chosen : XGBoost Classifier (F2 score after parameter tuning : 93.11%)
---


From the result of confusion matrix in the test set (654), the model successfully predicted :
- 525 True Negatives = The customers who were predicted to not churn and actually not churn
- 23 False Negatives (type II error) = The customers who were predicted to not churn but actually churn
- 22 False Positives (type I error) = The customers who were predicted to churn but actually not churn
- 84 True Positives = The customers who were predicted to churn and actually churn

Cashback will not be given the False Positive group and True Positive group, since they are predicted to churn regardless they will churn or not. 
