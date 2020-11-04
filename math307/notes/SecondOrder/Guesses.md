---
layout: standard
title: "A Big Collection of Guesses for Method of Undetermined Coefficients"



---

[Back to index](/../index.md)



Here is a collection of differential equations, I suggest trying to find the correct guess for the particular solution $y_p$ before moving onto the answers.

1. $y'' + 2y' + y = e^{4t}$
2. $y'' + 6y = \cos(3t)$
3. $y'' + 7y' + 6y = e^{-t}$
4. $y'' + 3y' + 2y = t^2 +5$
5. $y''+5y' + 4y = t^2e^t$
6. $y''-4y = te^{2t}$
7. $y''+2y'+y = e^{-t} + e^t$
8. $y''+10 y' + 16y = e^t + \cos(2t)+ t$





# Solutions



## 1

$$
y'' + 2y' + y = e^{4t}
$$





Since the homogeneous solution is 
$$
y_h = (c_1+c_2t) e^{-t}.
$$

Our normal guess for the particular solution is $y_p = Ae^{4t}$. Since there are no terms which overlap with the homogeneous solutions we do not have to include any correction (which is the multiplication by $t$).


$$
y_p = Ae^{4t}.
$$


## 2

$$
y'' + 6y = \cos(3t)
$$



The homogeneous solution is


$$
y_h = c_1\cos(\sqrt{6}t) + c_2\sin(\sqrt{6}t).
$$


The normal guess for the particular solution is $y_p = A\cos(3t)+B\sin(3t)$, which does not have any term appearing in the homogeneous solution. So there is no correction again. Thus


$$
y_p = A\cos(3t) + B\sin(3t).
$$




## 3

$$
y'' + 7y' + 6y = e^{-t}
$$



The homogeneous solution is
$$
y_h = c_1e^{-6t}+c_2e^{-t}
$$


Our normal guess for the particular solution is $y_p = Ae^{-t}$ which does appear in the homogeneous solution exactly once. We therefore have to include the correction by multiplying the $t$:
$$
y_p =  A te^{-t}.
$$


## 4

$$
y'' + 3y' + 2y = t^2 +5
$$



The homogeneous solution is
$$
y_h = c_1 e^{-2t} + c_2 e^{-t}.
$$


The guess for the particular solution is
$$
y_p = A t^2 + Bt + C,
$$
 and we don't have to have any correction.



## 5

$$
y''+5y' + 4y = t^2e^t
$$





The homogeneous solution is
$$
y_h = c_1e^{-t} + c_2e^{-4t}.
$$


The particular solution is


$$
y_p = (At^2 + Bt + C) e^{t},
$$
and none of these terms appear in the homogeneous solution and so there is no correction need as well.



## 6

$$
y''-4y = te^{2t}
$$



The homogeneous solution is


$$
y_h = c_1 e^{2t} + c_2e^{-2t}.
$$


The normal guess for the particular solution would be
$$
y_p = (At+B)e^{2t}.
$$


However, the $Be^{2t}$ term overlaps with the homogeneous solution. Now if we just multiply the $Be^{2t}$ term by $t$ then
$$
y_p = (At+Bt)e^{2t}  = (A+B)te^{2t},
$$
which can be simplified by setting $C = A+B$. This idea turns out to be wrong!



The correct thing to do is to multiply *everything* involving $t^ne^{2t}$ for some $n = 0,1,\dotsm$ by $t$. That means;
$$
y_p = t(At+B)e^{2t}
$$
is the correct guess. 



## 7

$$
y''+2y'+y = e^{-t} + e^t
$$



The homogeneous solution is
$$
y_h = (c_1+c_2 t) e^{t}.
$$


The normal particular solution is
$$
y_p = Ae^{-t} + B e^t.
$$


The $e^t$ term appears in the homogeneous solution *twice*! In order to correct the guess for the particular solution we have to multiply the $t^n e^{t}$ terms by $t^2$:
$$
y_p = Ae^{-t} + t^2 B e^t.
$$


## 8


$$
y''+10 y' + 16y = e^t + \cos(2t)+ t
$$




The homogeneous solution is
$$
y_h = c_1 e^{-2t} + c_2 e^{-8t}.
$$




The guess for the particular solution is


$$
y_p = A e^t + B \cos(2t) + C\sin(2t) + Dt +E,
$$


and does not need any correction terms.

