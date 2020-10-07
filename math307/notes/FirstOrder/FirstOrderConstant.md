---
layout: standard
title: "Some Examples of First Order ODEs with Constant Coefficients"


---

[Back to Notes](/../index.md)



# Example 1

Let us start with a simple example:


$$
y' = 6y,\qquad y(0) = 3.
$$


For this problem we can guess what the solution to the ODE should be. However, let us solve it as a separable differential equation. We begin by separating the variables:


$$
\begin{split}
y' &= 6y\\
\frac{dy}{dt} &= 6y\\
\frac{dy}{y}  &= 6\,dt\\
\end{split}
$$
Once we are at this point, we integrate both sides


$$
\begin{split}
\int \frac{dy}{y}&= \int 6\,dt\\
\ln|y| &= 6t+c
\end{split}
$$


for some constant $c$. We only include one constant of integration, because including a second constant of integration would be redundant. 

We can remove by natural logarithm by exponentiating both sides:


$$
|y| = e^{6t+c} = e^ce^{6t}.
$$


We can undo the absolute value as follows:


$$
y = \pm e^c e^{6t} = A e^{6t}\qquad\text{where}\qquad A = \pm e^c.
$$


Thus the solution to the differential equation is


$$
y = Ae^{6t}.
$$


To handle the initial condition we just plug in the initial value:
$$
3 = y(0) = A e^{0} = A
$$
 

and so 
$$
y(t) = 3 e^{6t}
$$
solves the differential equation.



# Example 2



Let us now go to a more complicated example:


$$
y' = 2y + 6,\qquad y(0) = 7
$$


We solve this by separating variables as above:


$$
\begin{split}
\frac{dy}{dt} = 2y+6\\
\frac{dy}{dt} = 2(y+3)\\
\frac{dy}{y+3} = 2\,dt
\end{split}
$$
 

and then we integrate:


$$
\begin{split}
\int \frac{dy}{y+3} &= \int 2\,dt\\
\ln|y+3| &= 2t + c\\
|y+3| &=e^{2t+c} =e^{c}e^{2t}\\
y+3 &=\pm e^{c}e^{2t}
\end{split}
$$


and so
$$
y = Ae^{2t} - 3.
$$


Using the initial value $y(0) = 7$, we can write


$$
7 = y(0) = Ae^{2\times 0} - 3 = A - 3,
$$


and so $A = 10$.



Therefore the solution is:


$$
y(t) = 10 e^{2t} - 3.
$$




# Example 3

Let us now solve a similar example to Example 2, using a method that will be more useful for integrating factors. In the future, I'd recommend solving this example as we solved the two previous examples, but this is to introduce a technique that will work for more general situations.


$$
y' = 5y+ 6,\qquad y(0) = 3.
$$


We are going to start by rearranging the above equation as:


$$
y' - 5y = 6.
$$


We are not going to multiply by a function $\mu = \mu(t)$ on both sides:


$$
\mu y' - 5\mu y = 6\mu.
$$


The function $\mu$ is called an *integrating factor*. We now what to choose a good choice of $\mu$ which makes the above equation simpler. We do this by saying say that left hand side should be the derivative of $\mu y$:


$$
(\mu y)' \overset{\text{want}}{=}  \mu y' - 5\mu y = 6\mu.
$$
By the product rule $(\mu y)' = \mu' y + \mu y'$ and so we want:


$$
(\mu y)' = \mu y' + \mu' y = \mu y' - 5\mu y .
$$


We can match the $\mu y'$ terms together which leads to:
$$
\mu' y = -5\mu y,\qquad \text{   and so   }\qquad \mu' = -5\mu.
$$


The right-most equation above can be solved as the first two examples and has a general solution of the form:


$$
\mu = A e^{-5t}.
$$


Now it turns out we don't need to include the most general solution, we just want a single solution so we'll choose $\mu = e^{-5t}$, i.e. $A = 1$.



Going back to the equation with $\overset{\text{want}}{=}$ included in it we arrive at


$$
(e^{-5t} y)' = 6 e^{-5t}.
$$


By the fundamental theorem of calculus we know that if $f(t)$ is a function such that 
$$
f'(t) = 6e^{-5t},\qquad\text{then}\qquad f(t) = \int 6e^{-5t} = -\frac{6}{5} e^{-5t} + C.
$$


But we know that $(e^{-5t}y)' = 6e^{-5t}$ and so we must have:


$$
e^{-5t} y = -\frac{6}{5} e^{-5t} + C,\qquad \text{or by dividing by }e^{-5t}  \qquad y(t) = -\frac{6}{5} + C e^{5t}.
$$


We can then use the initial condition $y(0) = 3$ to get


$$
3 = y(0) = -\frac{6}{5} + C e^{5\times 0} = -\frac{6}{5} +C,\qquad\text{so}\qquad C = \frac{21}{5}.
$$


Thus


$$
y(t) = -\frac{6}{5}+ \frac{21}{5} e^{5t}.
$$
