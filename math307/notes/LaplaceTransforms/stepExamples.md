---
layout: standard
title: "Some Examples with Step Functions"
---

[Back to index](/../index.md)

## Example 1

Consider the function 


$$
f(t) = \left\{\begin{array}{ll}
5 &: 0\le t< 2\\
\pi &: 2\le t< 3\\
-4 &: 3\le t< 2\pi\\
2 &: t\ge 2\pi
\end{array}\right..
$$


Here is a graph of $f$:



![](C:\Users\dclan\OneDrive\Documents\GitHub\djclancy.github.io\math307\notes\LaplaceTransforms\images\stepExample1.png)





I've included different colors in the graph so that we can discuss the different parts of the function.



How do we handle each different part?

We recall that $u_a-u_b$ is the function which is 1 for $a \le t< b$ and $0$ for all other $t$'s. 

So the red part of the graph (i.e. what happens for $0\le t < 2$) can be described as turning on the constant function $5$ for the times between 0 and 2. That is


$$
5(u_0 - u_2) \quad \text{is the red part of the graph}.
$$


![](C:\Users\dclan\OneDrive\Documents\GitHub\djclancy.github.io\math307\notes\LaplaceTransforms\images\stepExample1a.png)



Similarly, 


$$
\pi (u_2-u_3) \qquad\text{is the light blue part of the graph,}\\
-4(u_3-u_{2\pi}) \qquad \text{ is the purple part of the graph,}\\
2 u_{2\pi} \qquad \text{is the black part of the graph.}
$$


Adding all of these together gives the decomposition of $f$ into step functions:


$$
f(t) = 5(u_0-u_2) + \pi (u_2-u_3) - 4 (u_3-u_{2\pi}) + 2u_{2\pi}\\
= 5u_0 + (\pi-5) u_2 + (-4-\pi)u_3 + 6 u_{2\pi}.
$$


Typically we write $u_0 = 1$, since we usually just care about positive time $t\ge 0$. 


$$
f(t) = 5+(\pi-5) u_2 + (-4-\pi)u_3 + 6 u_{2\pi}.
$$




## Example 2

Consider the function 


$$
f(t) = \left\{ \begin{array}{ll}
t^2 &:0\le t<2\\
4 &: 2\le t < 5\\
4 - (t-5)^2 &: t\ge 5
\end{array}\right..
$$


Here is the graph of $f$



![](C:\Users\dclan\OneDrive\Documents\GitHub\djclancy.github.io\math307\notes\LaplaceTransforms\images\stepExample2.png)





Again, we think of $g(t) (u_a-u_b)$ as the function which turns on the function $g(t)$ only during the time $a\le t<b$. 



Therefore,


$$
t^2(u_0-u_2) \quad \text{is the red part,}\\
4(u_2-u_5) \quad \text{is the light blue part,}\\
\left(4-(t-5)^2\right)(u_5) \quad \text{is the green part.}
$$
Adding these together gives the decomposition of $f$.


$$
f(t) = t^2(u_0-u_2) +4(u_2-u_5) + (4-(t-5)^2)u_5\\
= t^2 u_0 + (4-t^2)u_2 + (-(t-5)^2) u_5\\
=t^2 +(4-t^2)u_2 - (t-5)^2 u_5.
$$
