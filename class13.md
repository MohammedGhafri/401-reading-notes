# Regression

Regression analysis is one of the most important fields in statistics and machine learning. There are many regression methods available. Linear regression is one of them.

## When Do You Need Regression?

Typically, you need regression to answer whether and how some phenomenon influences the other or how several variables are related. For example, you can use it to determine if and to what extent the experience or gender impact salaries.

## Linear Regression
Linear regression is probably one of the most important and widely used regression techniques. It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.

## Implementing Linear Regression in Python

The package NumPy is a fundamental Python scientific package that allows many high-performance operations on single- and multi-dimensional arrays. It also offers many mathematical routines. Of course, it’s open source.

The package scikit-learn is a widely used Python library for machine learning, built on top of NumPy and some other packages. It provides the means for preprocessing data, reducing dimensionality, implementing regression, classification, clustering, and more. Like NumPy, scikit-learn is also open source.

## There are five basic steps when you’re implementing linear regression:

1. Import the packages and classes you need.
2. Provide data to work with and eventually do appropriate transformations.
3. Create a regression model and fit it with existing data.
4. Check the results of model fitting to know whether the model is satisfactory.
5. Apply the model for predictions.




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



# Conclusion
1. how we can implement it with Python and three open-source packages: NumPy and scikit-learn.
2. You use NumPy for handling arrays.
3. Linear regression is implemented with the following:

    * scikit-learn if you don’t need detailed results and want to use the approach consistent with other regression techniques
    * statsmodels if you need the advanced statistical parameters of a model

    