## 3. Random Variables and Probability Distributions - Distribution functions

**Lai Hui Shan**  
**m5281022**

### Part 1: Distribution Functions of Common PDFs

#### Uniform Distribution

For a uniform random variable $X$ on the interval $[a, b]$, the probability density function (pdf) is given by:
$$
f_X(x) = \frac{1}{b - a}, \quad a \leq x \leq b.
$$
The cumulative distribution function (CDF) $F_X(x)$ is calculated as:
$$
F_X(x) = P(X \leq x) = \int_{a}^{x} f_X(t) \, dt.
$$
Evaluating this integral, we find:
1. For $x < a$, $F_X(x) = 0$.
2. For $a \leq x \leq b$, 
   $$
   F_X(x) = \frac{x - a}{b - a}.
   $$
3. For $x > b$, $F_X(x) = 1$.

Thus, the CDF of a uniform distribution on $[a, b]$ is:
$$
F_X(x) = \begin{cases} 
      0, & x < a, \\
      \frac{x - a}{b - a}, & a \leq x \leq b, \\
      1, & x > b.
   \end{cases}
$$

#### Exponential Distribution

For an exponential random variable $X$ with rate parameter $\lambda > 0$, the pdf is:
$$
f_X(x) = \lambda e^{-\lambda x}, \quad x \geq 0.
$$
The CDF $F_X(x)$ is calculated as:
$$
F_X(x) = \int_{0}^{x} \lambda e^{-\lambda t} \, dt.
$$
Evaluating this integral,
$$
F_X(x) = \left[ -e^{-\lambda t} \right]_{0}^{x} = 1 - e^{-\lambda x}.
$$
Thus, the CDF of an exponential distribution is:
$$
F_X(x) = \begin{cases} 
      0, & x < 0, \\
      1 - e^{-\lambda x}, & x \geq 0.
   \end{cases}
$$

#### Normal Distribution

For a normal random variable $X$ with mean $\mu$ and variance $\sigma^2$, the pdf is:
$$
f_X(x) = \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(x - \mu)^2}{2 \sigma^2}}, \quad x \in \mathbb{R}.
$$
The CDF $F_X(x)$ is given by:
$$
F_X(x) = \int_{-\infty}^{x} f_X(t) \, dt = \int_{-\infty}^{x} \frac{1}{\sqrt{2 \pi \sigma^2}} e^{-\frac{(t - \mu)^2}{2 \sigma^2}} \, dt.
$$
This integral does not have a closed-form expression, so it is typically evaluated using numerical methods or tables. 

---

### Part 2: Line through $(1, 0)$ in a Random Direction

A line is drawn through the point $(1, 0)$ in a random direction. Let $(0, Y)$ be the point at which this line intersects the $Y$-axis. We aim to show that $Y$ has the standard Cauchy distribution with density
$$
f_Y(y) = \frac{1}{\pi (1 + y^2)}, \quad y \in \mathbb{R}.
$$

#### 1. Showing that $Y$ has the Cauchy Distribution

1. Let $\theta$ be the angle that the line makes with the positive $X$-axis, chosen uniformly over $[0, \pi]$.
2. The slope of the line is $\tan \theta$.
3. The line equation through $(1, 0)$ is:
   $$
   y = \tan \theta \cdot (x - 1).
   $$
4. Setting $x = 0$, we find the $y$-intercept:
   $$
   Y = -\tan \theta.
   $$
5. Since $\theta$ is uniformly distributed, $\tan \theta$ follows a standard Cauchy distribution.

Thus, $Y$ has the density
$$
f_Y(y) = \frac{1}{\pi (1 + y^2)}.
$$

#### 2. Proving that $1/Y$ has the Same Distribution as $Y$

1. The reciprocal property of the Cauchy distribution implies that if $Y$ has a standard Cauchy distribution, then so does $1/Y$.
2. Geometrically, rotating the line by $90^\circ$ around the origin swaps $Y$ with $1/Y$, preserving the Cauchy distribution due to the symmetric nature of the Cauchy density.

