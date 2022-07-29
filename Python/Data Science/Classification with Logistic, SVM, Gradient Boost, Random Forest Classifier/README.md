# Purchase Prediction with Classification

## Intro

Enclosed is a Jupyter Notebook for a personal project involving classification. The idea is for the reader to gain an understanding of my thought process relatetd to fitting a classification model using Logistic Regression, Support Vector Machine, Gradient Boost, and Random Forests.

I have also included some rudimentary Exploratory Data Analysis within the notebook, including converting object data types to floats and balance checking the data before modeling. 

## Problem Statement

Given access to WalMart Corporation's data, can we predict whether or not a customer will make a purchase.

## Approach

After exploring and manipulating the data, it was identified that the data is unbalanced. This is worth noting, as automatically adjudting weights inversely proportional to the class frequencies is essential to the modeling data. Feature selection was completed, and it was determined that number of views and number in cart are important features. A logistic regression model was first fitted, followed by a support vector machine (SVM) model. The SVM model produced a better accuracy and F-1 scores. Next, a Gradient Boosted Trees model was fit and its accuracy is comparable to that of the SVM model. Last, a Random Forest Classifier was fitted and this model produced the lowest F1 score but a comparable accuracy.

## Result

As it relates to accuracy, all models are comparable but the SVM model edges out the other three. In addition, accuracy is used when True Positives and True Negatives are more important, whereas the F1 metric is a better metric when there are unbalanced classes.
