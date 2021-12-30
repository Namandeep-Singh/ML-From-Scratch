# ML-From-Scratch

#LINEAR REGRESSION

1 Write a function to generate an m+1 dimensional data set, of size n, consisting of m continuous independent
variables (X) and one dependent variable (Y) defined as
yi = xiβ + e
where,
• e is a Gaussuan distribution with mean 0 and standard deviation (σ), representing the unexplained
variation in Y
• β is a random vector of dimensionality m + 1, representing the coefficients of the linear relationship
between X and Y, and
• ∀i ∈ [1, n], xi0 = 1
The function should take the following parameters:
• σ: The spread of noise in the output variable
• n: The size of the data set
• m: The number of indepedent variables
Output from the function should be:
• X: An n × m numpy array of independent variable values (with a 1 in the first column)
• Y : The n × 1 numpy array of output values
• β: The random coefficients used to generatre Y from X
2 Write a function that learns the parameters of a linear regression line given inputs
• X: An n × m numpy array of independent variable values
• Y : The n × 1 numpy array of output values
• k: the number of iteractions (epochs)
• τ : the threshold on change in Cost function value from the previous to current iteration
The function should implement the Gradient Descent algorithm as discussed in class that initialises β with
random values and then updates these values in each iteraction by moving in the the direction defined by
the partial derivative of the cost function with respect to each of the coefficients. The function should use
only one loop that ends after a number of iterations (k) or a threshold on the change in cost function value
(τ ).
The output should be an m + 1 dimensional vector of coefficients and the final cost function value.


#LOGISTIC REGRESSION

1 Write a function to generate an m+1 dimensional data set, of size n, consisting of m continuous independent
variables (X) and one dependent binary variable (Y) defined as
Y =
{ 1 if p(y = 1|~x) = 1
1+exp−~x.~β > 0.5
0 otherwise
where,
• β is a random vector of dimensionality m + 1, representing the coefficients of the linear relationship
between X and Y, and
• ∀i ∈ [1, n], xi0 = 1
To add noise to the labels (Y) generated, we assume a Bernoulli distribution with probability of success, θ,
that determines whether or not the label generated, as above, is to be flipped. The larger the value of θ, the
greater is the noise.
The function should take the following parameters:
• θ: The probability of flipping the label, Y
• n: The size of the data set
• m: The number of indepedent variables
Output from the function should be:
• X: An n × m numpy array of independent variable values (with a 1 in the first column)
• Y : The n × 1 binary numpy array of output values
• β: The random coefficients used to generate Y from X
2 Write a function that learns the parameters of a logistic regression function given inputs
• X: An n × m numpy array of independent variable values
• Y : The n × 1 binary numpy array of output values
• k: the number of iteractions (epochs)
• τ : the threshold on change in Cost function value from the previous to current iteration
• λ: the learning rate for Gradient Descent
The function should implement the Gradient Descent algorithm as discussed in class that initialises β with
random values and then updates these values in each iteraction by moving in the the direction defined by
the partial derivative of the cost function with respect to each of the coefficients. The function should use
only one loop that ends after a number of iterations (k) or a threshold on the change in cost function value
(τ ).
The output should be a m + 1 dimensional vector of coefficients and the final cost function value.
Add L1 and L2 regularization to the Logistic Regression cost function. How does this impact the models
learnt? How does the choice of regularization constant impact the β vector learned?


