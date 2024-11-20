## 4. Conditioning and Independent - Conditional Probability

**Lai Hui Shan**  
**m5281022**

### 1. Proof: Conditional Probability is a Probability Measure

Let $(\Omega, \mathcal{F}, \mathbb{P})$ be a probability space, and consider a fixed event $A \in \mathcal{F}$ with $\mathbb{P}(A) > 0$. Define the conditional probability $\mathbb{P}(B \mid A) = \frac{\mathbb{P}(B \cap A)}{\mathbb{P}(A)}$ for $B \in \mathcal{F}$.

We prove that $B \mapsto \mathbb{P}(B \mid A)$ satisfies the axioms of a probability measure:

#### Step 1: Non-negativity
For any $B \in \mathcal{F}$,
$$
\mathbb{P}(B \mid A) = \frac{\mathbb{P}(B \cap A)}{\mathbb{P}(A)} \geq 0
$$
since $\mathbb{P}(B \cap A) \geq 0$ and $\mathbb{P}(A) > 0$.

#### Step 2: Additivity for Disjoint Events
If $B_1, B_2 \in \mathcal{F}$ are disjoint ($B_1 \cap B_2 = \emptyset$),
$$
\mathbb{P}((B_1 \cup B_2) \mid A) = \frac{\mathbb{P}((B_1 \cup B_2) \cap A)}{\mathbb{P}(A)}.
$$
Using the fact that $B_1 \cap B_2 = \emptyset$,
$$
(B_1 \cup B_2) \cap A = (B_1 \cap A) \cup (B_2 \cap A),
$$
and since $B_1 \cap A$ and $B_2 \cap A$ are disjoint, we have
$$
\mathbb{P}((B_1 \cup B_2) \mid A) = \frac{\mathbb{P}(B_1 \cap A) + \mathbb{P}(B_2 \cap A)}{\mathbb{P}(A)} = \mathbb{P}(B_1 \mid A) + \mathbb{P}(B_2 \mid A).
$$

#### Step 3: Total Probability
For the whole space $\Omega$,
$$
\mathbb{P}(\Omega \mid A) = \frac{\mathbb{P}(\Omega \cap A)}{\mathbb{P}(A)} = \frac{\mathbb{P}(A)}{\mathbb{P}(A)} = 1.
$$

Thus, $\mathbb{P}(\cdot \mid A)$ is a probability measure on $(\Omega, \mathcal{F})$.

---

### 2. Proof: $\mathbb{P}(B \cup C \mid A) = \mathbb{P}(B \mid A) + \mathbb{P}(C \mid A)$

Given $B$ and $C$ are disjoint ($B \cap C = \emptyset$) and $\mathbb{P}(A) > 0$, we compute:
$$
\mathbb{P}(B \cup C \mid A) = \frac{\mathbb{P}((B \cup C) \cap A)}{\mathbb{P}(A)}.
$$
Since $B \cap C = \emptyset$,
$$
(B \cup C) \cap A = (B \cap A) \cup (C \cap A),
$$
and because $(B \cap A)$ and $(C \cap A)$ are disjoint, we have
$$
\mathbb{P}((B \cup C) \cap A) = \mathbb{P}(B \cap A) + \mathbb{P}(C \cap A).
$$
Therefore,
$$
\mathbb{P}(B \cup C \mid A) = \frac{\mathbb{P}(B \cap A) + \mathbb{P}(C \cap A)}{\mathbb{P}(A)} = \mathbb{P}(B \mid A) + \mathbb{P}(C \mid A).
$$

---

### 3. Example: Conditional Probabilities with Balls

**Scenario:** A bag contains red ($r$) and white ($w$) balls. Suppose $X$ represents the outcome of interest (e.g., a specific ball being chosen), and $Y_1, Y_2, Y_3$ represent sequential draws with results $r, r, w$ respectively. We compute:
$$
\mathbb{P}(X = b \mid Y_1 = r, Y_2 = r, Y_3 = w).
$$

Let us define:
- Total number of balls = $n_r + n_w$,
- Total ways to draw $r, r, w$.

#### Step 1: Define Sample Space
Each sequence corresponds to one outcome. Compute probabilities for $r, r, w$ given prior probabilities and update.

#### Step 2: Compute Conditional Probabilities
By the definition of conditional probability:
$$
\mathbb{P}(X = b \mid Y_1 = r, Y_2 = r, Y_3 = w) = \frac{\mathbb{P}(X = b \cap Y_1 = r, Y_2 = r, Y_3 = w)}{\mathbb{P}(Y_1 = r, Y_2 = r, Y_3 = w)}.
$$
Explicit calculations depend on specific numbers of $r$ and $w$.

---

### 4. Proof: Independence of $A^c$ and $B^c$

Given $A$ and $B$ are independent, $\mathbb{P}(A \cap B) = \mathbb{P}(A) \mathbb{P}(B)$.

To prove $A^c$ and $B^c$ are independent, we compute:
$$
\mathbb{P}(A^c \cap B^c) = \mathbb{P}((A \cup B)^c) = 1 - \mathbb{P}(A \cup B).
$$
By inclusion-exclusion,
$$
\mathbb{P}(A \cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cap B).
$$
Substituting independence,
$$
\mathbb{P}(A^c \cap B^c) = 1 - \big(\mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A) \mathbb{P}(B)\big).
$$
Simplify:
$$
\mathbb{P}(A^c \cap B^c) = (1 - \mathbb{P}(A))(1 - \mathbb{P}(B)) = \mathbb{P}(A^c) \mathbb{P}(B^c).
$$
Thus, $A^c$ and $B^c$ are independent.


