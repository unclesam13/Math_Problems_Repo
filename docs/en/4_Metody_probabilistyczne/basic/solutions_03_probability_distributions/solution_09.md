# Task 9 — Poisson Model (Calculation)

## The Setup

- Average rate: $\lambda = 5$ requests per hour
- Time window: 1 hour

$$X \sim \text{Poisson}(5)$$

$X$ = number of requests received in one hour.

---

## Why Poisson?

| Condition | Check |
|---|---|
| Counting events in a fixed interval | ✓ one hour window |
| Events occur randomly and independently | ✓ one request arriving doesn't affect others |
| Constant average rate | ✓ $\lambda = 5$ per hour |
| No fixed upper bound on count | ✓ any number of requests is possible |

All conditions hold → **Poisson is the correct model.**

---

## The Poisson Formula

$$P(X = k) = \frac{\lambda^k \cdot e^{-\lambda}}{k!} = \frac{5^k \cdot e^{-5}}{k!}$$

**Useful constant:** $e^{-5} = 0.006738$ (memorise or compute once, use repeatedly)

---

## Part 1 — Exactly 3 Requests

We want $P(X = 3)$.

$$P(X = 3) = \frac{5^3 \cdot e^{-5}}{3!}$$

### Computing step by step

**Step 1 — numerator $5^3$:**

$$5^3 = 125$$

**Step 2 — the constant $e^{-5}$:**

$$e^{-5} = 0.006738$$

**Step 3 — denominator $3!$:**

$$3! = 6$$

**Step 4 — multiply:**

$$P(X = 3) = \frac{125 \times 0.006738}{6} = \frac{0.8423}{6} = \boxed{0.1404}$$

There is approximately a **14.04% chance** of receiving exactly 3 requests in one hour.

---

## Part 2 — At Least One Request

We want $P(X \geq 1)$.

### Why use complement?

Direct calculation:

$$P(X \geq 1) = P(X=1) + P(X=2) + P(X=3) + \cdots$$

This is an **infinite sum**. We cannot compute it directly.

### Complement gives a one-line solution

The complement of "at least one request" is "zero requests":

$$P(X \geq 1) = 1 - P(X = 0)$$

**Computing $P(X = 0)$:**

$$P(X = 0) = \frac{5^0 \cdot e^{-5}}{0!} = \frac{1 \times e^{-5}}{1} = e^{-5} = 0.006738$$

> **Note:** $5^0 = 1$ and $0! = 1$ — both equal 1 by definition, so $P(X=0)$ is simply $e^{-\lambda}$.

**Final answer:**

$$P(X \geq 1) = 1 - e^{-5} = 1 - 0.006738 = \boxed{0.9933}$$

There is a **99.33% chance** of receiving at least one request in one hour.

---

## Intuition Check

With an average of 5 requests per hour:
- Receiving **zero** requests is extremely unlikely: only 0.67%
- Receiving **at least one** is almost certain: 99.33%

This makes perfect sense — if requests arrive at an average rate of 5 per hour, it would be very unusual for an entire hour to pass with no requests at all.

---

## Summary of Results

| Event | Probability |
|---|---|
| Exactly 3 requests | $0.1404 \approx 14.0\%$ |
| Zero requests (complement) | $0.0067 \approx 0.7\%$ |
| At least 1 request | $0.9933 \approx 99.3\%$ |

---

## Nearby Probabilities for Reference

| $k$ | $P(X = k)$ | Approx |
|---|---|---|
| 0 | $e^{-5}$ | 0.0067 |
| 1 | $5e^{-5}$ | 0.0337 |
| 2 | $\frac{25}{2}e^{-5}$ | 0.0842 |
| **3** | $\frac{125}{6}e^{-5}$ | **0.1404** |
| 4 | $\frac{625}{24}e^{-5}$ | 0.1755 |
| 5 | $\frac{3125}{120}e^{-5}$ | 0.1755 |

> $P(X=4) = P(X=5)$ because $\lambda = 5$ is an integer — the distribution peaks at $k = \lambda$ and $k = \lambda - 1$ simultaneously when $\lambda$ is a whole number.