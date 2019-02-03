##Linear Regression Models



Here are some materials I found interesting and compiled at the end of the course of Linear Regression Models.

To start with, the essence of linear regression models is autually conditional expectation. That's to say, given $X$, the best estimator of $Y$ is $\mathbb{E}(Y|X)$. And further, if we assume that $\mathbb{E}(Y|X)$ is a linear function of $X$, here comes the following interesting theorem.

#####Theorem 1

Suppose that $X$ and $Y$ have a joint distribution with means $\mu_X$ and $\mu_Y$ , standard deviations $\sigma_X$and $\sigma_Y$ , and correlation $\rho$. Show that if $\mathbb{E}(Y|X)$ is a linear function of $X$, then

$\mathbb{E}(Y|X) = \mu_Y+\rho\sigma_Y(\frac{X-\mu_X}{\sigma_X})$ 

Its proof is not very difficult.

We may find this theorem is quite similar to the theorem below:

#####Theorem 2 

Let $(X_1, X2)$ have a joint p.d.f of the form below:

$f(x_1, x_2) = \frac{1}{2\pi\sigma_1\sigma_2\sqrt{1-\rho^2}}e^{-\frac{1}{2(1-\rho^2)}\{(\frac{x_1-\mu_1}{\sigma_1})^2-2\rho(\frac{x_1-\mu_1}{\sigma_1})(\frac{x_2-\mu_2}{\sigma_2})+(\frac{x_2-\mu_2}{\sigma_2})^2\}}$ 

The conditional distribution of $X_2$ given $X_1 = x_1$ is the normal distribution with mean and variance
given by

$\mathbb{E}(X_2|X_1=x_1) = \mu_1+\rho\sigma_2(\frac{x_1-\mu_1}{\sigma_1})$, $Var(X_2|X_1=x_1)=(1-\rho^2)\sigma_2^2$



#### Without normal assumption

To some extent, we may relax the conditon of the distribution of the error to not just nomal but any well-defined distribution and still obtain the results under normality. 

###### simple

###### multiple



####With normal assumption

Most of the time, however, we are interested in the inference problem. And here comes into existence the assumption of normality.

###### simple

###### multiple



The independence between coefficients estimates and sum of squared residuals





#####VIF

VIF is an important index for the problem of multicollinearity. And we will give its derivation below which also illustrates why it can be taken as a sign of multicollinearity.



Just to mention, one approach to handle multicollinearity could be ridge regression.



#####Regularization

######0-norm regularization 

######1-norm regularization

######2-norm regularization

######Under the condition of orthogonalization

Things become simple when the design matrix is column orthogonal. And we will talk about the behavior of coefficient estimators under this situation.

###### 1-norm regularization

###### 2-norm regularization



#####Diagnostic and Remedial

Actually, for me this is supposed to be the most importan part which really requires lots of experience. Since I don't have much experience, however, I'm not gonna talk much about it. But maybe one day, I'll come back and finish this part. lol

The diagnostic is actually centered around the four assumptions, which are ...

While for the remedial, 	