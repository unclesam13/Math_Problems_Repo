# Task 8 — Geometric Model (Calculation)

## The Setup

- Each compilation has probability $p = 0.1$ of producing an error
- Each compilation is **independent**
- We compile until the **first error** appears

$$X = \text{number of compilations until the first error}$$
$$X \sim \text{Geom}(0.1)$$

---

## Why Geometric?

| Condition | Check |
|---|---|
| Independent trials | ✓ compilations are independent |
| Constant probability | ✓ $p = 0.1$ for every compilation |
| Counting until first success | ✓ we stop at the first error |
| Number of trials is NOT fixed | ✓ we don't know how many compilations we'll need |

All conditions hold → **Geometric is the correct model.**

---

## The Geometric Formula

For the first error to appear on the $k$-th compilation:
- the first $k-1$ compilations must be **error-free**
- the $k$-th compilation must have an **error**

$$\boxed{P(X = k) = (1-p)^{k-1} \cdot p = (0.9)^{k-1} \cdot 0.1}$$

---

## Part 1 — First Error on the 4th Compilation

We want $P(X = 4)$.

**What must happen:**

| Compilation | Result | Probability |
|---|---|---|
| 1st | no error | $0.9$ |
| 2nd | no error | $0.9$ |
| 3rd | no error | $0.9$ |
| 4th | **error** | $0.1$ |

Since compilations are **independent**, multiply:

$$P(X = 4) = (0.9)^{4-1} \times 0.1 = (0.9)^3 \times 0.1$$

$$= 0.729 \times 0.1 = \boxed{0.0729}$$

There is a **7.29% chance** that the first error appears exactly on the 4th compilation.

---

## Part 2 — Error No Later Than the 3rd Compilation

We want $P(X \leq 3)$.

### Method 1 — Direct sum

$$P(X \leq 3) = P(X=1) + P(X=2) + P(X=3)$$

$$= 0.1 + (0.9)(0.1) + (0.9)^2(0.1)$$

$$= 0.1 + 0.09 + 0.081 = \boxed{0.271}$$

### Method 2 — Complement (cleaner)

"Error by the 3rd compilation" is the complement of "no error in the first 3 compilations":

$$P(X \leq 3) = 1 - P(X > 3) = 1 - P(\text{first 3 all error-free})$$

$$= 1 - (0.9)^3 = 1 - 0.729 = \boxed{0.271} \checkmark$$

> **Method 2 is much faster when the bound is large.** For example, $P(X \leq 10) = 1 - (0.9)^{10}$ takes one calculation instead of summing 10 terms.

---

## Summary of Results

| Event | Probability |
|---|---|
| First error on exactly the 4th compilation | $0.0729 \approx 7.3\%$ |
| First error no later than the 3rd compilation | $0.271 \approx 27.1\%$ |
| First error after the 3rd compilation (complement) | $0.729 \approx 72.9\%$ |

---

## Quick Reference — Geometric Probabilities for $p = 0.1$

| $k$ | $P(X = k)$ | $P(X \leq k)$ |
|---|---|---|
| 1 | 0.1000 | 0.1000 |
| 2 | 0.0900 | 0.1900 |
| 3 | 0.0810 | 0.2710 |
| 4 | 0.0729 | 0.3439 |
| 5 | 0.0656 | 0.4095 |

> **Pattern:** $P(X = k)$ decreases geometrically (each term is $0.9$ times the previous). $P(X \leq k) = 1 - (0.9)^k$ increases toward 1.