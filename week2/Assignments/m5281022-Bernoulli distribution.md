## 2. Events and Probabilities - Bernoulli distribution

**Lai Hui Shan**  
**m5281022**

Let us consider a Bernoulli distribution;

$$
\mathbb{P}(X=1)=p, \quad \mathbb{P}(X=0)=1-p. 
$$

### 1. The expectation $\mathbb{E}(X)$

**Ans:**

For a Bernoulli random variable $X$, which can take values 0 or 1, the expectation is computed as:

$$
\mathbb{E}(X) = \sum_{x} x \cdot \mathbb{P}(X = x)
$$

Since $X = 1$ with probability $p$ and $X = 0$ with probability $1-p$, we have:

$$
\mathbb{E}(X) = 1 \cdot \mathbb{P}(X=1) + 0 \cdot \mathbb{P}(X=0)
$$
$$
\mathbb{E}(X) = 1 \cdot p + 0 \cdot (1-p) = p
$$

Thus, the expectation of $X$ is:

$$
\mathbb{E}(X) = p
$$

### 2. The expectation $\mathbb{E}((X - \mathbb{E}(X))^2)$

**Ans:**

The quantity $\mathbb{E}((X - \mathbb{E}(X))^2)$ is the **variance** of $X$. Let’s compute it.

First, recall that $\mathbb{E}(X) = p$. The variance is defined as:

$$
\text{Var}(X) = \mathbb{E}((X - \mathbb{E}(X))^2)
$$

We can expand this expression as:

$$
\text{Var}(X) = \mathbb{E}(X^2) - (\mathbb{E}(X))^2
$$

For a Bernoulli distribution, since $X$ can only take values 0 or 1, we have $X^2 = X$, so $\mathbb{E}(X^2) = \mathbb{E}(X)$. Therefore:

$$
\text{Var}(X) = \mathbb{E}(X) - (\mathbb{E}(X))^2
$$
$$
\text{Var}(X) = p - p^2
$$

We can also factor this expression as:

$$
\text{Var}(X) = p(1 - p)
$$

Thus, the expectation $\mathbb{E}((X - \mathbb{E}(X))^2)$ is:

$$
\mathbb{E}((X - \mathbb{E}(X))^2) = p(1 - p)
$$

### 3. Denoting $S_n = X_1 + X_2 + \dots + X_n$ for Bernoulli IID $\{ X_n \}$, then $S_n$ becomes a binomial distribution. Prove it.

**Ans:**

To prove this, let’s first define $S_n = X_1 + X_2 + \dots + X_n$, where each $X_i$ is an independent and identically distributed (IID) Bernoulli random variable with probability $p$ of success ($X_i = 1$) and $1-p$ of failure ($X_i = 0$).

The random variable $S_n$ represents the sum of $n$ Bernoulli trials, which counts the number of successes (the number of times $X_i = 1$) in $n$ independent trials.

The probability mass function of a binomial distribution is given by:

$$
\mathbb{P}(S_n = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

Now, let’s show that $S_n$ follows this form:

- Each $X_i$ is Bernoulli distributed, so the probability of success in a single trial is $p$, and the probability of failure is $1 - p$.
- Since the $X_i$’s are independent, the probability of getting exactly $k$ successes (i.e., $S_n = k$) is the probability of choosing $k$ trials to be successes (which can happen in $\binom{n}{k}$ different ways), times the probability of $k$ successes ($p^k$) and $n-k$ failures $(1 - p)^{n-k}$.

Thus, the probability that $S_n = k$ is:

$$
\mathbb{P}(S_n = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

This is exactly the probability mass function of a binomial distribution with parameters $n$ and $p$.

Therefore, we have proven that $S_n$, the sum of $n$ IID Bernoulli random variables, follows a binomial distribution:

$$
S_n \sim \text{Binomial}(n, p)
$$