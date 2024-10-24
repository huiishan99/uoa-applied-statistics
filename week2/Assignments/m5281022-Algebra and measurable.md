## 2. Events and Probabilities - Algebra and measurable

**Lai Hui Shan**  
**m5281022**

Let us consider that Omega is construct two different elements like Head or Tail:

$$
\Omega = \{H,T\}
$$

If you consider a collection of subsets, say $\mathcal{F}_0$.

### 1. What is $\mathcal{F}_0$?

**Ans:**

The collection $\mathcal{F}_0$ refers to the set of all possible subsets of $\Omega$. This collection is also called the **power set** of $\Omega$, often denoted as $\mathcal{P}(\Omega)$. For your set $\Omega = \{H, T\}$, the power set $\mathcal{F}_0$ will consist of all possible subsets of $\Omega$, including the empty set $\emptyset$ and the set $\Omega$ itself. So,

$$
\mathcal{F}_0 = \{\emptyset, \{H\}, \{T\}, \{H, T\}\}
$$

### 2. What is the number of elements in $\mathcal{F}_0$?

**Ans:**

The number of elements in $\mathcal{F}_0$ is the number of all possible subsets of $\Omega$. For any set with $n$ elements, the number of subsets (or elements of the power set) is $2^n$. In this case, $\Omega = \{H, T\}$ has 2 elements, so the number of subsets in $\mathcal{F}_0$ is:

$$
2^2 = 4
$$

Thus, there are 4 elements in $\mathcal{F}_0$: $\emptyset, \{H\}, \{T\}, \{H, T\}$.

### 3. If $\Omega$ is a finite $n$-element set, what is the number of elements in a collection of all subsets, and why?

**Ans:**

If $\Omega$ is a finite set with $n$ elements, the collection of all subsets of $\Omega$ (i.e., the power set of $\Omega$) will contain $2^n$ elements. This is because for each element in the set, you have two choices when forming a subset: either include the element or exclude it. Therefore, for $n$ elements, there are $2^n$ possible subsets.

For example:
- If $n = 1$ (e.g., $\Omega = \{H\}$), the power set contains $2^1 = 2$ subsets: $\emptyset$ and $\{H\}$.
- If $n = 2$ (as in the original case $\Omega = \{H, T\}$), the power set contains $2^2 = 4$ subsets.

In general, for any finite set $\Omega$ with $n$ elements, the number of elements in the power set is $2^n$.