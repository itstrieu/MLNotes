Gradient descent is a method used to find the minimum of your cost function $J(w)$. It works by starting at a point in your cost function and then taking a step proportional to $\alpha$, the learning rate. The function for gradient descent is 

$$
w = w - \alpha \frac{\partial}{\partial w} J(w)
$$ 

As seen in the function, w is updated with regard to the learning rate and the slope of the cost function. If the cost function slope is negative, w increases in size. If the cost function slope is positive, w decreases in size. As the gradient descent gets closer to the local minima, it takes smaller steps due to the decreasing slope. 

### Learning Rate
Choosing a learning rate that is too small or too big can be problematic. Learning rates that are too small require more time and computation while learning rates that are too large may cause the gradient descent function to miss the minima. 

One option for choosing the learning rate is to plot a graph of the cost function versus the # of iterations. This graph should converge. If it does not, there may be a bug or the learning rate is too large. A good practice is to graph the cost function versus # of iterations for these values of $\alpha$: 0.001, 0.01, 0.1, 1, ...

### Linear Regression Application
Gradient descent can be applied to linear regression. In linear regression, the most common cost function is the squared error. In this case, the gradient descent function would look like this:

$$
\begin{gather}
f_w(x) = wx \\
w = w - \alpha \frac{\partial}{\partial w} \Big(\frac{1}{2m} \sum^m_{i=1}{y^{(i)} - f_w(x^{(i)}) \Big)^2} \\
\text{where}\\
\frac{\partial}{\partial w} J(w) = \sum^m_{i=1}{\Big(y^{(i)}- f_w(x^{(i)})\Big)x^{(i)}}\\
\end{gather}
$$

The process for deriving the gradient descent function for $b$, the intercept, is the same. 


### Batch Gradient Descent vs. Mini-Batch Gradient Descent

### Gradient Approximation

### Gradient Checking

### Gradient Descent with Momentum
The math behind gradient descent with momentum involves computing an exponentially weighted average of the gradients and using that to update the weights. 
