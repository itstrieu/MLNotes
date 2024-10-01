---
topic: Logistic Regression
---
tags: [[01. second brain/3 - tags/logistic regression|logistic regression]] [[cost function]] 

Logistic regression is a supervised learning method used for classification problems. Unlike with linear regression, logistic regression is modeled by the [[Sigmoid Function]]. 

$$
f_{w,b}(x) = \frac{1}{1+e^{-f_(x)}}
$$

The output of the Sigmoid function can be considered the "probability" that the class is 1 and not 0. All the probabilities must add up to 1. 

The logit or log odds function is the inverse of the Sigmoid Function. 

$$
g(f(x)) = log(\frac{f(x)}{1-f(x)}) = wx + b
$$

We get the odds by exponentiating both sides

$$
\frac{f(x)}{1-f(x)}=e^{wx+b}
$$

The [[Odds Ratio]] is defined as

$$
OR=\frac{odds(x+1)}{odds(x)}=\frac{\frac{f(x+1)}{1-f(x+1)}}{\frac{f(x)}{1-f(x)}}=\frac{e^{w(x+1)+b}}{e^{wx+b}}
$$


The [[cost function]], or goodness-of-fit, for logistic regression uses the log function and is called the log loss function, which is the [[Negative Log-Likelihood]].

$$
L(f_{w,b}(x^{(i)},y^{(i)}))= 
	\begin{cases}
		-log(f(x)) &\text{if } y^{(i)}=1 \\
		-log(1-f(x)) &\text{if } y^{(i)}=0
	\end{cases}
$$

It can also be written as a single expression also known as the cross-entropy of the predicted distribution from the actual. 

$$
L(f_{w,b}(x^{(i)}))=-y^{(i)}log(f(x))-(1-y^{(i)})log(1-f(x))
$$

The best fit is obtained when $-L(f_{w,b})$ is minimized. Alternatively, one could maximize the inverse, its positive log-likelihood. This is known as the maximum likelihood estimation, or [[MLE]].

$$
L(f(x)) = \prod_{y^{(i)}=1}=1{f(x))} \prod_{y^{(i)}=0}{(1-f(x))}
$$

### Decision Boundary 
https://community.deeplearning.ai/t/derivation-of-dl-dz/165
