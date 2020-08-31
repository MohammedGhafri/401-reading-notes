# How to Run Linear Regression in Python

* **Scikit-learn** is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

1. What we import :

- %matplotlib inline
- import numpy
- import pandas
- import matplotlib.pyplot
- import sklearn


## Scikit Learn

WE IMPORT : `from sklearn.linear_model import LinearRegression`

* Fitting a Linear Model : `In [20]: lm.fit(X, bos.PRICE)`

## How to do train-test split:
* You have to divide your data sets randomly.

1. Input: print “Fit a model X_train, and calculate MSE with Y_train:”, np.mean((Y_train – lm.predict(X_train)) ** 2)
2. Output: Fit a model X_train, and calculate MSE with Y_train: 19.5467584735 Fit a model X_train, and calculate MSE with X_test, Y_test: 28.5413672756

### Residual Plots
Residual plots are a good way to visualize the errors in your data. If you have done a good job then your data should be randomly scattered around line zero. If you see structure in your data, that means your model is not capturing some thing.



