# Regression
## Basic concept:
* features(x): independent variables can be categorical or continuous
* response(y): dependent variable should b continuous, can't be a discrete value.
* Type of regression:
1. simple linear regression: one independent variable
2. Multiple linear regression: more than one independent variable

## Simple Linear Regression
* representation: y=b+ ax
  * a: slop
  * b: intercept
* Evaluation Metrics 
 * MSE(mean squared error): the focus is geared more towards large errors
<img width="142" alt="Screen Shot 2019-04-22 at 4 38 33 PM" src="https://user-images.githubusercontent.com/27160394/56528401-1f97a680-651d-11e9-8c6e-5a6e8d58365c.png">
 * MAE(mean average error)
 * RMSE(root mean squared error)
 * RAE(relative absolute error)
 * RSE(relative squared error)
 * R^2(1-RSE):how close the data values are, to the fitted regression line.

* Model evaluation
1. train/test dataset split: K-fold cross-validation
2. train test on same dataset: lead to overfitting

* Estimating the parameters(coefficients): minimize the MSE
 1. Least squares estimation
<img width="639" alt="Screen Shot 2019-04-22 at 4 57 36 PM" src="https://user-images.githubusercontent.com/27160394/56530067-ce3ce680-651f-11e9-949a-eb4baa4b6b92.png">


* Prons and cons
1. Very fast
2. no parameter tuning
3. Highly interpretable
  
## Multiple Linear Regression
* Applications for multiple linear regression
1. Identify the strength of the effect that the independent variables have on the dependent variable
2. predict how the dependent variable changes when we change the independent variables
* representation: y=b+ ax
