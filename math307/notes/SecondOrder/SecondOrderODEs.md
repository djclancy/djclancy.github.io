---
layout: standard
title: "Second Order ODEs"

---

[Back to index](/../index.md)



Before doing any examples, we begin with recalling that the solutions to the differential differential equation 


$$
ay''+by' +cy = 0
$$


is intimately connected to the roots of the parabola


$$
ar^2 + br+c = 0.
$$




# Example 1



Consider


$$
y''+6y' + 5y = 0.
$$


The *characteristic polynomial* is 


$$
r^2 + 6r + 5 = (r+5)(r+1),
$$


and so the roots are 


$$
r = -1\qquad \text{and}\qquad r= -5.
$$


Thus the solution is


$$
y = c_1 e^{-t} + c_2 e^{-5t}.
$$




# Example 2



Consider 


$$
y''+ 8y' + 25 y = 0,
$$


which has characteristic equation


$$
r^2 + 8r + 25 = 0.
$$




This terms cannot be factored with *real roots* but does have complex roots. We use the quadratic formula


$$
r = \frac{-b\pm \sqrt{b^2-4ac}}{2a} = \frac{-8\pm \sqrt{64- 100}}{2},
$$
 

which can be rewritten as


$$
r = \frac{-8 \pm \sqrt{-36}}{2} = \frac{-8 \pm 6i}{2} = -4\pm 3i.
$$


Therefore the solution is


$$
y = e^{-4t} \left(c_1 \cos(3t) + c_2 \sin(3t) \right).
$$


## Note:

Sometimes it is easier to just complete the square when we have complex roots:


$$
r^2+ 8r +25 = r^2+8r + 16 + 9 = (r+4)^2 + 3^2
$$


and so 


$$
r^2+8r+25 = 0
$$


means


$$
\begin{split}
(r+4)^2 &= -3^2\\
r+4 &= \sqrt{-3^2} = \pm 3i\\
r &=-4 \pm 3i.
\end{split}
$$








# Example 3



Consider


$$
y'' + 6y' + 9 y = 0.
$$




The characteristic equation is


$$
r^2+6r+9 = (r+3)^2.
$$


This is a repeated root which is $r= -3$.



This means the general solution to the ODE is


$$
y = (c_1+c_2t)e^{-3t}.
$$
















