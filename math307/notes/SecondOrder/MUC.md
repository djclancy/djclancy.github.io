---
layout: standard
title: "Method of Undetermined Coefficients"

---

[Back to index](/../index.md)





# Example 1

Consider 
$$
y''+3y' + 2y = \cos(2t) + t.
$$


We start by finding the homogeneous solution. That is the solution to
$$
y'' + 3y' + 2y = 0.
$$


The characteristic polynomial is $r^2+3r+2 = (r+2)(r+1) = 0$ and so the homogeneous solution is
$$
y_h = c_1 e^{-t} + c_2 e^{-2t}.
$$




Now the guess for the particular solutions is 


$$
\displaystyle y_p =\underset{\text{from the cosine term}}{\underbrace{ A\cos(2t)+B\sin(2t)}}+ \underset{\text{from the $t$ term}}{\underbrace{Ct +D}}.
$$




The derivatives of $y_p$ are
$$
\begin{split}
y_p' &= -2A\sin(2t) +2 B\cos(2t) + C\\
y_p'' &= -4 A\cos(2t) -4 B\sin(2t)
\end{split}
$$


We plug these into the differential equation:
$$
\begin{split}
&y_p''+3y_p' + 2y_p \\
&= (-4 A\cos(2t) - 4B\sin(2t)) + 3 (-2A\sin(2t) +2B\cos(2t)+C) \\
&\qquad + 2(A\cos(2t)+B\sin(2t)+Ct+D)\\
&= (-2A+6B)\cos(2t) + (-2B -6A)\sin(2t) + 2Ct + (2D+3C)\\
&= \cos(2t)+t.
\end{split}
$$




So we get this system of equations:
$$
\begin{split}
(-2A+6B)&= 1\\
(-6A-2A)&= 0\\
2C&=1\\
2D+3C &= 0.
\end{split}
$$




To solve for $A$ and $B$ we have


$$
\begin{split}
-3\big(-2A + 6B &= 1 \big)\\
-6A - 2A &= 0\\
\hline 
0A -20 B &= -3
\end{split}\qquad B = 3/20.
$$
Similarly, we can find that $A = -1/20$.



Solving for $C$ and $D$ is much easier. It is given by


$$
C = \frac{1}{2},\qquad D = \frac{-3}{4}.
$$


Thus the general solution is


$$
y = c_1 e^{-t}+c_2e^{-2t} + \frac{1}{20}(3\sin(2t)-\cos(2t)) + \frac{1}{4} (2t  - 3).
$$


# Example 2

Consider 
$$
y'' + 4y = \cos(2t).
$$


Again, we first find the homogeneous solution
$$
y_h = c_1\cos(2t) + c_2 \sin(2t).
$$


Normally our guess for the particular solution would be 


$$
y_p = A \cos(2t) + B\sin(2t).
$$


Unfortunately, since both of these terms appear in the homogenous solutions, the above guess is wrong. The correct guess involves multiplying the above guess by $t$:
$$
y_p = t(A\cos(2t)+B\sin(2t)).
$$


We compute the first two derivatives:


$$
\begin{split}
y_p' &= (A\cos(2t)+B\sin(2t)) + t (-2A \sin(2t) + 2B\cos(2t))\\
y_p''&= (-2A\sin(2t) + 2B\sin(2t)) + (-2A\sin(2t) + 2B\cos(2t)) \\
&\qquad + t(-4A\cos(2t) -4B\sin(2t))
\end{split}
$$


So, plugging this into the differential equation gives


$$
\begin{split}
&y_p'' + 4y_p \\
 &=(-4A\sin(2t) + 4B\cos(2t)) + t(-4A\cos(2t) -4B\sin(2t))\\
 &\qquad + 4t(A\cos(2t)+B\sin(2t))\\
 &= -4A\sin(2t) + 4B\cos(2t)\\
 &= \cos(2t).
\end{split}
$$


This leads to the system
$$
\begin{split}
-4A = 0\\
4B = 1
\end{split},\qquad B = 1/4, A = 0.
$$


So


$$
y_p = \frac{1}{4}t\sin(2t).
$$






And lastly the general solution is


$$
y = c_1\cos(2t)+ c_2\sin(2t) + \frac{1}{4}t\sin(2t).
$$


