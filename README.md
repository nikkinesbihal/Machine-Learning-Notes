# Machine-Learning-Notes
Coursera Machine Learning Course 2017

INTRODUCTION

Maching Learning - 
  Arthur Samuel: the field of study that gives computers the ability to learn without being explicitly programmed
  Tom Mitchell: A computer program is said to learn from experience, E, with respect to some task, T, and some performance       measure, P, if its performance on T as measured by P imporoves with experience E.

Supervised Learning - we are given a data set and already know what pur correct output should look like, having the idea that   there is a relationship between the input and output
Regression Problem - trying to predict a continuous value output
Classification Problem - trying to predict a discrete value output

Unsupervised Learning - little or no idea what our results should look lik.  We can derive structure from data where we don't   necessarily know the efect of the variables. There is no feedback based on prediction results
Clustering Algorithm - sub segments of data, structured by algorithm


LINEAR REGRESSION WITH ONE VARIABLE

Model and Cost Function

m - number of training examples
x - input variable; feature
y - output variable; target variable
(x^i, y^i) - ith training example
h - hypothesis; output function of a supervised learning algorithm that maps from x's to y's
hsubtheta(x)=thetasub0 + thetasub1 * x  - Linear Regression
The Cost Function measures the accuracy of our hypothesis
thetasub0 and thetasubone are parameter values we choose to stabilize parameters
J(thetasub0, thetasub1) = 1/2m sigma(h(x)-y)^2 ; i=1, m on sigma
The best possible line will be such so that the average squared vertical distances of the scattered points fron the line will be the least
If you plot y=J(theta) and x=thetasub1, the minimum is the slope of the ideal like (thetasub1)

Parameter Learning

Gradient Descent helps us estimate the parameters of our hypothesis function
Imagine stepping down from peak on contour plot; each step goes in the direction on steepest descent until reaching a minimum
  alpha - the size of each step; Learning Rate; too small: slow convergence too large: divergence or failure to converge
Gradient Descent - thetasubj := thetasubj - alpha * partial deriv(J(thetasub0,thetasub1)) with resp.to thetasubj j is the       feature index number
At each j interation, one should simultaneously update all theta parameter
Combining gradient descent with the cost function will give an algorithm for linear regression
  partial w/ respect to thetasubj 1/2m sigma (thetasub0 + thetasub1 * x^i - y^i)^2
j=0: partial(J) = 1/m sigma (hsubtheta * (x^i) - y^i)
j=1: partial(J) =1/m sigma (hsubtheta * (x^i) - y^i) * x^i
"Batch" Gradient Descent - each step of gradient descent uses all the training examples

LINEAR ALGEBRA REVIEW
