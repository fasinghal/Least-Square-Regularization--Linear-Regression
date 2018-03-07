# Least-Square-Regularization-Linear-Regression
CS 6301 R for data Scientists- Lasso and Ridge Regularization with Gradient Descent for linear regression

Problem Setup
Recall the linear regression problem: Suppose we are given a training set { X, yi } where the
response variable yi is now numeric and X is a vector of predictors
Our first assumption is that y is some function of the predictors, and perhaps a noise component
(which we assume is normally distributed with zero mean and constant variance): y = f(X) + e
Our goal is to find an approximation to f(), which we will assume has a linear form for f(X).

Gradient Descent
We can use the gradient of the cost
function to try to find values for the betas
that will minimize the cost function …
Algorithm: Start with an initial guess for the
betas, move in the direction of the negative
gradient, update our guess of the betas,
repeat until convergence (gradient descent)
Alternative: Set the partial derivatives equal
to zero and solve! (These are the normal
equations.)

Regularization
Regularization puts constraints
on betas …
◦ Essentially will “select” the most
important ones
Notice this limits how large the
betas can get
Two popular choices are q = 1
(Lasso) and q = 2 (Ridge)

Regularization
Regularization will limit the betas in a situation when there are many
variables
By adding the penalty term to the cost function, the betas are forced
to be small
◦ It essentially shrinks the “non-important” features
Lasso vs. Ridge:
◦ Ridge will keep all variables (betas), but the more important ones will be larger
(in magnitude) than the less important ones
◦ Lasso will set the less important betas to zero and keep the best ones
