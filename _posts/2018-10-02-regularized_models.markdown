---
layout: post
title: "Ridge vs Lasso vs Elastic Net(Regularized Linear Models)!"
date: 2018-10-02 11:32:20 +0300
description: Regularized Regression Models . # Add post description (optional)
img:  # Add image post (optional)
---
## 1. Ridge Regression
It is a regularized version of Linear Regression.  A regularization term equal to $\alpha$ $\sum_{i=1}^n$$\theta_i$ is added to the cost function. This forces the learning algorithm to not only fit the data but also keep the model weights as small as possible.
The hyperparameter $\alpha$  controls how much you want to regularize the model. If $\alpha$  = 0 then Ridge
Regression is just Linear Regression. If $\alpha$  is very large, then all weights end up very close to zero and the result is a flat line going through the data’s mean.
### Ridge Regression cost function
![](/assets/img/ridge_cost_function.png)

Note that the bias term $\theta_0$  is not regularized (the sum starts at i = 1, not 0). If we define w as the vector of feature weights ($\theta_1$  to $\theta_n$  ), then the regularization term is simply equal to 1⁄2(∥ w ∥$_2$ ) $^2$ , where ∥ · ∥ $_2$ represents the [L2 norm](https://www.kaggle.com/residentmario/l1-norms-versus-l2-norms) of the weight vector.


## 2. Lasso Regression
**Least Absolute Shrinkage and Selection Operator Regression** or Lasso Regression is
another regularized version of Linear Regression: just like Ridge Regression, it adds a regularization term to the cost function, but it uses the L1 norm of the weight vector instead of half the square of the L2 norm
###  Lasso Regression cost function
![](/assets/img/Lasso_cost_function.png)

An important characteristic of Lasso Regression is that it tends to completely eliminate the weights of the least important features. In other words, Lasso Regression automatically performs **feature selection** and outputs a **sparse model** (i.e., with few nonzero feature weights).

## 3. Elastic Net
Elastic Net is a middle ground between Ridge Regression and Lasso Regression. The regularization term is a simple mix of both Ridge and Lasso’s regularization terms, and you can control the mix ratio r. When r = 0, Elastic Net is equivalent to Ridge Regression, and when r = 1, it is equivalent to Lasso Regression.

### Elastic Net cost function
![](/assets/img/Elastic_Net_cost_function.png)
## So when should we use Ridge, Lasso, or Elastic Net?
Ridge is a good default, but if you suspect that only a few features are actually useful, you should prefer Lasso or Elastic Net since they tend to reduce the useless features’ weights down to zero as we have discussed. In general, Elastic Net is preferred over Lasso since Lasso may behave erratically when the number of features is greater than the number of training instances or when several features are strongly correlated.
