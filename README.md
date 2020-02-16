# Customer-Churn-Prediction
<img src = https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/1.jpg>

## BUSINESS PROBLEM:
Customer churn, also known as customer attrition, occurs when customers stop doing business with a company. The companies are interested in identifying segments of these customers because the price for acquiring a new customer is usually higher than retaining the old one. For example, if Netflix knew a segment of customers who were at risk of churning they could proactively engage them with special offers instead of simply losing them.

## OBJECTIVE and CONSTRAINTS:
- To develop a model for predicting customer churn at a fictitious wireless telecom company .
- Use insights from the model to develop an incentive plan for enticing would-be churners to remain with company.
- The only constraint is interpretability of the model.
- How to further utilise it to take business decison to avoid the customer churn

## APPROACH:
Solving an end to end business problem requres the hypothesis to be tested ,so the strategy I have used is finding the correlating between the variable for getting interaction features after perfroming the initial EDA.
- <img src = https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/Capture.PNG height="400" width="600">
 __Advanced Feature extraction and data visualization in 2-D__:
  <br>Here We will be using PCA for feature selection and understanding the variance in the data and TSNE for visualizing separatibility of the data  
      __Principal Component Analysis__:
              <img src = https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/PCA.PNG height="400" width="600">
      __TSNE__:
              <img src = https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/TSNE.PNG height="400" width="600">
<br>but as features are less so dropping any one of them might prove costly to us as it may hamper the interpretability of the model ,so we must fit all the features in our model for better understanding

## Modelling :
__Logistic Regression__
<br>__Random Forest__ 
<br>__Linear SVM__
 - Hyperparameter tuning GridsearchCV along with L2 Regularization
 <div class="row">
  <div class="column">
    <img src="https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/lr_hp.PNG" alt="Logistic regression Hyperparameter tuning" height="400" width="1000">
  </div>
  <div class="column">
    <img src="https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/rf.PNG" alt="Random Forest Hyperparameter tuning" height="400" width="1000">
</div>
 
## Model evaluation and results 

<br>For our analysis, recall will be our target metric. We care the most about capturing as many true positives (people who are likely to churn) with our model, and we’re less concerned that we may sweep in some false negatives (people who did not churn) along with them.

<img src = https://github.com/yatscool007/Customer-Churn-Prediction/blob/master/results.PNG>
- Logistic Regression perfomed best with best recall score ,though AUC score for random forest is better than the Logistic regression
