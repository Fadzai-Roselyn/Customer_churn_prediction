# Customer churn prediction project

## Project/Goals
The project seeks to address customer churn for ConnectTel Telecom company. Customer churn is the percentage of customers that have stopped using a company's product or service, including cancelling a subscription or membership during a certain time frame.
Problem definition and expected benefits;
ConnectTel Telecom Company is facing a critical issue of customer churn, which poses a substantial threat to its business sustainability and growth. The current customer retention strategies lack precision, leading to the loss of valuable customers to competitors. To address this challenge, This project aims to develop a robust customer churn prediction system using advanced analytics and machine learning techniques on available customer data. The goal is to accurately predict customer churn and implement targeted retention initiatives.

The project seeks to provide a solution that empowers ConnectTel with actionable insights derived from customer data, enabling them to predict churn, implement effective retention strategies, and ultimately strengthen their position in the telecommunications market.

## Process
<li> Problem definition
<li> EDA using Python, to understand the data summary and structure, identify patterns, detect anomalies, and create visualizations such as  statistical graphics, charts, and descriptive statistics tables
<li> Feature engineering; encoding categorical variables
<li> Model selection, training and validation
<li> Model evaluation
<li>Tableau
<li>Microsoft PowerPoint; Compilation and presentation of project

## Results
### Correlation of numerical values

The correlation table shows the pairwise correlations between the specified variables:
SeniorCitizen and tenure: A weak positive correlation (0.016567).
SeniorCitizen and MonthlyCharges: A moderate positive correlation (0.220173).
SeniorCitizen and TotalCharges: A weak positive correlation (0.102411).
tenure and MonthlyCharges: A weak positive correlation (0.247900).
tenure and TotalCharges: A strong positive correlation (0.825880).
MonthlyCharges and TotalCharges: A moderate positive correlation (0.651065).

These correlations give insights into the relationships between the variables. For instance, there is a stronger positive correlation between tenure and TotalCharges, indicating that as tenure increases, TotalCharges tends to increase. Additionally, MonthlyCharges and TotalCharges also show a moderate positive correlation. The correlation values range from weak to moderate, suggesting that the relationships are not extremely strong.

An image of the correlation heatmap is attached below;

![alt text](image.png)


### Relationships between churning and selected features
Customer churn by gender;
The gender distribution was males 50.5% : females 49.5%, therefore the customers were almost evenly distributed. The churning rates were also evenly distributed between the genders;
Of the total customers, 37.3% were males that were retained. 36.2% were females that were retained. 13.2% and 13.3% were males and females that churned respectively.

A graph that shows this information is attached below; 

![alt text](image-1.png)

Customer churn by senior citizenship
About 77% of non senior citizens were retained while 23% churned. For senior citizens, about 57% were retained while 43% churned. This shows that senior citizens are more likely to churn compared to non senior citizens. A visualizatiion of this is shown below;

![alt text](image-2.png)

Churn by partner status
It was shown that the people with partners are less likely to churn compared to those without. This could be because of a promotion involving multiple users, however, a survey would be required for a more accurate reason. A graph highlighting this is shown below;

![alt text](image-3.png)

Churn by tenure
From boxplot visuals, retained customers had a median tenure just below 40, with the interquartile range extending approximately from 15 to 60.
This suggests that retained customers have varying tenure lengths.
Churned Customers:
The boxplot had a median tenure around 10, with the interquartile range extending roughly from around 2 to about 30. 
This implies that most customers who churned had shorter tenures. However, there were also some outliers with tenure scores of 68 to just over 70
Tenure matters: Shorter tenure may correlate with higher churn rates.
Retention strategies: Focus on retaining new customers during their early tenure.
The boxplots are shown below;

![alt text](image-4.png)


For other features;
customer churn by dependents showed that those with dependents were less likely to churn.

Customers that had fiber optic internet service were more likely to churn compared to those with DSL and those without internet service. It is also important to note that fiber optic options are usually more expensive.

Customers that did not have the option of tech support were very likely to churn compared to those with support and those without internet. Support may well be a good retention initiative.

The relationship between customer churn and movie and TV streaming was such that for both forms of streaming, the churning rate was almost half of the retention rate.

It was interesting to note that there were contract types as follows; month to month, one year and two years. The less the contract duration, the greater the churning statistics. The two years contract had an extremely low customer churn rate.

The relationship between churn and payment method was also interesting. The methods were Electronic check, Mailed check, Bank transfer (automatic) and Credit card (automatic). For all the other methods, customer churn was around +/-20%, while for Electronic check, churn was around 45%. This means the company has to look at providing alternatives to Electronic check payment method.

All the other charts, diagrams and plots are included in the Jupyter notebook attached.

CLASSIFIERS:

<li>Logistic Regressor
<li>XGBoost Classifier 
<li>Random Forest Classifier
<li>Decision Tree Classifier
<li>CatBoost Classifier

Accuracy scores;

Accuracy Score for Logistic Regressor is 0.8024164889836531 

Accuracy Score for Random Forest is 0.7917555081734187 

Accuracy Score for CatBoost is 0.7981520966595593 

Accuracy Score for XGBoost is 0.7938877043354655 

Accuracy Score for Decision Tree is 0.7341862117981521

The most accurate model was the Logistic Regressor, with an accuracy of 0.80, the least was the decision tree with an accuracy of 0.73

Features that are most important for the problem, based on the models;
Positive Correlations with Churn: The features below have a weak positive correlation with customer churn; MonthlyCharges: 0.19 SeniorCitizen: 0.15 PaperlessBilling: 0.19 PaymentMethod (Electronic check): 0.11

Negative Correlations with Churn: The features below have weak to moderate negative correlation with customer churn;
Contract (Longer-term contracts): -0.40 Tenure: -0.35 Partner_Yes: -0.15 Dependents_Yes: -0.16

These features have a notable impact on customer churn prediction. Notably, longer-term contracts, higher tenure, having a partner or dependents, and lower monthly charges are associated with lower churn. Conversely, having a month-to-month contract, higher monthly charges, being a senior citizen, using paperless billing, and using electronic check as the payment method are associated with higher churn.

## To note
The business should optimize for True Positives, thereby minimizing false negatives. If there are a lot of false negatives, the business will fail to identify customers that may actually churn, inturn losing out on potential revenue. Minimizing false negatives allows the business to target customers that are likely to churn and enticing them to stay.

The business shouls also aim to optimizing for False Negatives, which would minimize False Positives. It would not be economic to direct marketing man power and costs to attract customers who would have stayed anyway.

## Future research
The importance of features and metrics that are important for these predictions may differ based on the model and other factors. It would be interesting to use machine learning algorithms for a more thorough evaluation of feature importance.
