## 3. Random Variables and Probability Distributions - Random generator

**Lai Hui Shan**  
**m5281022**

Let $Z$ be a random variable with a uniform distribution on $[0, 1]$, and let $X$ be a continuous-valued random variable with cumulative distribution function $F_X$.

## 1. Why does the Distribution Function $F_X$ Have an Inverse Function $F_X^{-1}$?

For a continuous random variable $X$ with cumulative distribution function $F_X$, the function $F_X(x)$ is monotonic and strictly increasing on its support (the range of possible values for $X$). This monotonicity implies that for each $p \in (0, 1)$, there is a unique value $x$ such that $F_X(x) = p$. Therefore, $F_X$ has an inverse function $F_X^{-1}$, which satisfies
$$
F_X(F_X^{-1}(p)) = p, \quad p \in (0, 1).
$$
The inverse $F_X^{-1}$ allows us to "map" probabilities back to the corresponding values of $X$.

## 2. Proving $\mathbb{P}(Z \leq z) = F_X(F_X^{-1}(z)), \quad z \in \mathbb{R}$

Since $Z$ is a uniform random variable on $[0, 1]$, we have:
$$
\mathbb{P}(Z \leq z) = z, \quad 0 \leq z \leq 1.
$$

For $z \in (0, 1)$, let $X = F_X^{-1}(Z)$. Then the probability that $Z$ is less than or equal to some value $z$ is the probability that $X \leq F_X^{-1}(z)$:
$$
\mathbb{P}(Z \leq z) = \mathbb{P}(X \leq F_X^{-1}(z)).
$$

Since $F_X$ is the cumulative distribution function of $X$, we know that
$$
\mathbb{P}(X \leq F_X^{-1}(z)) = F_X(F_X^{-1}(z)).
$$
Thus, we have shown that:
$$
\mathbb{P}(Z \leq z) = F_X(F_X^{-1}(z)), \quad z \in (0, 1).
$$

## 3. Generating a Value of $X$ Using $U$

To generate a value of $X$ from a uniform random variable $U \sim U[0,1]$, we can use the inverse transform sampling method:
1. Generate a value $U$ from the uniform distribution on $[0, 1]$.
2. Compute $X = F_X^{-1}(U)$.

Since $U$ is uniform on $[0, 1]$ and $F_X^{-1}(U)$ maps uniformly distributed values to the distribution of $X$, the random variable $X = F_X^{-1}(U)$ will follow the distribution defined by $F_X$.

This method allows us to transform uniformly distributed values into samples from the distribution of $X$.
