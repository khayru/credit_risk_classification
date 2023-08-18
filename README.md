 Credit_risk_classification
 ## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  The purpose of this analysis is to predict users will be at high-risk for loans.
  
* Explain what financial information the data was on, and what you needed to predict.
  For the dataset landing_csv, I created a logistic regression model with Resampled data. oversample  model generated the accuracy of a 100% score
  for(low-rick)loans.
# Check the balance of our target values
y.value_counts()


  ## Results
* Describe the stages of the machine learning process you went through as part of this analysis.
 # Check the balance of our target values
y.value_counts()
0    75036
1    75036
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
   method uses LogisticRegression

# Print the balanced_accuracy score of the model 
predicted_score = balanced_accuracy_score(y_test, predictions)
print(predicted_score)
0.9959744975744975
# Generate a confusion matrix for the model
predicted_matrix = confusion_matrix(y_test, predictions)
print(predicted_matrix)

# Print the classification report for the model
predicted_classreport = classification_report(y_test, predictions)
print(predicted_classreport)
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      1.00      0.93       625

    accuracy                           1.00     19384
   macro avg       0.94      1.00      0.96     19384
weighted avg       1.00      1.00      1.00     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  
Based on the precision I think this will be a good  model to put into practice because the score is 100% accuracy is a good score and the balance is 99%.
