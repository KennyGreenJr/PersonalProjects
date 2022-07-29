# Regression with Gradient Descent, Normal Equations, Regularized Normal Equations, Generalized Linear Models (GLM), and Random Forest Regression

## Intro

Enclosed is a Jupyter Notebook for a personal project featuring some advanced topics of regression analysis. The idea is for the reader to gain an understanding of my thought process of building a statistical model, and more specifically to look at how I design models when predicting Tesla car sales to ensure inventory meets demand. 

I have also included some very rudimentary Exploratory Data Analysis within the notebook.

## Problem Statement

Given access to 2019 California-state data for Tesla car sales for quarters one and two, can we predict the number of car sales for quarters three and four.

## Approach

The first step was to clean the data to see how many unique mnodels we had in the training data. It was noted to be 66. The test set had 73, so this led me to assume that new models were introduced in quarters three and four.

I first implemented a linear model with gradient descent (GD) where hyperparameters were set for the learning rate and max iterations (0.001 and 1000), respectively.  A hypothesis and loss function were created before the stochastic gradient descent function was calculated. The R-squared was 63%, and MSE was 5702. Despite GD being an iterative method for converging quickly, the thesis was that a better model could be developed.

Next, I implemented Normal Equations, which is an approach used to compute the solution directly. The model producted a slightly smaller R-squared (59.8%), and slightly larger MSE.

Next, I implemented Regularized Normal Equations. Given that X_train has 66 rows and 73 columns (wider than it is tall), the data suggests that this approach might perform better. Theta was computed using Numpy's linalg function. Also used in Numpy was the linspace funciton to set regularization parameters from 0.01 to 0.01. The R-squared and MSE was computed over 10 intervals and the best model produced a R-squared of 63%.

The second to last approach used was GLM. I used the statsmodels package and assumed the prediction errors belonged to the Gaussian family. I noticed that the Normal Equations and GLM approach result in the same RMSE and R-squared. This is because when we use the Gaussian model for the error, GLM is considered linear regression.


## Result

The 20th order polynomial produced the lowest MSE. However, this model would have a hard time passing any Model Risk group, as the model results indicate poor model fit and better features should've been explored and ultimately selected. 

## Importance

Understanding MLR, and being able to think critically and improve the modeling approach is one of the most important skills in statisical modeling/data science. This project serves as the baseline for all future Data Science/ Machine Learning projects in the PersonalProjects repository.

