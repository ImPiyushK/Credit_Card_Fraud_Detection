# Credit Card Fraud Detection
This repository contains a machine learning project for predicting whether a Credit Card Transaction is Fraud or Valid.

![Display Image](./Rawdata/cap1.jpg)

## Problem Description
Credit card companies should be to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase. We will use various predictive models to see how accurate they are in detecting whether a transaction is a normal payment or a fraud. As described in the dataset, the features are scaled and the names of the features are not shown due to privacy reasons. Nevertheless, we can still analyze some important aspects of the dataset. 


## File Description

* Credit_Card_Fraud_Detection.ipynb - Jupyter Notebook which contains python code for predicting Fraud Transactions.<br>
* credit_card_fraud_detection.py - Python code for predicting model.<br>
* Dataset- contains training and testing data.<br>
  * creditcard.csv - Training & Testing Data
* readme.md - for guide to this project.<br>

## Project Description
We will use various Machine Learning Models to see how accurate they are in detecting whether a transaction is Valid or a Fraud and find which model gives best accuracy for implementing on Test Data.
The Credit Card Fraud detection Dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset present transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

The dataset has been collected and analyzed during a research collaboration of Worldline and the [Machine Learning Group](http://mlg.ulb.ac.be) of ULB(Université Libre de Bruxelles) on big data mining and fraud detection.

Since the data is highly unbalanced I have used the Confusion Matrix to find out the how the model is working. After using different models including Random Forest, Logistic Regression, Decision Tree, SVM and found out that the best suited model is the RandomForestClassifier.

## ExploratoryData Analysis
Correlation Matrix between different features of the dataset
![features](./Rawdata/cap3.png)

## Algorithm Performance
I have used four classification algorithms namely Logistic Regression , Random Forest, SVM and Decision Tree. I have split the data into training and test set at a ratio of 70:30.
| Model  | Accuracy Score | Precision Score |
| --- | --- | --- |
| Random Forest | 0.9996 | 0.9666 |
| Logistic Regression | 0.9991 | 0.8396 |
| SVM | 0.9983 | 0.8132  |
| Decision Tree | 0.9992 | 0.7671 |

## Result
I have used F1 Score, Recall, Precision, Average score and Confusion Matrix as metrics to evaluate the classifiers as they give a better indication of the model compared to only accuracy. The Random Forest gives the best Recall score on the original dataset among the four algorithms.

> Classification report of Random Forest 
```
Classification Report:
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     85302
           1       0.97      0.82      0.89       141

    accuracy                           1.00     85443
   macro avg       0.98      0.91      0.94     85443
weighted avg       1.00      1.00      1.00     85443
```

> Confusion Matrix of Random Forest

![confusion matrix](./Rawdata/cap2.png)
