# Task 5 — Multinomial Model (Categories of Outcomes)

## The Setup

A die is rolled **5 times**. The outcomes are grouped into three categories:

| Category | Die outcomes | Probability |
|---|---|---|
| Small | 1, 2 | $p_1 = \frac{2}{6} = \frac{1}{3}$ |
| Medium | 3, 4 | $p_2 = \frac{2}{6} = \frac{1}{3}$ |
| Large | 5, 6 | $p_3 = \frac{2}{6} = \frac{1}{3}$ |

---

## Step 1 — Describe the Random Experiment

We repeat the same trial (roll a die) **5 times** independently. Each roll produces one of **three categories**.

> **This is the generalization of the Binomial model.**  
> Binomial: each trial has **2** outcomes (success/failure)  
> Multinomial: each trial has **$r \geq 2$** outcomes (multiple categories)

When $r = 2$, the Multinomial reduces exactly to the Binomial.

---

## Step 2 — Sample Space

We describe each outcome as a triple $(k_1, k_2, k_3)$ where:

- $k_1$ = number of rolls that fell in "small" (1–2)
- $k_2$ = number of rolls that fell in "medium" (3–4)
- $k_3$ = number of rolls that fell in "large" (5–6)

The constraint is that the counts must add up to the total number of rolls:

$$k_1 + k_2 + k_3 = 5, \qquad k_i \geq 0$$

> **Example outcomes:**  
> $(5, 0, 0)$ — all 5 rolls were small  
> $(2, 2, 1)$ — 2 small, 2 medium, 1 large  
> $(0, 0, 5)$ — all 5 rolls were large

The number of distinct outcomes in $\Omega$ is given by stars and bars:

$$|\Omega| = \binom{5 + 3 - 1}{3 - 1} = \binom{7}{2} = 21$$

---

## Step 3 — Multinomial Distribution

### The Formula

$$\boxed{P(X_1 = k_1,\, X_2 = k_2,\, X_3 = k_3) = \frac{n!}{k_1!\,k_2!\,k_3!} \cdot p_1^{k_1} \cdot p_2^{k_2} \cdot p_3^{k_3}}$$

where $k_1 + k_2 + k_3 = n = 5$.

### Where does each piece come from?

**The probability part** $p_1^{k_1} \cdot p_2^{k_2} \cdot p_3^{k_3}$:

Fix one specific ordering — say small, small, medium, medium, large (in that exact order). Its probability is:

$$p_1 \cdot p_1 \cdot p_2 \cdot p_2 \cdot p_3 = p_1^2 \cdot p_2^2 \cdot p_3^1$$

**The coefficient** $\frac{n!}{k_1!\,k_2!\,k_3!}$:

This counts how many different orderings of the 5 rolls produce exactly $(k_1, k_2, k_3)$. It is the **multinomial coefficient** — a generalization of $\binom{n}{k}$.

For example, with $(k_1, k_2, k_3) = (2, 2, 1)$:

$$\frac{5!}{2!\,2!\,1!} = \frac{120}{2 \times 2 \times 1} = 30 \text{ different orderings}$$

Each ordering gives the same probability $p_1^2 p_2^2 p_3^1$, so we multiply by 30.

> **Think of it this way:** the multinomial coefficient is exactly the "permutations with repeated elements" formula from combinatorics — we are arranging 5 rolls where $k_1$ are identical (all "small"), $k_2$ are identical (all "medium"), and $k_3$ are identical (all "large").

---

## Step 4 — Interpretation of Parameters

| Parameter | Symbol | Value | Meaning |
|---|---|---|---|
| Number of trials | $n$ | 5 | how many times the die is rolled |
| Category 1 probability | $p_1$ | $\frac{1}{3}$ | prob. of rolling 1 or 2 on each roll |
| Category 2 probability | $p_2$ | $\frac{1}{3}$ | prob. of rolling 3 or 4 on each roll |
| Category 3 probability | $p_3$ | $\frac{1}{3}$ | prob. of rolling 5 or 6 on each roll |
| Count of category 1 | $k_1$ | 0 to 5 | how many rolls produced a small number |
| Count of category 2 | $k_2$ | 0 to 5 | how many rolls produced a medium number |
| Count of category 3 | $k_3$ | 0 to 5 | how many rolls produced a large number |
| Multinomial coefficient | $\frac{n!}{k_1!\,k_2!\,k_3!}$ | varies | number of orderings producing $(k_1,k_2,k_3)$ |

**Required constraint on probabilities:**

$$p_1 + p_2 + p_3 = 1 \qquad \text{(the categories cover all possible outcomes)}$$

$$\frac{1}{3} + \frac{1}{3} + \frac{1}{3} = 1 \checkmark$$

---

## Relationship to Binomial

If we merge "medium" and "large" into one category "not small":

$$p_{\text{small}} = \frac{1}{3}, \qquad p_{\text{not small}} = \frac{2}{3}$$

The multinomial with $r = 2$ becomes:

$$P(X_1 = k_1,\, X_2 = k_2) = \frac{5!}{k_1!\,k_2!} \left(\frac{1}{3}\right)^{k_1} \left(\frac{2}{3}\right)^{k_2} = \binom{5}{k_1} \left(\frac{1}{3}\right)^{k_1} \left(\frac{2}{3}\right)^{5-k_1}$$

This is exactly $\text{Bin}(5, \frac{1}{3})$ — confirming that the Binomial is a special case of the Multinomial.

---

## Key Conditions for the Multinomial Model

Use the Multinomial distribution when:

1. **Fixed number of trials** $n$ — we roll exactly 5 times
2. **Each trial has the same $r$ possible categories** — every roll can be small, medium, or large
3. **Constant category probabilities** — $p_1, p_2, p_3$ are the same on every roll
4. **Independent trials** — each roll is independent of all others
5. **Categories are exhaustive and mutually exclusive** — every outcome belongs to exactly one category, and $p_1 + p_2 + \cdots + p_r = 1$