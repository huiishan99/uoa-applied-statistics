## 3. Random Variables and Probability Distributions - Exponential function

**Lai Hui Shan**  
**m5281022**

For a positive $\lambda > 0$, we are given the function
$$
f(x) = e^{-\lambda x} 1_{[0, \infty)}(x), \quad x \in \mathbb{R},
$$
where $1_{[0, \infty)}(x)$ is the indicator function on the interval $[0, \infty)$.

### 1. Plot of $f(x)$

The function $f(x)$ is defined as:
- $f(x) = e^{-\lambda x}$ for $x \geq 0$.
- $f(x) = 0$ for $x < 0$.

This represents an exponentially decaying function for $x \geq 0$, starting from $f(0) = 1$ and approaching $0$ as $x \to \infty$.

A plot of $f(x)$ would show an exponential decay curve starting from $1$ at $x = 0$ and gradually decreasing towards $0$ as $x \to \infty$.

### 2. Computation of $\int_{0}^{\infty} f(x) \, dx$

We aim to compute the integral
$$
\int_{0}^{\infty} f(x) \, dx = \int_{0}^{\infty} e^{-\lambda x} \, dx.
$$

To solve this, we calculate the integral:
$$
\int_{0}^{\infty} e^{-\lambda x} \, dx = \left[ \frac{-e^{-\lambda x}}{\lambda} \right]_{0}^{\infty}.
$$

Evaluating this expression:
1. As $x \to \infty$, $e^{-\lambda x} \to 0$.
2. At $x = 0$, $e^{-\lambda \cdot 0} = 1$.

Thus, we have
$$
\int_{0}^{\infty} e^{-\lambda x} \, dx = \frac{1}{\lambda}.
$$

### 3. Computation of $\int_{0}^{\infty} e^{t x} f(x) \, dx$

Next, we compute the integral
$$
\int_{0}^{\infty} e^{t x} f(x) \, dx = \int_{0}^{\infty} e^{t x} e^{-\lambda x} \, dx.
$$

Simplifying the integrand:
$$
e^{t x} e^{-\lambda x} = e^{(t - \lambda) x}.
$$

Thus, the integral becomes
$$
\int_{0}^{\infty} e^{(t - \lambda) x} \, dx.
$$

We need to consider two cases:
1. If $t < \lambda$, the integral converges.
2. If $t \geq \lambda$, the integral diverges.

For $t < \lambda$, we compute the integral:
$$
\int_{0}^{\infty} e^{(t - \lambda) x} \, dx = \left[ \frac{e^{(t - \lambda) x}}{t - \lambda} \right]_{0}^{\infty}.
$$

Evaluating this:
1. As $x \to \infty$, $e^{(t - \lambda) x} \to 0$ because $t - \lambda < 0$.
2. At $x = 0$, $e^{(t - \lambda) \cdot 0} = 1$.

Thus, we have
$$
\int_{0}^{\infty} e^{t x} f(x) \, dx = \frac{1}{\lambda - t}, \quad \text{for } t < \lambda.
$$

If $t \geq \lambda$, the integral does not converge.

---
