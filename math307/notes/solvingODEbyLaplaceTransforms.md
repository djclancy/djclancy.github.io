---
layout: standard
title: Solving ODEs Using Laplace Transforms
---

In this note, I'll describe how to solve a general second order constant coefficient ODE with a general forcing function $f(t)$. That is, we'll solve
$$ \left\{ \begin{array}{l}  ay''+by'+cy = f(t)\\ y(0) = y_0 \\ y'(0) = y_1 \end{array} \right..$$

We'll require the following few rules for Laplace transforms
$$ \mathcal{L}(\delta_c(t)) = e^{-cs}$$
$$ \mathcal{L}(u_c(t) f(t-c) )  = F(s-c)$$
