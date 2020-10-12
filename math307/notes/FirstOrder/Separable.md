---
layout: standard
title: "Some Examples of Separable"



---

[Back to Notes](/../index.md)

# Example 1

Consider


$$
y' = x^2 e^y.
$$


To solve this we rewrite as


$$
\begin{split}
\frac{dy}{dx} &= x^2 e^y\\
e^{-y} dy &= x^2\,dx\\
\int e^{-y}\,dy &= \int x^2\,dx\\
-e^{-y} &= \frac{1}{3} x^3 + c\\
-y &= \ln \left(-\frac{1}{3}x^3 + C \right)\\
y &= -\ln \left( -\frac{1}{3}x^3 + C \right).
\end{split}
$$




# Example 2

Consider
$$
y' - t = ty^2.
$$


This can be solved by


$$
\begin{split}
\frac{dy}{dt} &= t + ty^2\\
\frac{dy}{dt}&= t(1+y^2)\\
\frac{dy}{1+y^2} &= t\,dt\\
\int \frac{dy}{1+y^2} &= \int t\,dt\\
\arctan(y)&= \frac{1}{2}t^2 + c\\
y &= \tan\left( \frac{1}{2}t^2 +C \right).
\end{split}
$$


# Example 3

Consider


$$
\frac{dy}{dt} = \frac{1}{\pi}\left(3+ \sin t \right) y
$$
We will write $\exp(x) = e^x$. 

This can be solved by


$$
\begin{split}
\frac{dy}{y} &= \frac{3+\sin t}{\pi}\,dt\\
\int \frac{dy}{y} &= \int \frac{3+\sin t}{\pi} \,dt\\
\ln |y| &= \frac{3}{\pi}t - \frac{1}{\pi} \sin t + C\\
|y| &= \exp\left(\frac{3}{\pi}t -\frac{1}{\pi}\sin t + C \right)\\
y &= \pm e^C\exp\left(\frac{3}{\pi}t -\frac{1}{\pi}\sin t \right)\\
y&= A\exp\left(\frac{3}{\pi}t -\frac{1}{\pi}\sin t \right).
\end{split}
$$
