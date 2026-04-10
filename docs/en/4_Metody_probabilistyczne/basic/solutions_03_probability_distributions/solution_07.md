# Task 7 — Hypergeometric Model (Calculation)

## The Setup

A box contains **15 light bulbs** in total:

- $N - K = 12$ working bulbs
- $K = 3$ defective bulbs

We draw **$n = 5$ bulbs without replacement**.

$$X = \text{number of defective bulbs in the sample}$$

---

## Why Hypergeometric?

| Condition | Check |
|---|---|
| Finite population | ✓ exactly 15 bulbs |
| Two types of objects | ✓ working / defective |
| Drawing without replacement | ✓ stated in the problem |
| Fixed sample size | ✓ exactly 5 drawn |

All conditions hold → **Hypergeometric is the correct model.**

> **Why not Binomial?** Because we draw **without replacement**. After each draw, the composition of the box changes. If the first bulb drawn is defective, then only 2 defective bulbs remain among 14 — the probability changes. Draws are **dependent**.

---

## The Hypergeometric Formula

$$P(X = k) = \frac{\dbinom{K}{k}\dbinom{N-K}{n-k}}{\dbinom{N}{n}} = \frac{\dbinom{3}{k}\dbinom{12}{5-k}}{\dbinom{15}{5}}$$

---

## Exactly 2 Defective Bulbs

We want $P(X = 2)$, so $k = 2$.

$$P(X = 2) = \frac{\dbinom{3}{2} \cdot \dbinom{12}{3}}{\dbinom{15}{5}}$$

### Computing step by step

**Step 1 — choose 2 defective bulbs from the 3 defective ones:**

$$\binom{3}{2} = 3$$

> There are 3 ways to choose which 2 of the 3 defective bulbs end up in our sample.

**Step 2 — choose the remaining 3 bulbs from the 12 working ones:**

$$\binom{12}{3} = \frac{12 \times 11 \times 10}{3!} = \frac{1320}{6} = 220$$

> We need $5 - 2 = 3$ more bulbs, and they must all come from the 12 working ones.

**Step 3 — count all possible samples of 5 from 15:**

$$\binom{15}{5} = \frac{15 \times 14 \times 13 \times 12 \times 11}{5!} = \frac{360{,}360}{120} = 3003$$

> This is the total number of equally likely samples — the denominator.

**Step 4 — compute the probability:**

$$P(X = 2) = \frac{3 \times 220}{3003} = \frac{660}{3003} = \boxed{0.2198}$$

There is approximately a **21.98% chance** of drawing exactly 2 defective bulbs.

---

## Visualising the Calculation

$$P(X=2) = \frac{\overbrace{\binom{3}{2}}^{\text{pick 2 defective}} \times \overbrace{\binom{12}{3}}^{\text{pick 3 working}}}{\underbrace{\binom{15}{5}}_{\text{all possible samples}}} = \frac{3 \times 220}{3003} \approx 0.2198$$

---

## Full Distribution for Context

| $k$ | $\binom{3}{k}$ | $\binom{12}{5-k}$ | $P(X=k)$ | Approx |
|---|---|---|---|---|
| 0 | 1 | $\binom{12}{5} = 792$ | $\frac{792}{3003}$ | 0.2638 |
| 1 | 3 | $\binom{12}{4} = 495$ | $\frac{1485}{3003}$ | 0.4945 |
| **2** | **3** | $\binom{12}{3} = 220$ | $\frac{660}{3003}$ | **0.2198** |
| 3 | 1 | $\binom{12}{2} = 66$ | $\frac{66}{3003}$ | 0.0220 |

**Verification:** $792 + 1485 + 660 + 66 = 3003 \checkmark$

> Notice $k$ cannot exceed 3 (we only have 3 defective bulbs) even though we draw 5. The maximum value of $k$ is always $\min(n, K) = \min(5, 3) = 3$.