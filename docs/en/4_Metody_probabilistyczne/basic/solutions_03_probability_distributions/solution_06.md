# Task 6 — Binomial Model (Calculation)

## The Setup

- Probability of a defective part: $p = 0.04$
- Probability of a good part: $q = 1 - p = 0.96$
- Number of parts inspected: $n = 10$
- Inspections are **independent**

$$X \sim \text{Bin}(10,\ 0.04)$$

$X$ = number of defective parts among the 10 inspected.

---

## Why Binomial?

Before computing anything, verify the four Binomial conditions:

| Condition | Check |
|---|---|
| Fixed number of trials | ✓ exactly 10 parts inspected |
| Two outcomes per trial | ✓ defective or good |
| Constant probability | ✓ $p = 0.04$ for every part |
| Independent trials | ✓ stated in the problem |

All four hold → **Binomial is the correct model.**

---

## The Binomial Formula

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k} = \binom{10}{k} (0.04)^k (0.96)^{10-k}$$

---

## Part 1 — Exactly 2 Defective Parts

We want $P(X = 2)$.

$$P(X = 2) = \binom{10}{2} (0.04)^2 (0.96)^8$$

### Computing step by step

**Step 1 — the binomial coefficient:**

$$\binom{10}{2} = \frac{10!}{2!\,8!} = \frac{10 \times 9}{2 \times 1} = 45$$

> This counts the number of ways exactly 2 of the 10 parts can be defective — which 2 positions out of 10 are the defective ones.

**Step 2 — the success probability raised to $k$:**

$$(0.04)^2 = 0.0016$$

> This is the probability that both chosen positions are defective.

**Step 3 — the failure probability raised to $n-k$:**

$$(0.96)^8 = 0.7214 \quad \text{(to 4 d.p.)}$$

> This is the probability that the remaining 8 parts are all good.

**Step 4 — multiply everything:**

$$P(X = 2) = 45 \times 0.0016 \times 0.7214 = \boxed{0.0519}$$

So there is approximately a **5.19% chance** of finding exactly 2 defective parts in 10.

---

## Part 2 — At Least One Defective Part

We want $P(X \geq 1)$.

### Why not compute directly?

Direct calculation would require:

$$P(X \geq 1) = P(X=1) + P(X=2) + P(X=3) + \cdots + P(X=10)$$

That is **10 separate terms**. Very tedious.

### Use the complement instead

The complement of "at least one defective" is "zero defectives":

$$P(X \geq 1) = 1 - P(X = 0)$$

**Computing $P(X = 0)$:**

$$P(X = 0) = \binom{10}{0} (0.04)^0 (0.96)^{10} = 1 \times 1 \times (0.96)^{10}$$

$$(0.96)^{10} = 0.6648 \quad \text{(to 4 d.p.)}$$

**Final answer:**

$$P(X \geq 1) = 1 - 0.6648 = \boxed{0.3352}$$

There is approximately a **33.52% chance** that at least one part is defective.

> **Intuition check:** With $p = 0.04$ and $n = 10$, we expect on average $np = 0.4$ defective parts. Finding at least one in a sample of 10 should be moderately likely — 33.5% seems reasonable.

---

## Summary of Results

| Event | Probability |
|---|---|
| Exactly 2 defective | $0.0519 \approx 5.2\%$ |
| At least 1 defective | $0.3352 \approx 33.5\%$ |
| Zero defective (complement) | $0.6648 \approx 66.5\%$ |

> **Always use complement for "at least one" problems.** It converts a sum of 10 terms into a single calculation.