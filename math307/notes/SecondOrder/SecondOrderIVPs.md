---
layout: standard
title: "Second Order IVPs"

---

[Back to index](/../index.md)



# Example 1



Consider the initial value problem


$$
\begin{split}
&y''+6y' - 7y = 0\\
& y(0) = 4\\
&y'(0) = 7
\end{split}
$$


We begin by solving the differential equation. We start with the characteristic equation


$$
r^2+6r -7 = (r+7)(r-1).
$$


Therefore the roots are $r = -7$ and $r = 1$. This means


$$
y = c_1 e^{t} + c_2 e^{-7t}.
$$


To solve for the values of $c_1$ and $c_2$, we use the initial conditions:


$$
y(0) = 4,\qquad y'(0) = 7.
$$




We use the first initial value to get


$$
4 = y(0) = c_1 e^0 + c_2 e^{-7\times 0} = c_1+c_2.
$$


Using the second initial value we get


$$
7 = y'(0) = c_1 e^0 - 7c_2 e^{-7\times 0} = c_1 - 7c_2.
$$


This gives the system of equations


$$
\begin{split}
c_1 + c_2 &= 4\\
c_1 - 7c_2 &= 7
\end{split}.
$$


We solve this as we would any system of equations. For this example we will add/subtract (multiples) of the equations together.

We can cancel the $c_1$ terms by subtracting the bottom equation from the top equation:


$$
\begin{split}
c_1+c_2 &= 4\\
-\Big(c_1 - 7c_2 &= 7 \Big)\\
\hline
0c_1 +8 c_2&= -3.
\end{split}
$$


This means that 


$$
c_2 = -3/8.
$$


We then use either equation to solve for $c_1$; we'll choose using the $c_1+c_2 = 4$ equation:


$$
c_1 - \frac{3}{8} = 4,\qquad \quad c_1 = 4+\frac{3}{8} = \frac{35}{8}.
$$


Thus


$$
y = \frac{35}{8} e^t - \frac{3}{8} e^{-7t}.
$$




# Example 2



Consider


$$
\begin{split}
&y'' - 8y' + 16y = 0\\
&y(0) = 5\\
&y'(0)  = 3.
\end{split}
$$


We solve the differential equation by looking at the characteristic equation


$$
r^2-8r+16 = (r-4)^2.
$$


So, we have a repeated root $r = 4$ which means


$$
y = (c_1+c_2t)e^{4t}.
$$


But then, we differentiate to get


$$
y' = 4(c_1+c_2 t)e^{4t} + c_2 e^{4t}.
$$


But then we can use the initial values $y(0) = 5$ and $y'(0) = 3$ to have:


$$
\begin{split}
5 &= y(0) = (c_1 + c_2\times 0)e^{4\times 0} = c_1\\
3&= y'(0) = 4(c_1+c_2\times 0)e^{4\times 0} + c_2 e^{4\times 0} = 4c_1+c_2.
\end{split}
$$


This is easier to solve than Example 1, which is 


$$
c_1 = 5,\qquad \text{and}\qquad c_2 = -17.
$$


Then


$$
y = (5-17t)e^{4t}.
$$


## Note



This algebra in this example was much easier than the first example and, as we will see, is much easier than the third example below. This is very often the case.



# Example 3



Consider 


$$
\begin{split}
&y'' + 2y' + 5y = 0\\
&y(0) = 2\\
&y'(0) = 3
\end{split}
$$


We begin by looking at the characteristic equation:


$$
r^2+2r+5 = (r+1)^2 + 2^2,
$$


which has (complex) roots


$$
r = -1\pm 2i.
$$


This can also be obtained by the the quadratic formula.



The solution is therefore


$$
y(t) = e^{-t} \left( c_1 \cos(2t)+c_2 \sin(2t)\right).
$$


We should also differentiate this to get


$$
\begin{split}
y' &= - e^{-t} (c_1 \cos(2t) + c_2\sin(2t)) \\
&\qquad + e^{-t}(-2c_1\sin(2t) + 2 c_2\cos(2t))\\
&= e^{-t} \left((-c_1+2c_2)\cos(2t) + (-c_2-2c_1)\sin(2t) \right).
\end{split}
$$


We now use the initial conditions


$$
\begin{split}
2 &= y(0) = e^{-0} \left( c_1 \cos(2\times 0) + c_2 \sin(2\times 0)\right) \\
2&= c_1\\
3&= e^{-0} \left( (-c_1+2c_2) \cos(2\times 0) + (-c_2-2c_1) \sin(2\times 0)\right)\\
3&= -c_1 + 2c_2.
\end{split}
$$


The above equations are easily solved. Indeed the second line gives $c_1 = 2$ and then we have 


$$
3 = -c_1 +2c_2 = -2 + 2c_2.
$$


So


$$
c_1 = 2,\qquad c_2 = \frac{5}{2}.
$$




Plugging this into the general solution gives


$$
y = e^{-t} \left(2\cos(2t) +\frac{5}{2}\sin(2t) \right).
$$
