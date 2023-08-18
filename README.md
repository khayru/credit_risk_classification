 Credit_risk_classification
 ## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  The purpose of this analysis is to predict users will be at high-risk for loans.
  
* Explain what financial information the data was on, and what you needed to predict.
  For the dataset landing_csv, I created a logistic regression model with Resampled data. oversample  model generated the accuracy of a 100% score
  for(low-risk)loans.

  ## Results
* Describe the stages of the machine learning process you went through as part of this analysis.
* Check the value_counts from the dataset. we see the result unbalanced it shows more healthy loans [0] than the low value showing me a non-healthy loan[1]
* 
# Check the balance of our target values
y.value_counts()
0    75036
1     2500
Name: loan_status, dtype: int64

Calculate the accuracy score of the model was 94%
logistic_score = balanced_accuracy_score(y_test, prediction_testing)
print(logistic_score)
0.9442676901753825

Calculate the accuracy score of the model.
# Generate a confusion matrix for the model
logistic_matrix = confusion_matrix(y_test, prediction_testing)
print(logistic_matrix)
[[18679    80]
 [   67   558]]
 
 The result of unbalanced data
 80 False Positive 
 67 False Negative
 
According to the confusing matrix result, after splitting the data into training and testing  using the value_count. I used the model RandomoverSample to test the split data. I found out that it is reading the unhealthy loans as healthy.
 
# Count the distinct values of the resampled labels data
y_over.value_counts()
1    56277
0    56277
Name: loan_status, dtype: int64

# Print the balanced_accuracy score of the model 
predicted_score = balanced_accuracy_score(y_test, predictions)
print(predicted_score)
0.9959744975744975

It is giving me 99% balance of healthy loans. The accuracy is 100%. This is showing that the model is perfect for healthy loans. 

# Generate a confusion matrix for the model
predicted_matrix = confusion_matrix(y_test, predictions)
print(predicted_matrix)
[[18668    91]
 [    2   623]]
 
 The result from Balanse data
 91 False Positive 
 2 False Negative

 
# Print the classification report for the model
predicted_classreport = classification_report(y_test, predictions)
print(predicted_classreport)
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      1.00      0.93       625

    accuracy                           1.00     19384
   macro avg       0.94      1.00      0.96     19384
weighted avg       1.00      1.00      1.00     19384

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
  
Based on the logistic Regration model, I think this will be a good  model to put into practice because there is 100% accuracy and the balance is 99%. While it can still predict false positives and false negatives, the chances of this are very low.

