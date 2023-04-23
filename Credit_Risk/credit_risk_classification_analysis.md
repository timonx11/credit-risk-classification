# Module 20 Report Analysis

## Purpose of the analysis.
Purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. 
## Explain what financial information the data was on, and what you needed to predict.
We'll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
We'll classiying it to 2 category which are Healthy loans (low-risk) categorized as `0` and Non Healthy loans (high-risk) categorized as `1`
## Details Information about the variables we use and we are trying to predict.
* Using the dataset provided, we created label set (y) from the "loan_status" Column and then created the features (x) from the remaining columns in the Dataset/frame.

* Then I created a Logistic Regression Model, which in this case gives us an accuracy score of 99%. 
* Although the model generated a high-accuracy, the models recall value (0.89) for non-healthy loans (1) is lower than the recall value (1) for healthy loans(0). 
* This shows us that the model will predict loan status's as healthy better than being able to predict loan status's as non-healthy. 
* This could be beacause of the dataset is not balanced, meaning that most of the data belongs to one category (in this case, the data shows that the healthy loans greatly outweighed non-healthy loans). 

* This can be seen (on the code) by using the <b>"value_counts function"</b>, we are able to see that the data is highly imbalanced. Marked by the number of healthy loans `0` , 75036 entry and non-healthy loans `1` , 2500 entry

* And to strenghten that analysis, we can also see on the confusion matrix code that:
   * Out of the 18,759 loan status's that are healthy (low-risk), the model predicted 18,679 as healthy correctly (True Positive) and 80 as healthy incorrectly (False Positive).
   * Out of the 625 loan status's that are non-healthy (high-risk), the model predicted 558 as non-healthy correctly (True Negative) and 67 as non-healthy incorrectly (False Negative).

* Based on above results, To generate a higher accuracy score and see how the model handles non healthy loans (high-risk), we can oversample the data using the RandomOverSampler module from the imblearn library, which will adds more copies of the non-healthy loans (minority) to obtain a balanced dataset.

* After resampled the training data, I created another Logistic Regression Model to fit with the oversampled data, And that generated an accuracy score of 100%, which turns out to be higher than the model fitted with the non balance / original data. The oversampled model performs better due to the dataset being balanced. The non-healthy (high-risk) loans recall value increased from 0.89 to 1 indicating that the model does much better job in identifying non-healthy (high-risk) loans as well as healthy (low-risk). 

* Confusion matrix on the oversampled data as below:
   * Out of the 18,759 loan status's that are healthy (low-risk), the model predicted 18,668 as healthy correctly (True Positive) and 91 as healthy incorrectly (False Positive).
   * Out of the 625 loan status's that are non-healthy (high-risk), the model predicted 623 as non-healthy correctly (True Negative) and 2 as non-healthy incorrectly (False Negative).

## Results
* Machine Learning Model 1: (Logistic Regression)
  * Description of Model 1 Accuracy give us result of (0.99) / 99%,
  * Precision of 1 for healthy loans and 0.87 for non healthy loans,
  * and Recall scores of 1 for healthy loans and 0.89 for non healthy loans.
  * f1-score also give us 1 as the result of healthy loans and 0.88 for non healthy loans.


* Machine Learning Model 2: (Oversampler)
  * Description of Model 1 Accuracy give us result of (1) / 100%,
  * Precision of 1 for healthy loans and 0.87 for non healthy loans,
  * and Recall scores of 1 for healthy loans and 1 for non healthy loans.
  * f1-score also give us 1 as the result of healthy loans and 0.93 for non healthy loans.

## Summary
* Both models seems capable to predict high level of accuracy, with the second model (oversampled data) slightly performs better.
* Lending company most likely want a model that can predict healthy loans and non-healthy loans as accurate / close to accurate as possible most of the time because if theres a lot of healthy loan application being marked as healthy, it will be a huge loss to the lending company as the lender might not able to paid it back.
* And based on points above, I would recommend using Model 2 (Logistic Regression Model fit with (oversampled) data.
