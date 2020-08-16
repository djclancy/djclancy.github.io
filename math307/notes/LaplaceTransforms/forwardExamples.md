---
layout: standard
title: "Some Examples of Laplace Transforms"
---

## Example 1

Taking the Laplace transform of
$$
f(t) = \left\{
\begin{array}{l}
3t^2 - 9t &: 0\le t< 3\\
0 &: 3\le t<2\pi\\
\sin(t) &: \pi \le t
\end{array}
\right..
$$
Below is a graph of the function $f$.

![](C:\Users\dclan\OneDrive\Documents\GitHub\djclancy.github.io\math307\notes\LaplaceTransforms\images\examplef_parabola_0_sin.png)

The first thing we do is to rewrite the function $f$ in terms of Heaviside functions $u_c$. We also make no distinction between the function $u_0(t)$ and the function which is identically 1.



We will handle this by treating each different part of the function $f$ one at a time (which is why the image above has red, blue and green sections).



The red curve, which is $f(t)$ for $0\le t< 2$, is the function $3t^2-9t$. The Heaviside functions can be viewed as turning on and off a function at specified times. That is $g(t)(u_a - u_b)$ is the function which is $g(t)$ for $a\le t< b$ and $0$ for $0\le t< a$ and 0 for $t\ge b$. Hence the red curve is represented by
$$
\left(3t^2-9t\right)\left(u_0 - u_3\right) = (3t^2-9t)(1-u_3).
$$
The blue curve is just zero so we can represent that by $0(u_3-u_{2\pi}) = 0$. 



The green curve is a sine curve, which is turned on after time $t = 2\pi$ and is never turned off. Therefore, the green part of the curve is represented by
$$
\sin(t) u_{2\pi}.
$$
Hence
$$
f(t) = (3t^2 - 9t)(1-u_{3}) + \sin(t) u_{2\pi}.
$$
In order to easily use the [table](Laplace.Transform.Table.pdf) of Laplace transforms, we must have terms of the form 
$$
g(t-c)u_c.
$$
