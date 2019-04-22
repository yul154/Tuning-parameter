# Regression
## Basic concept:
* features(x): independent variables can be categorical or continuous
* response(y): dependent variable should b continuous, can't be a discrete value.
* Type of regression:
1. simple linear regression: one independent variable
2. Multiple linear regression: more than one independent variable

## Simple Linear Regression
### Representation: y=b+ ax
  * a: slop
  * b: intercept
### Evaluation Metrics 
* MSE(mean squared error): the focus is geared more towards large errors
<img width="142" alt="Screen Shot 2019-04-22 at 4 38 33 PM" src="https://user-images.githubusercontent.com/27160394/56528401-1f97a680-651d-11e9-8c6e-5a6e8d58365c.png">
* MAE(mean average error)
* RMSE(root mean squared error)
* RAE(relative absolute error)
* RSE(relative squared error)
* R^2(1-RSE):how close the data values are, to the fitted regression line.

### Model evaluation
1. train/test dataset split: K-fold cross-validation
2. train test on same dataset: lead to overfitting

### Estimating the parameters(coefficients): minimize the MSE
1. Least squares estimation
<img width="639" alt="Screen Shot 2019-04-22 at 4 57 36 PM" src="https://user-images.githubusercontent.com/27160394/56530067-ce3ce680-651f-11e9-949a-eb4baa4b6b92.png">
2. Gradient descent

### Prons and cons
1. Very fast
2. no parameter tuning
3. Highly interpretable
  
## Multiple Linear Regression
### Applications for multiple linear regression
1. Identify the strength of the effect that the independent variables have on the dependent variable
2. predict how the dependent variable changes when we change the independent variables
### representation:
<img width="270" alt="Screen Shot 2019-04-22 at 5 31 38 PM" src="https://user-images.githubusercontent.com/27160394/56532861-97b59a80-6524-11e9-9c82-3e66a95e45a6.png">
### Optimized parameters 
* Ordinary Least Squares: take a long time to calculate if dataset is large
* Optimization algorithm:use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data
 1. gradient descent: proper approach if dataset is large
 
## Non-Linear Regression（polynomial）
> the relationship between the independent variable X and the dependent variable Y is modeled as an Nth degree polynomial in X
### representation： 
 
 
