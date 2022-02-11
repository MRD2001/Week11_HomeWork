# Week11_HomeWork
Machine Learning Models To predict credit risk

## Background

> Auto loans, mortgages, student loans, debt consolidation ... these are just a few examples of credit and loans that people are seeking online. Peer-to-peer lending services such as LendingClub, Plenty or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk, so we have been asked by a client to help them use machine learning techniques to predict credit risk.

> In this assignment, we will build and evaluate several machine-learning models to predict credit risk using free data from LendingClub. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so we will need to employ different techniques for training and evaluating models with imbalanced classes. We  will use the **imbalanced-learn** and **Scikit-learn** libraries to build and evaluate models using the two techniques of **Resampling** and **Ensamble Learning**

> The assignmnet includes two notebooks under the Starter_Code directory 1. credit_risk_resampling.ipynb and 2. credit_risk_ensamble.ipynb. The source data is a CSV file exist in Resources directory Lending_data.csv


## Libraries Imported and Packages

- numpy : the fundamental package for scientific computing with Python
- pandas : open source data analysis and manipulation tool 
- pathlib : provides classes representing file system paths with sementics for all operating systems
- Collections : built-in python module that implements specialised container data types as alternative to dict, list, set 
- sklearn.metrics : simple tool for predictive data analysis. metrics module provides loss, score, and utility functions to measure classificaiton performance
- imblearn.metrics : toolbox for imbalanced dataset in machine learning

## Resampling

- Oversample the data using the Naive Random Oversampler and SMOTE algorithms.
- Undersample the data using the Cluster Centroids algorithm
- Oversample and undersample the data using the SMOTEENN algorithim.
- Generate the Balance Accuracy Score, Confusion Matrix and Classification Report for all of the above methods.

### Classification Analysis - Resampling

- Train a logistic regression classifier from sklearn.linear_model using the resampled data.
- Calculate the balanced accuracy score from sklearn.metrics.
- Calculate the confusion matrix from sklearn.metrics.
- Print the imbalanced classification report from imblearn.metrics.

## Ensamble Learning


> In this section, we will train and compare two different ensemble classifiers to predict loan risk and evaluate each model. We will use the balanced random forest classifier and the easy ensemble AdaBoost classifier.

> The following are completed for the each model: 

- Train the model using the quarterly data from LendingClub provided in the Resource folder.
- Calculate the balanced accuracy score from sklearn.metrics.
- Print the confusion matrix from sklearn.metrics.
- Generate a classification report using the imbalanced_classification_report from imbalanced learn.
- For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

> We used the above to answer the provided questions:

- Which model had the best balanced accuracy score?
The balanced accuracy in binary and multiclass classification problems to deal with imbalanced datasets. It is defined as the average of recall obtained on each class. The best balaned accuracy score is 0.7885466545953005 , and then 0.933852541007141 (which is closer to 1 produced by the Easy ensemble classifier.

- Which model had the best recall score?
The recall score is The recall is the ratio tp / (tp + fn) where tp is the number of true positives and fn the number of false negatives. The recall is intuitively the ability of the classifier to find all the positive samples. The best value is 1 and the worst value is 0.The easy ensamble classification model produced recall score of 0.95 which is better than 0.87 produced by the Balanced random forest classifier

- Which model had the best geometric mean score?
The geometric mean is the average rate of return of a set of values calculated using the products of the terms.For volatile numbers, the geometric average provides a far more accurate measurement of the true return by taking into account year-over-year compounding that smooths the average.In this case Easy ensamble model had the best score of 0.93.

- What are the top three features?
The top three features are total_rec_prncp, total_pymnt, and total_pymnt_inv

