# Modeling Summary

In this section, I present briefly the process of feature engineering prior to machine learning, and the modeling process itself.

## Feature Engineering

- Price sensitivity is a notion that doesn't exist yet in out clients dataset, but since we had the historical prices for last year, we can think of different ways to calculates.
- The way I was is that, from the exploratory phase, we saw that prices were different on average for churned and non-churned customers, so I thought about including this information about central tendancy, and the variation of prices for each client.
- The mean was calculated for each client by averaging prices across months, and the variation was simply the difference in price between December and January of last year.
- Besides price sensitivity, categories with few observations were grouped together for reducing the complexity of the data and the risk of overfitting.
- The final step was dropping the old columns, columns with high correlations, and columns with weak associations with the target variable (churn).

## Modeling

Now In the modeling part, we are dealing with a binary classification problem, which is predicting whether a customer will churn or not.  
The right metric to use here is the F1 score, which is the harmonic mean of precision and recall, and here's why:

- We are more interested in getting the right customers that are going to churn, because that's the main goal of the project, in order to take the right actions to prevent them from churning, and achieve high retention rates, this is done through maximizing recall.
- The actions we are going to take are going to cost money, so we want to make sure that we are taking these actions with the right people, and not wasting money on customers that are not going to churn, this is done through maximizing precision.
- What better metric to use than the harmonic mean of both precision and recall, which is the F1 score.

Here's how I made sure the model's performance is good:

- We had to establish a baseline, and try to beat it with more sophisticated technics, or otherwise this problem isn't worth spending all the resources and money.
- The baseline was a random classifier, with a 10% chance of predicting a customer to churn, which is the percentage of churned customers in the dataset.
- Such a baseline would give the following results:
  - Precision: 10%
  - Recall: 10%
  - F1 score: 10%
- We had to perform some data preprocessing prior to modeling, we used one hot encoding for categorical features and standardization for numerical ones. We did this through pipelines, which are a great way to automate this process each time we make a change in the model or select different set of features.
- Our first model was a logistic regression, which was chosen because it's a simple model that assumes linearity between the features and the target. Its performance was worst than the random baseline, and couldn't even learn from the traning data.
- Because of this complexity in the data, we had to move to a model that can capture non-linear relationships, we proceeded with the decision tree model.
  - The model was able to learn and overfit the training data. Changing the depth of the tree, and the minimum number of samples per and class weights helped reduce the overfitting.
  - Precision: 20%
  - Recall: 24%
  - F1 score: 22%
- The problem with the decision tree is that even after tuning hyperparameters, there was a gap between training and testing performances. To address this problem, we tried the random forest model.
  - The model was able to learn and generalize well, and the gap between training and testing performances was reduced.
  - Precision: 20%
  - Recall: 30%
  - F1 score: 25%
- This final model was also fast during training and prediction, we had to use it to see what impact it could have on the business.
