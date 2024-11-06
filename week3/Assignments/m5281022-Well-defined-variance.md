## 3. Random Variables and Probability Distributions - Well-defined: variance

**Lai Hui Shan**  
**m5281022**

Let $Y$ be a random variable with the standard Cauchy density
$$
f_Y(y) = \frac{1}{\pi(1 + y^2)}, \quad y \in \mathbb{R}.
$$

## 1. Does the Expectation $\mathbb{E}(Y)$ Exist?

To determine if $\mathbb{E}(Y)$ exists, we consider the integral
$$
\mathbb{E}(Y) = \int_{-\infty}^{\infty} y \cdot f_Y(y) \, dy = \int_{-\infty}^{\infty} \frac{y}{\pi(1 + y^2)} \, dy.
$$

The integrand $\frac{y}{1 + y^2}$ does not converge absolutely on $(-\infty, \infty)$ because the tails of the Cauchy distribution decay too slowly for this integral to have a finite value. Specifically, the Cauchy distribution is known to have "heavy tails," meaning that $\int_{-\infty}^{\infty} |y| f_Y(y) \, dy$ diverges.

Therefore, the expectation $\mathbb{E}(Y)$ does not exist.

## 2. Can We Define $\mathbb{V}(Y)$? If Not, Explain the Reason.

Variance is defined as
$$
\mathbb{V}(Y) = \mathbb{E}((Y - \mathbb{E}(Y))^2),
$$
but since the expectation $\mathbb{E}(Y)$ does not exist, we cannot define $\mathbb{V}(Y)$ in the usual sense.

Even if we consider the alternative approach of calculating $\mathbb{E}(Y^2)$, the integral
$$
\mathbb{E}(Y^2) = \int_{-\infty}^{\infty} y^2 \cdot f_Y(y) \, dy = \int_{-\infty}^{\infty} \frac{y^2}{\pi(1 + y^2)} \, dy
$$
also diverges due to the heavy tails of the Cauchy distribution.

Therefore, the variance $\mathbb{V}(Y)$ is undefined for the standard Cauchy distribution because $\mathbb{E}(Y^2)$ does not exist.

## 3. The Median of $Y$

The median of a Cauchy distribution is the value $m$ such that
$$
\mathbb{P}(Y \leq m) = \frac{1}{2}.
$$
For the standard Cauchy distribution, which is symmetric about $y = 0$, the median is $0$.

Thus, the median of $Y$ is $0$.
