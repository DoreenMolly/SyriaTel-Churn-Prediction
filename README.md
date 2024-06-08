# SyriaTel Churn Prediction
## Business Understanding
Syriatel is a telecommunications company that operates in Syria. It is one of the two major mobile network operators in the country. Syriatel was founded in 2001 and is one of the largest companies in Syria. It is majority-owned by Rami Makhlouf, a Syrian businessman with close ties to the Assad regime.

The company plays a crucial role in connecting people and driving economic growth by providing a range of mobile services including voice, SMS, and data. It has a significant market share in the Syrian mobile market. They also offer various data plans catering to different customer needs, allowing users to access the internet, stream music/videos, and use mobile applications.

SyriaTel targets individual consumers in Syria, offering mobile subscriptions with voice, text, and data options to suit various usage patterns (personal, professional). Subscription-Based Revenue: SyriaTel's primary revenue stream comes from customer subscriptions to their mobile network plans. These plans offer a set amount of voice minutes, text messages, and data for a fixed monthly fee.

## Problem Statement
SyriaTel is facing the challenge of customer churn, where customers discontinue their services. This churn results in lost revenue and increased customer acquisition costs. To address this challenge, we can use machine learning to build a customer churn prediction model. This model will analyze historical customer data to identify patterns and characteristics associated with customer churn. By predicting which customers are at high risk of churning, SyriaTel can take proactive steps to retain these valuable customers.

## Objectives
To prepare the data for modeling by handling missing values, encoding categorical variables, and scaling features.
To understand the dataset's characteristics, identify patterns, and uncover insights to inform modeling through EDA.
To create a training and testing set for model evaluation using an 80-20 split.
To develop a simple baseline model to establish a performance benchmark.
To develop a more complex model (Random Forest classifier) to improve performance.
To optimize the model's performance by tuning on the Random Forest model using GridSearchCV.
To assess the final model's performance and interpret the results.
To create a non-technical presentation with an overview, modeling approach, and results.
To offer actionable insights and recommendations based on model results.

## Exploratory Data Analysis

### Checking Counts for Columns with Numeric Features
![Description of Image](http://localhost:8888/view/Image1.png)

### Checking Counts for Columns with Categorical Features
![Description of Image](http://localhost:8888/view/Image2.png)


## Modeling
![Description of Image](http://localhost:8888/view/Image3.png)
Our Logistic Regression model has a relatively high number of false positives (215) compared to true positives (351), indicating that it often incorrectly classifies negative instances as positive. The number of false negatives (34) is lower than the number of false positives, suggesting that it is more likely to incorrectly classify positive instances as negative.

Our XGBoost model shows a very low number of false positives (1) and a relatively low number of false negatives (15), indicating high precision and recall. The high number of true positives (555) and true negatives (86) suggests that it performs well in distinguishing between the classes.

Our Random Forest model has a high number of true positives (2799) and true negatives (2615), indicating strong overall performance. The number of false positives (51) and false negatives (235) is higher than in the XGBoost, but still relatively low given the large number of instances.

![Description of Image](http://localhost:8888/view/Image4.png)

## Conclusion
Among the three models evaluated (Logistic Regression, XGBoost, Random Forest), XGBoost demonstrates the best overall performance across multiple metrics, including accuracy, precision, recall, and F1 score. It consistently outperforms both Logistic Regression and Random Forest, indicating its effectiveness in predicting churn.

Analyzing the confusion matrices reveals that XGBoost has the lowest number of false positives and false negatives compared to Logistic Regression and Random Forest. This confirms its ability to correctly classify both positive and negative instances.

Based on these findings, I recommend using the XGBoost model as the final predictive model for churn prediction. Its superior performance in terms of accuracy, precision, recall, and F1 score, along with its robustness demonstrated through cross-validation, makes it the most suitable choice for predicting customer churn.

## Recommendations
![Description of Image](http://localhost:8888/view/Image5.png)

Based on our Feature Importance graph, to reduce churn, I would advise SyriaTel to:

Focus on improving customer service quality, as frequent calls to customer service likely indicate dissatisfaction.
Implement proactive measures such as follow-up calls.
Review the pricing strategy and provide transparent billing to mitigate churn caused by the high total charges.
Offer attractive international calling plans and promotions so as to retain customers who make frequent international calls.


