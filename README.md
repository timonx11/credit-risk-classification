# Credit-risk-classification
## Tim N - Module 20 Challenge
### PLEASE NOTE: ALL CODE AND ANALYSIS REPORT ARE STORED ON THE "credit-risk-classification" Folder. credit-risk-classification.ipynb for the code and "credit-risk-classification-report" for the Written Analysis.

## Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

##Before You Begin
Create a new repository for this project called credit-risk-classification. Do not add this homework to an existing repository.
Clone the new repository to your computer.
Inside your credit-risk-classification repository, create a folder titled "Credit_Risk."
Inside the "Credit_Risk" folder, add the credit_risk_classification.ipynb and lending_data.csv files found in the "Starter_Code.zip" file.

Push your changes to GitHub.

## Files
Download the Started_code files to help you get started:

## Instructions
### The instructions for this Challenge are divided into the following subsections:
Split the Data into Training and Testing Sets
Create a Logistic Regression Model with the Original Data
Predict a Logistic Regression Model with Resampled Training Data
Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:
Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

### NOTE
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
Split the data into training and testing datasets by using train_test_split.
Create a Logistic Regression Model with the Original Data

### Use your knowledge of logistic regression to complete the following steps:
Fit a logistic regression model by using the training data (X_train and y_train).
Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
Evaluate the model’s performance by doing the following:
    Calculate the accuracy score of the model.
    Generate a confusion matrix.
    Print the classification report.
Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip
