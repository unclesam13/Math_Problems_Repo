# Task 10 — Multinomial Model (Calculation)

## The Setup

A box contains candies of three flavors:

| Flavor | Probability | Symbol |
|---|---|---|
| Strawberry | 40% | $p_1 = 0.40$ |
| Lemon | 35% | $p_2 = 0.35$ |
| Mint | 25% | $p_3 = 0.25$ |

We select **$n = 6$ candies with replacement** (the probabilities stay the same each time).

**Goal:** find the probability of getting exactly 3 strawberry, 2 lemon, 1 mint.

---

## Why Multinomial?

| Condition | Check |
|---|---|
| Fixed number of trials | ✓ exactly 6 selections |
| More than 2 outcome categories | ✓ 3 flavors |
| Constant probabilities per trial | ✓ with replacement, same each time |
| Independent trials | ✓ each selection is independent |
| Categories are exhaustive | ✓ $0.40 + 0.35 + 0.25 = 1$ |

All conditions hold → **Multinomial is the correct model.**

---

## Setting Up the Calculation

We want:

$$k_1 = 3 \text{ (strawberry)}, \quad k_2 = 2 \text{ (lemon)}, \quad k_3 = 1 \text{ (mint)}$$

**Check the constraint:** $k_1 + k_2 + k_3 = 3 + 2 + 1 = 6 = n$ ✓

---

## The Multinomial Formula

$$P(X_1 = 3,\, X_2 = 2,\, X_3 = 1) = \frac{6!}{3!\,2!\,1!} \times (0.40)^3 \times (0.35)^2 \times (0.25)^1$$

---

## Computing Step by Step

### Step 1 — Multinomial coefficient $\frac{6!}{3!\,2!\,1!}$

This counts the number of different **orderings** of 6 selections that give exactly (3 strawberry, 2 lemon, 1 mint).

$$\frac{6!}{3!\,2!\,1!} = \frac{720}{6 \times 2 \times 1} = \frac{720}{12} = 60$$

> **Why 60 orderings?** Think of it as arranging the sequence S,S,S,L,L,M (where S=strawberry, L=lemon, M=mint). How many distinct arrangements of these 6 letters exist? Since the 3 S's are identical and the 2 L's are identical, it's $\frac{6!}{3!\,2!\,1!} = 60$. This is the "permutations with repeated elements" formula.

### Step 2 — Probability of each specific ordering

Fix one particular ordering, e.g. S,S,S,L,L,M (first 3 are strawberry, next 2 are lemon, last 1 is mint). Its probability:

$$(0.40)^3 \times (0.35)^2 \times (0.25)^1$$

$$= 0.064 \times 0.1225 \times 0.25 = 0.00196$$

### Step 3 — Multiply coefficient by probability

Every one of the 60 orderings has exactly the same probability $0.00196$.

$$P = 60 \times 0.00196 = \boxed{0.1176}$$

---

## Full Calculation in One Block

$$P = \underbrace{\frac{6!}{3!\,2!\,1!}}_{= 60} \times \underbrace{(0.40)^3}_{= 0.064} \times \underbrace{(0.35)^2}_{= 0.1225} \times \underbrace{(0.25)^1}_{= 0.25}$$

$$= 60 \times 0.064 \times 0.1225 \times 0.25 = \boxed{0.1176}$$

There is approximately an **11.76% chance** of getting exactly 3 strawberry, 2 lemon, and 1 mint candy.

---

## Intuition Check

The expected number of each flavor in 6 draws:

| Flavor | Expected count | We want |
|---|---|---|
| Strawberry | $6 \times 0.40 = 2.4$ | 3 |
| Lemon | $6 \times 0.35 = 2.1$ | 2 |
| Mint | $6 \times 0.25 = 1.5$ | 1 |

We are asking for a result close to (but not exactly at) the expected values — so a probability around 10–15% is reasonable. ✓

---

## What Changes if the Probabilities Were Equal?

If all three flavors had probability $\frac{1}{3}$:

$$P = \frac{6!}{3!\,2!\,1!} \times \left(\frac{1}{3}\right)^3 \times \left(\frac{1}{3}\right)^2 \times \left(\frac{1}{3}\right)^1 = 60 \times \left(\frac{1}{3}\right)^6 = \frac{60}{729} \approx 0.0823$$

The multinomial coefficient stays the same — only the probability part changes. This is a useful check: if you change the $p_i$ values but keep the $k_i$ values fixed, only the probability part of the formula changes.

---

## Summary

| Step | What we computed | Value |
|---|---|---|
| Multinomial coefficient | number of orderings giving (3,2,1) | 60 |
| $(0.40)^3$ | prob. all 3 strawberry draws succeed | 0.064 |
| $(0.35)^2$ | prob. both lemon draws succeed | 0.1225 |
| $(0.25)^1$ | prob. the one mint draw succeeds | 0.25 |
| **Final answer** | **total probability** | **0.1176** |