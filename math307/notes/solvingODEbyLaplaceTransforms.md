---
layout: standard
title: Solving ODEs Using Laplace Transforms
---

In this note, I'll describe how to solve a general second order constant coefficient ODE with a general forcing function $f(t)$. That is, we'll solve
\begin{equation} 
\label{eqn:IVPgen}   ay''+by'+cy = f(t),\qquad  y(0) = y_0, \qquad  y'(0) = y_1  .
\end{equation}

We'll require the following few rules for Laplace transforms and their correspinding inverses:

\begin{equation} \label{eqn:convLT}  \mathcal{L} (f\ast g) = F(s)G(s), \end{equation}

\begin{equation} \label{eqn:f'}  \mathcal{L} (f') = sF(s) - f(0), \end{equation}

\begin{equation} \label{eqn:f''}  \mathcal{L} (f'') = s^2 F(s) - sf(0) - f'(0).\end{equation}

Applying rules \eqref{eqn:f'} and \eqref{eqn:f''} to the IVP in \eqref{eqn:IVPgen} gives

$$
\mathcal{L}\left(ay''+by'+cy\right) = \mathcal{L}(f)
$$

$$
a\left(s^2Y(s)-sy(0)-y'(0) \right) + b \left( sY(s) -y(0)\right) + c\left( Y(s) \right) = F(s)
$$

$$
\left(as^2+bs+c\right)Y(s) - \left(asy_0 + ay_1 + by_1\right) = F(s).
$$

Rearranging gives
\begin{equation} \label{eqn:Y}
Y(s) = F(s) \left(\frac{1}{as^2+bs+c} \right) + \frac{asy_0+ay_1+by_0}{as^2+bs+c}.
\end{equation}
We will rewrite this as 
\begin{equation} \label{eqn:Y2}
Y(s) = F(s) H(s) + \Phi(s),
\end{equation}
where

$$
H(s) = \frac{1}{as^2+bs+c},\qquad 
\Phi(s) = \frac{asy_0+ay_1+by_0}{as^2+bs+c}.
$$ 

It is difficult to write out general explicit formulas for the inverse Laplace transforms of $H$ and $\Phi$, so instead we'll say that we can take the inverse Laplace transform and write it as

$$
h(t) = \mathscr{L}^{-1}(H),\qquad \phi(t) = \mathscr{L}^{-1}(\Phi).
$$

What are the fuctions $\phi$ and $h$ representing? Well, $h$ has Laplace transform
$$
\mathcal{L}(h) = \frac{1}{as^2+bs+c},
$$ which is also the same as the solution to the initial value problem
$$
ay''+by'+cy = \delta_0(t),\qquad y(0) = 0,\quad y'(0) = 0.
$$

