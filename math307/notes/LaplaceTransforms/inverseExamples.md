---
layout: standard
title: "Inverse Laplace Transform Examples"
---



[Back to index](/../index.md)



## Example 1

Consider the function 


$$
F(s) = \frac{2}{(s-4)(s+7)}.
$$


We do a partial fraction decomposition (which is almost always a good first step). That is we write


$$
\frac{2}{(s-4)(s+7)} = \frac{A}{s-4}+\frac{B}{s+7}.
$$


Multiplying by the denominator on the LHS gives



\begin{equation}\label{eqn:1}
2 = A(s+7) + B(s-4).
\end{equation}



Then setting $s = 4$ gives 


$$
2 = A(4+7) + B(4-4) = 11A\\
A = \frac{2}{11}.
$$


We can also look at the coefficient of $s$  in \eqref{eqn:1} gives


$$
0s = (A+B)s\\
B = -A = -\frac{2}{11}.
$$


So
$$
F(s) = \frac{2}{11} \left(\frac{1}{s-4}- \frac{1}{s+7} \right).
$$




Hence


$$
\mathcal{L}^{-1}(F) = \frac{2}{11} \mathcal{L}^{-1}\left(\frac{1}{s-4} \right) - \frac{2}{11} \mathcal{L}^{-1}\left(\frac{1}{s+7} \right)\\
= \frac{2}{11} \left( e^{4t} - e^{-7t}\right).
$$




## Example 2



Consider the function


$$
F(s) = \frac{24s}{(s+1)(s^2+8s+31)}.
$$




Again, we start with partial fractions:


$$
\frac{24s}{(s+1)(s^2+8s+31)} = \frac{A}{s+1} + \frac{Bs+C}{s^2+8s+31},
$$


because the term $s^2+8s+31$ cannot be factored.



Multiplying by the denominator on the left hand side gives:



\begin{equation} \label{eqn:2}

24s = A(s^{2} +8s+31) + (Bs+C)(s+1).

\end{equation}



Setting $s = -1$ gives


$$
-24 = A((-1)^2 +8(-1)+31) + (B(-1)+C)(-1+1) = 24 A\\
A = -1.
$$


Looking at the coefficient of $s^2$ on both sides of \eqref{eqn:2} gives


$$
0s^2 = (A+B)s^2\\
B = -A = 1.
$$


Lastly, setting $s = 0$ in \eqref{eqn:2} gives


$$
0 = 31 A + C\\
C = -31 A = 31,
$$


and therefore



\begin{equation} \label{eqn:3}

F(s) = \frac{24}{(s+1)(s^2+8s+31) } = -\frac{1}{s+1} + \frac{s+31}{s^2+8s+31}.

\end{equation}





We now complete the square on the $s^2+8s+31$ term. This gives


$$
s^2+8s+31 = (s-a)^2+b^2\\
s^2+8s+31 = s^2-2as+a^2+b^2\\
-2a = 8\\
a^2 +b^2 = 31,
$$


which in turn gives


$$
s^2+8s+31 = (s+4)^2 + \sqrt{15}^2.
$$




Going back to \eqref{eqn:3}, we have



\begin{equation} \label{eqn:4}

F(s) = -\frac{1}{s+1} + \frac{s+31}{(s+4)^2 + \sqrt{15}^2}.

\end{equation}



We want to make the last term on the right-hand side of equation \eqref{eqn:4} be of the form


$$
\frac{\tilde{A}(s+4) + \tilde{B}(\sqrt{15})}{(s+4)^2 + \sqrt{15}^2},
$$


in order to use the Laplace transform table.



We do this by adding zero in a clever way, $s = (s+4-4)$, and multiplying by 1 in a clever way, $1 = \sqrt{15}/\sqrt{15}$ so that \eqref{eqn:4} becomes:


$$
F(s) = -\frac{1}{s+1} + \frac{s+31}{(s+4)^2 + \sqrt{15}^2}\\
= -\frac{1}{s+1} + \frac{(s+4-4)+31}{(s+4)^2+\sqrt{15}^2}\\
= -\frac{1}{s+1} + \frac{(s+4) + -4 +31}{(s+4)^2+\sqrt{15}^2}\\
= -\frac{1}{s+1} + \frac{s+4}{(s+4)^2+\sqrt{15}^2} + \frac{27}{(s+4)^2+\sqrt{15}^2}\\
= -\frac{1}{s+1} + \frac{s+4}{(s+4)^2+\sqrt{15}^2} + \frac{27}{\sqrt{15}}\frac{\sqrt{15}}{(s+4)^2+\sqrt{15}^2}.
$$


This is much easier to take the inverse Laplace transform of:


$$
\mathcal{L}^{-1}(F) = -\mathcal{L}^{-1}\left(\frac{1}{s+1}\right) + \mathcal{L}^{-1}\left(\frac{s+4}{(s+4)^2+\sqrt{15}^2} \right) + \frac{27}{\sqrt{15}}\mathcal{L}^{-1}\left(\frac{\sqrt{15}}{(s+4)^2+\sqrt{15}^2}  \right)\\
= -e^{-t} + e^{-4t}\cos(\sqrt{15}t) + \frac{27}{\sqrt{15}} e^{-4t}\sin(\sqrt{15}t).
$$









$$

$$


