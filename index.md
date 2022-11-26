---
title: Deriving the Euler-Lagrange equation
layout: default
---
$$\require{physics}$$

Say we want to minimize the integral
$$ S = \int\limits_{t_i}^{t_f}\dd{t}\mathcal{L}(q, \dot{q}) \,,$$
where \(\mathcal{L}\) depends on an unknown function \(q(t)\) and its
derivative \(\dot{q}(t).\) We would like to set the variation \(\delta S\) to
zero.

Thus,
$$
\begin{align}
\delta S &= \delta \int\limits_{t_i}^{t_f}\dd{t}\mathcal{L}(q, \dot{q}) \\
&= \int\limits_{t_i}^{t_f}\dd{t}\delta\mathcal{L}(q, \dot{q}) \\
&= \int\limits_{t_i}^{t_f}\dd{t}\qty[
  \pdv{\mathcal{L}}{q}\delta q + \pdv{\mathcal{L}}{\dot{q}} \delta\dot{q}] \\
&= \int\limits_{t_i}^{t_f}\dd{t}\qty[
  \pdv{\mathcal{L}}{q}\delta q +
  \dv{t}\qty(\pdv{\mathcal{L}}{\dot{q}}\delta q)
  -\dv{t}\qty(\pdv{\mathcal{L}}{\dot{q}})\delta q] \\
&= \eval{\pdv{\mathcal{L}}{\dot{q}}\delta q}_{t_i}^{t_f}
  +\int\limits_{t_i}^{t_f}\dd{t}\qty[
  \pdv{\mathcal{L}}{q}\delta q
  -\dv{t}\qty(\pdv{\mathcal{L}}{\dot{q}})\delta q] \,.\\
\end{align}
$$

If we assume that the function \(\delta q(t)\) vanishes at the endpoints,
then it follows that
$$
\delta S = \int\limits_{t_i}^{t_f}\dd{t}\qty[
  \pdv{\mathcal{L}}{q}\delta q
  -\dv{t}\qty(\pdv{\mathcal{L}}{\dot{q}})\delta q] \,.\\
$$

And if we enforce \(\delta S = 0\), then we conclude that
$$
\pdv{\mathcal{L}}{q} - \dv{t}\qty(\pdv{\mathcal{L}}{\dot{q}}) = 0 \,.
$$

This is the Euler-Lagrange equation.
