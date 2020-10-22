---
layout: standard
title: "Some Examples of Autonomous Differential Equations"




---

[Back to Notes](/../index.md)

# Example 1

Consider the autonomous equation


$$
y' = f(y) = (9y+1)(y-5)(y+3)^2.
$$




We see that $f(c) = 0$ only for the values $c = 5, -3, -1/9$. These correspond the *equilibrium solutions* $y(t) = 5$, $y(t) = -3$ and $y(t) = -1/9$ to the differential equation. 



In order to figure out the behavior of solutions $y$, we need to know the behavior of the function $f(y)$ for $y<-3$, -3<y<-1/9$, $-1/9<y<5$ and $y>5$. We now compute the signs of $f$ on these regions:


$$
\begin{split}
f(-10) &= (-)(-)(+)>0\\
f(-1)&= (-)(-)(+)>0\\
f(0) &= (+)(-)(+)<0\\
f(10) &= (+)(+)(+) >0.
\end{split}
$$


Therefore, we know the graph of $f$ should look something like:



![](/images/aut1.1.png)



The above picture is an actual graph of $f(y)$ in red with $y$ in the horizontal axis. We can also write the phase diagram:







