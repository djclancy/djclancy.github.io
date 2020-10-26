---
layout: standard
title: "Some Examples of Linear ODEs"




---

[Back to Notes](/../index.md)

# Example 1

Consider the differential equation:


$$
(4+6t^2) y' + 12 t y = \sin(t).
$$


We first check if


$$
\frac{d}{dt}(4+6t^2)  \overset{?}{=} 12 t,
$$


which is the case. 



This means the left-hand side is


$$
\left( (4+6t^2) y\right)' = (4+6t^2)y' + 12ty
$$


by the chain rule. 



Hence, combining these two observations


$$
\left( (4+6t^2)y\right)' = \sin(t).
$$


We can integrate both sides to get


$$
\begin{split}
(4+6t^2)y &= \int \sin(t)\,dt = -\cos(t)+C\\
y&= \frac{-\cos(t)+C}{4+6t^2}.
\end{split}
$$


Is the solution to the differential equations.



# Example 2



Consider the differential equation:


$$
y' + \frac{4}{t+3} y = t^2+6t+9.
$$


We normally multiply by $\mu$ to begin, but we will actually begin by first factoring the right-hand side


$$
y' + \frac{4}{t+3}y = (t+3)^2.
$$


We now multiply by $\mu$, the integrating factor:


$$
\mu y' + \frac{4\mu}{t+3} y = (t+3)^2
$$


and we need the left-hand side to be


$$
(\mu y)' = \mu y' + \mu' y  = \mu y' + \frac{4\mu}{t+3} y.
$$


So 


$$
\mu' = \frac{4\mu}{t+3}.
$$


We solve this as a separable differential equation:


$$
\begin{split}
\frac{d\mu}{\mu} &= \frac{4}{t+3} \,dt\\
\int \frac{d\mu}{\mu} &= 4 \int \frac{1}{t+3} \,dt\\
\ln \mu &= 4\ln (t+3) = \ln\left( (t+3)^4\right)\\
\mu &= (t+3)^4.
\end{split}
$$


Where here we ignore the constants of integration because it will not be useful for the general solution to the differential equation we *want* to solve. 



We are now at:


$$
\left((t+3)^4 y\right)' = (t+3)^4 (t+3)^2 = (t+3)^6.
$$


To undo the derivative of the left-hand side we integrate both sides of the equation to get
$$
(t+3)^4 y = \int(t+3)^6\,dt.
$$


Using $u = t+3$, we get


$$
(t+3)^4 y = \frac{1}{7}(t+3)^7 + C
$$
 and rearranging:


$$
y = \frac{(t+3)^3}{7} + \frac{C}{(t+3)^4}.
$$




# Example 3



Consider


$$
y' + \frac{6t}{t^2 + 6} y = t-4.
$$


We begin by multiplying everything by $\mu$, to get


$$
\mu y' + \frac{6t}{t^2+6}\,\mu y = (t-4)\mu.
$$


We want the left-hand side to be just $(\mu y)' = \mu y'+\mu' y$.



This means we need


$$
\begin{split}
\mu' &= \frac{6t}{t^2+6} \mu\\
\frac{d\mu}{\mu} &= \frac{6t}{t^2+6}\,dt\\
\int\frac{d\mu}{\mu} &= 3\int \frac{2t}{t^2+6}\,dt\\
\ln \mu&= 3\ln (t^2+6) = \ln\left((t^2+6)^3\right)\\
\mu &= \left(t^2+6\right)^3.
\end{split}
$$
 

Again, we ignore the constant of integration at *this* point in the process of solving the ODE.



We therefore have


$$
\left( (t^2+6)^3 y\right)' = (t-4)(t^2+6)^3.
$$


To undo the derivative we need to integrate both sides of the equation


$$
(t^2+6)^3 y = \int (t-4)(t^2+6)^3\,dt.
$$




We expand the cubed term and then multiply by $t-4$ gives the integrand of the right-hand side is


$$
t^7-4t^6+18t^5 -72t^4 +108t^3 -432 t^2+216t - 864.
$$


We can integrate this to get


$$
\begin{split}
(t^2+6)^3y  &= \frac{1}{8}t^8 - \frac{4}{7}t^7 + 3 t^6 - \frac{72}{5}t^5 \\
&\qquad + 27 t^4 - 144 t^3 + 108 t^2 - 864 t + C.
\end{split}
$$


as an implicit solution.



Solving for $y$ gives


$$
\begin{split}
y &= \frac{1}{(t^2+6)^3}\bigg( \frac{1}{8}t^8 - \frac{4}{7}t^7 + 3 t^6 - \frac{72}{5}t^5 \\
&\quad \quad+ 27 t^4 - 144 t^3 + 108 t^2 - 864 t + C\bigg).
\end{split}
$$
