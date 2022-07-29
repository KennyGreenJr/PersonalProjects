# Fitting models with Gradient Descent, Normal Equations, Regularized Normal Equations, Generalized Linear Models (GLM), and Random Forests

## Intro

Enclosed is a Jupyter Notebook for a personal project featuring some advanced topics of regression analysis. The idea is for the reader to gain an understanding of my thought process of fitting a model, and more specifically how I design models when predicting Tesla car sales to ensure inventory meets demand. 

I have also included some very rudimentary Exploratory Data Analysis within the notebook.

## Problem Statement

Given access to 2019 California-state data for Tesla car sales for quarters one and two, can we predict the number of car sales for quarters three and four.

## Approach

The first step was to clean the data to see how many unique car models we had in the training data. It was noted to be 66. The test set had 73, so this led me to assume that new models were introduced in quarters three and four.

I first implemented a linear model with gradient descent (GD) where hyperparameters were set for the learning rate and max iterations (0.001 and 1000), respectively.  A hypothesis and loss function were created before the stochastic gradient descent function was calculated. The R-squared was 63%, and MSE was 5702. Despite GD being an iterative method for converging quickly, the thesis was that a better model could be developed.

Next, I implemented Normal Equations, which is an approach used to compute the solution directly. The model producted a slightly smaller R-squared (59.8%), and slightly larger MSE.

Next, I implemented Regularized Normal Equations. Given that X_train has 66 rows and 73 columns (wider than it is tall), the data suggests that this approach might perform better. Theta was computed using Numpy's linalg function. Also used from Numpy was the linspace funciton to set regularization parameters from 0.001 to 0.01. The R-squared and MSE was computed over 10 intervals and the best model produced a R-squared of 63%.

The second to last approach used was GLM. I used the statsmodels package and assumed the prediction errors belonged to the Gaussian family. I noticed that the Normal Equations and GLM approach result in the same RMSE and R-squared. This is because when we use the Gaussian model for the error, GLM is considered linear regression.

Last, Random Forests, a non-linear approach, was implemented. The relevant parameters are max_depth and the random_state (so that our code will always yield the same results). This model yieled a R-squared of 72% and MSE of 4308.

## Result

When comparing the models, the Random Forests method resulted in the highest R-squared/lowest MSE.

## Importance

Having a diverse toolkit of machine learning algorithms to utilize and implement is essential for any Data Scientist in the modern era. As we saw, we fit both linear and non-linear algorithims. In the end, it is up to the Data Scientist to best understand their data and know if an approach is more logical to use over others.

