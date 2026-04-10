# Task 2 — Hypergeometric Model (Sampling from a Batch)

## The Setup

A warehouse has **20 components** in total:

- $K = 5$ are **defective**
- $N - K = 15$ are **functional**

We draw **4 components without replacement** and count the defective ones.

---

## Step 1 — Describe the Random Experiment

We are selecting a **sample of 4** from a **finite population of 20**, where the population contains two types of objects (defective / functional).

The crucial word here is **without replacement** — once a component is drawn, it is not returned to the warehouse. This means:

- The draws are **not independent** — removing one component changes what remains
- The composition of the remaining population changes after each draw

> **This is what separates the Hypergeometric from the Binomial model.**  
> Binomial assumes draws are independent (with replacement or infinite population).  
> Hypergeometric is used exactly when draws are dependent (without replacement, finite population).

---

## Step 2 — Define the Random Variable

$$X = \text{number of defective components in our sample of 4}$$

$X$ is a random variable — its value depends on which 4 components happen to be drawn.

---

## Step 3 — Possible Values of $X$

$X$ can range from the **minimum** to the **maximum** number of defectives we could possibly draw:

- **Minimum:** $\max(0,\ n - (N-K)) = \max(0,\ 4 - 15) = 0$  
  We could draw 4 components and all of them be functional.

- **Maximum:** $\min(n,\ K) = \min(4,\ 5) = 4$  
  We could draw up to 4 defectives (since we only draw 4 and there are 5 defectives available).

$$X \in \{0, 1, 2, 3, 4\}$$

---

## Step 4 — Probability Distribution

### The Formula

$$\boxed{P(X = k) = \frac{\dbinom{K}{k}\dbinom{N-K}{n-k}}{\dbinom{N}{n}} = \frac{\dbinom{5}{k}\dbinom{15}{4-k}}{\dbinom{20}{4}}}$$

### Where does this formula come from?

Think of it as three counting steps:

| Part | What it counts | Value |
|---|---|---|
| $\binom{5}{k}$ | ways to choose $k$ defectives from the 5 defective ones | depends on $k$ |
| $\binom{15}{4-k}$ | ways to choose the remaining $4-k$ components from the 15 functional ones | depends on $k$ |
| $\binom{20}{4}$ | total ways to choose any 4 components from all 20 | $= 4845$ (fixed) |

The numerator counts **favorable outcomes** (samples with exactly $k$ defectives).  
The denominator counts **all possible samples**.

> **Why do we multiply $\binom{5}{k}$ and $\binom{15}{4-k}$?**  
> Because choosing the defectives and choosing the functional components are **independent choices** — we use the product rule. The total number of samples with exactly $k$ defectives is the product of the two counts.

### Computing $\binom{20}{4}$

$$\binom{20}{4} = \frac{20 \times 19 \times 18 \times 17}{4!} = \frac{116{,}280}{24} = 4{,}845$$

### Full Distribution Table

| $k$ | $\binom{5}{k}$ | $\binom{15}{4-k}$ | Numerator | $P(X=k)$ | Approx |
|---|---|---|---|---|---|
| 0 | 1 | $\binom{15}{4} = 1365$ | 1365 | $\frac{1365}{4845}$ | 0.2817 |
| 1 | 5 | $\binom{15}{3} = 455$ | 2275 | $\frac{2275}{4845}$ | 0.4696 |
| 2 | 10 | $\binom{15}{2} = 105$ | 1050 | $\frac{1050}{4845}$ | 0.2167 |
| 3 | 10 | $\binom{15}{1} = 15$ | 150 | $\frac{150}{4845}$ | 0.0309 |
| 4 | 5 | $\binom{15}{0} = 1$ | 5 | $\frac{5}{4845}$ | 0.0010 |

**Verification:**

$$1365 + 2275 + 1050 + 150 + 5 = 4845 \checkmark$$

All probabilities sum to $\frac{4845}{4845} = 1$ ✓

---

## Step 5 — What is a Success?

$$\text{success} = \text{drawing a defective component}$$

Just like in Task 1, "success" is the label for what we count — not a desirable outcome.

---

## Hypergeometric vs Binomial — Key Comparison

| Feature | Binomial | Hypergeometric |
|---|---|---|
| Replacement | With replacement | **Without replacement** |
| Population | Infinite (or very large) | **Finite** |
| Draws | Independent | **Dependent** |
| Formula | $\binom{n}{k}p^k(1-p)^{n-k}$ | $\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}$ |

> **Rule of thumb:** If the sample size $n$ is less than 5% of the population $N$, the hypergeometric distribution is well approximated by the binomial with $p = K/N$. Here $n/N = 4/20 = 20\%$ — too large to use the approximation, so we must use hypergeometric.