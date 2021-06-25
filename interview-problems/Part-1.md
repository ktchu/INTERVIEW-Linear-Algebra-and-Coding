Portfolio Optimization: Part 1
==============================

------------------------------------------------------------------------------

Terminology
-----------

* __Return (Relative)__. The return on an asset over a time period is the
  relative change in the price of an asset from the beginning to the end of
  the time period. When the difference between the final and initial prices is
  small, the return may be computed as

  $$
    r = \log \left( \frac{P_{final}}{P_{initial}} \right)
  $$

* __Risk__. In quantiative finance, the variance and standard deviation of an
  asset's return are convenient (but not necessarily valid or accurate) measure
  of an assets riskiness. In financial parlance, the standard deviation of an
  asset's return is known as _volatility_.

Available Data
--------------

We are given the following information about a collection of assets:

* $\mu_i$: the average return for the $i$-th asset

* $\sigma_i^2$: the variance of the return for the $i$-th asset

* $\sigma_{ij}$: the covariance between the returns of the $i$-th and $j$-the
  asset. Note that $\sigma_{ii} = \sigma_i^2$.

Model Variables
---------------

* $r_i$: random variable representing the return on the $i$-th asset

* $w_i$: weight (fraction) of $i$-th asset in a portfolio

------------------------------------------------------------------------------

Problem 1
---------

### Problem 1

Suppose we have portfolio of assets where each asset has weight $w_i$. If
there are $n$ assets in a portfolio, the portfolio return and variance are:

$$
r_p = \sum_i^n r_i w_i
$$

$$
\sigma_p^2 = \sum_i^n \sum_j^n \sigma_{ij} w_i w_j
$$

Express both of these sums in matrix form.

------------------------------------------------------------------------------

Problem 2
---------

Write an expression for the expected return for the portfolio.

------------------------------------------------------------------------------

Problem 3
---------

### Problem 3

For risk tolerance level $\tau$, derive a matrix equation for the portfolio
that optimizes return-risk objective

$$
  f(w_1, w_2, \ldots, w_n) = r_p - \frac{\tau}{2} \sigma_p^2
$$

subject to the constraint $\sum_i^n w_i = 1$.

------------------------------------------------------------------------------
