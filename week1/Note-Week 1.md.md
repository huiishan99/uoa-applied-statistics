2024-10-03

---
##### **Question 1:**

$$\lim_{n \to \infty} \sum_{k=1}^{n} \frac{\lambda^k}{k!}=?$$

> **Ans =** $e^\lambda -1$

> [!Remark:]
>  $$\sum_{k=1}^{n} \frac{\lambda^k}{k!}=-\frac{\lambda^0}{0!}+\sum_{k=0}^{n} \frac{\lambda^k}{k!}\to e^{\lambda}-1$$

**References:**
- [Poisson distributer](https://en.wikipedia.org/wiki/Poisson_distribution)
- [Taylor series](https://en.wikipedia.org/wiki/Taylor_series)
---
##### **Question 2:**
$$\int_{-\infty}^{+\infty} \frac{x}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2} } dx =   ?$$
$$OR$$
$$\int_{-\infty}^{+\infty} \frac{x}{\sigma\sqrt{2\pi}}exp({-\frac{(x-\mu)^2}{2\sigma^2}}) dx =   ?$$


> **Ans =** $\mu$

> [!Remark:]
> $$ \int_{-\infty}^{\infty} \frac{x}{\sigma \sqrt{2 \pi}} \exp \left(-\frac{(x-\mu)^2}{2 \sigma^2}\right) d x = \mathbb{E}(X), \quad X \sim \mathcal{N}(\mu,\sigma^2).$$We need to prove $\mathbb{E}(X)=\mu$. Considering $z=(x-\mu)/\sigma$, we have….

**References:**
- [Normal Distribution](https://en.wikipedia.org/wiki/Normal_distribution)
---
**Materials:**
[[Basic Math.md]]