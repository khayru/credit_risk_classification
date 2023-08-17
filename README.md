 Credit_risk_classification
 ## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  The purpose of this analysis is to create and evaluate the accuracy of  the data model that produces
  
* Explain what financial information the data was on, and what you needed to predict.
  The data set information is about loan-healthy (low-rick) or non-healthy(high-risk)
  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* 
* Describe the stages of the machine learning process you went through as part of this analysis.
* 
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    
1- according to the machine learning model, I got the results 
2- The accuracy score for this model is -------

* The precision score for this model is
*   the classification report for the model
logistic_classreport = classification_report(y_test, prediction_testing)
print(logistic_classreport)
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

    accuracy                           0.99     19384
   macro avg       0.94      0.94      0.94     19384
weighted avg       0.99      0.99      0.99     19384



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  
Based on the precision or I think this will be a good  model to put into practice because the score is 0.9 accuracy is a good score.
If you do not recommend any of the models, please justify your reasoning.
I don't think this model can be predicted for the model because the accuracy score of 80%that means every  100 people get 20 mis labels this creates a lot of lost
test scores the one very summary of the training score.
