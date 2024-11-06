## 3. Random Variables and Probability Distributions - Well-defined: expectation

**Lai Hui Shan**  
**m5281022**


Let $X$ be a random variable with density
$$
f_X(x) = C x^{-\alpha}, \quad x \in (0, \infty),
$$
where $\alpha > 0$ and $C$ is a normalizing constant to ensure the total probability integrates to 1 over $(0, \infty)$.

## Existence of the Expected Value $\mathbb{E}(X)$

The expectation $\mathbb{E}(X)$ is given by
$$
\mathbb{E}(X) = \int_{0}^{\infty} x \cdot f_X(x) \, dx = \int_{0}^{\infty} x \cdot C x^{-\alpha} \, dx = C \int_{0}^{\infty} x^{1 - \alpha} \, dx.
$$

The integral $\int_{0}^{\infty} x^{1 - \alpha} \, dx$ converges or diverges depending on the value of $\alpha$. We analyze this integral over two regions: near $x = 0$ and as $x \to \infty$.

### 1. Behavior as $x \to 0$

For convergence near $x = 0$, we require that the exponent $1 - \alpha$ does not make the integral diverge. The integral
$$
\int_{0}^{1} x^{1 - \alpha} \, dx
$$
converges if $1 - \alpha > -1$, which simplifies to
$$
\alpha < 2.
$$

### 2. Behavior as $x \to \infty$

For convergence as $x \to \infty$, we consider
$$
\int_{1}^{\infty} x^{1 - \alpha} \, dx.
$$
This integral converges if $1 - \alpha < -1$, which simplifies to
$$
\alpha > 2.
$$

### Conclusion on $\mathbb{E}(X)$

To satisfy both conditions for convergence, the expected value $\mathbb{E}(X)$ is defined if and only if
$$
\alpha > 2.
$$
If $\alpha \leq 2$, the integral defining $\mathbb{E}(X)$ diverges, and thus the expected value does not exist.

In summary:
- **If $\alpha > 2$**: The expected value $\mathbb{E}(X)$ exists.
- **If $\alpha \leq 2$**: The expected value $\mathbb{E}(X)$ does not exist due to divergence in the integral.
