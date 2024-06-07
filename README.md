Syria Tel :
consumer churn data analysis
BY: EUGENE MARIUS

## **Overview**

Syria Tel faces a significant issue with declining paying customers, leading to lower revenue, increased expenses for new clients, and weakened brand loyalty. To reduce attrition and boost retention, a robust data-driven strategy is needed. The project aims to develop a model for forecasting customer attrition using SyriaTel's customer data, enabling targeted retention efforts and reducing attrition.

## **BUSINESS UNDERSTANDING**
The project aims to forecast customer churn, focus on high-risk consumers for retention, increase customer lifetime value, enhance client experience, and use model insights for customized marketing campaigns. 
SyriaTel's CRM system will be used to gather data on user demographics, account information, call usage trends, and customer service interactions. By anticipating problems and understanding customer behavior, businesses can build loyalty and improve overall customer experience. Data-driven decision making guides strategic retention initiatives and resource allocation.. 

## **DATA PROCESSING & MODELING**
-Label Encoding: converts label variables in "international plan", "voice mail plan", and "churn" columns to numeric form. The "Yes" and "No" categories are converted to 1 and 0, respectively, representing presence or absence. In the "churn" column, "False" and "True" categories are converted to 0 and 1, respectively, representing customer churn.
-One-hot encoding:  this converts categorical variables into numerical format for machine learning algorithms, especially useful for dealing with variables with multiple categories.
-Resample function: ensures a fairer representation of data and potentially enhancing the model's performance in handling imbalanced datasets

## **Modeling:** 
The SyriaTel Customer Churn project aims to develop a classifier that predicts customer churn based on call usage, account details, and customer service interactions, using machine learning techniques to accurately predict outcomes for unseen data.

Logistic Regression: 
Despite having an accuracy of 85%, the logistic regression model's recall and precision for predicting churn are both poor at 18% and 58%, respectively, suggesting a large miss of actual churn cases. The model might not be the best option for this classification assignment, according to these results..

Random Forests
The model exhibits high accuracy at 93.7%, with high precision, recall, and F1-score in the majority class ('False'). However, it tends to miss some 'True' samples, with a lower recall at 60%. The weighted averages show robust performance across both classes.

This XGBoost model demonstrates high precision, indicating that when it predicts a customer will churn (True), it is correct 96% of the time. However, its recall for churn is lower at 77%

The ROC AUC score of 0.93 for both models demonstrates strong discriminatory power, reducing false positives and false negatives, indicating their ability to accurately capture data patterns and provide well-informed predictions across various threshold values, thereby enhancing their reliability in classification tasks.
Hyperparameter Tuning:
We are going to select the two best performing models and tune them

##**Evaluation Metrics**
XGBoost vs Random Forest Evaluation
XGBoost outperformed Random Forest in accuracy, recall, and F1-score.
XGBoost achieved a higher accuracy (0.9610) than Random Forest (0.9415).
Random Forest had a perfect precision (1.0000), indicating all positive predictions were correct.
XGBoost's higher recall (0.7723) indicates its ability to identify more true positives.

Feature selection is crucial in enhancing model performance, reducing overfitting, and improving interpretability. Prioritizing informative features simplifies the model, reduces computational costs, and may improve predictive accuracy.

## **CONCLUSION & RECOMENDATION**
The project developed machine learning models to predict customer churn for SyriaTel using classification algorithms like Logistic Regression, Random Forests, and XGBoost. Key predictors of churn were identified and accurate predictive models were developed. 
The best course of action is focusing on customer retention strategies, enhancing service offerings, continuous model monitoring, establishing a customer feedback loop, and investing in data analytics and infrastructure. 
Targeted customer retention strategies, especially for high churn risk customers, can reduce churn rates and improve customer satisfaction. 
Enhancing service offerings, such as international plans and call durations, can also help. Continuous monitoring and retraining with updated data are recommended to ensure model effectiveness.


PRESENTATION: https://docs.google.com/presentation/d/1Vh3gVzYZm1DrjEq-J4UMNEM0qf0tdG0g/edit?usp=sharing&ouid=116677781127272109482&rtpof=true&sd=true

**RESORCES**
https://www.datacamp.com/tutorial/python-tips-examples?utm_source=google&utm_medium=paid_search&utm_campaignid=19589720824&utm_adgroupid=157156376311&utm_device=c&utm_keyword=&utm_matchtype=&utm_network=g&utm_adpostion=&utm_creative=684592140434&utm_targetid=dsa-2218886984100&utm_loc_interest_ms=&utm_loc_physical_ms=1009824&utm_content=&utm_campaign=230119_1-sea~dsa~tofu_2-b2c_3-row-p2_4-prc_5-na_6-na_7-le_8-pdsh-go_9-nb-e_10-na_11-na&gad_source=1&gclid=EAIaIQobChMIz_Pzg7rJhgMVT6ODBx0SZxt3EAAYASAAEgJVz_D_BwE

https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/code

https://www.w3schools.com/python/
