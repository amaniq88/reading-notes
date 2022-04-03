# Linear Regressions
Linear regression is a linear model, e.g. a model that assumes a linear relationship between the input variables (x) and the single output variable (y).

![image](https://user-images.githubusercontent.com/97660877/161411190-505b4bd4-0afe-4ec8-b8ea-2b4f0b4485e5.png)

Scikit-learn is a powerful Python module for machine learning. 
It contains function for regression, classification, clustering, model selection and dimensionality reduction.
## Steps :
1- import the required Python libraries into Ipython Notebook.
2- import the  data set into Ipython notebook and store it in a variable.
3- convert boston.data into a pandas data frame.
4- convert the  column names from  numbers, to the feature names.

### Scikit Learn
will use the linear regression model and predict  the data prices. 
will use the least squares method as the way to estimate the coefficients.

Y = boston housing price(also called “target” data in Python)

and

X = all the other features (or independent variables)

First, import linear regression from sci-kit learn module. 
Then drop the price column as we want only the parameters as my X values. 
will  store linear regression object in a variable called lm.
If we want to look inside the linear regression object, we can do so by typing LinearRegression. 
and the press <tab> key. This will give a list of functions available inside linear regression object.
  
  ![image](https://user-images.githubusercontent.com/97660877/161411839-19155dcc-b3cf-484a-bc59-a45cc7db3f66.png)

**important functions to keep in mind while fitting a linear regression model are:**

lm.fit() -> fits a linear model

lm.predict() -> Predict Y using the linear model with estimated coefficients

lm.score() -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, 
  as the proportion of total variation of outcomes explained by the model.

we can also explore the functions inside lm object by pressing lm.<tab>
 .coef_ gives the coefficients and .intercept_ gives the estimated intercepts.


  
