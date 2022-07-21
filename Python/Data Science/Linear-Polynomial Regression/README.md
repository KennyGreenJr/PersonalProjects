# Linear Regression with Polynomial Features - International Infection Prediction

## Intro

Enclosed is a Jupyter Notebook for a personal project involving linear regression. The idea is for the reader to gain an understanding of my thought process relatetd to building a statistical model.

I have also included some rudimentary Exploratory Data Analysis within the notebook.

## Problem Statement

Given access to country-wide Covid-19 data, can we predict the number of Covid cases using a country's latitude, longitude, and number of days since outset?

## Approach

I used three features (latitude, longitude, and number of days since outset) to predict the response variable (Covid-19 cases) and split the data into training and testing sets. I implemented multiple linear regression (MLR) to model and fit the data. As expected, the R-squared was low, as latitude and longitude weren't expected to be significant regressors. Next, I implemented polynomial regression, which ultimately added seven additional features. In doing so, I wanted to evaluate higher order polynomials (1 to 20) to see which model fit produced the lowest mean squared error (MSE).

## Result

The 20th order polynomial produced the lowest MSE. However, this model would have a hard time passing any Model Risk group, as the model results indicate poor model fit and better features should've been explored and ultimately selected. 

## Importance

Understanding MLR, and being able to think critically and improve the modeling approach is one of the most important skills in statisical modeling/data science. This project serves as the baseline for all future Data Science/ Machine Learning projects in the PersonalProjects repository.
