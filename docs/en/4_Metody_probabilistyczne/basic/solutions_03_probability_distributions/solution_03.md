# Task 3 — Geometric Model (Waiting for the First Event)

## The Setup

A printing house inspects pages one by one. Each page has probability $p$ of containing a printing error. Pages are **independent** and the probability $p$ is the same for every page.

We keep inspecting pages until we find the **first error**, then stop.

---

## Step 1 — Describe the Random Experiment

This is fundamentally different from Tasks 1 and 2. There:
- the number of trials $n$ was **fixed** in advance

Here:
- we do **not know in advance** how many pages we will inspect
- we stop as soon as the first error appears
- the number of inspections is the **random variable** itself

> **The question changes from "how many successes in $n$ trials?" to "how many trials until the first success?"**

---

## Step 2 — Build the Sample Space $\Omega$

Let us label each page result: $E$ = error (success), $C$ = correct (no error, failure).

The possible outcomes are:

| Outcome | Meaning | $k$ |
|---|---|---|
| $E$ | error on page 1 | 1 |
| $CE$ | correct page 1, error on page 2 | 2 |
| $CCE$ | two correct pages, error on page 3 | 3 |
| $CCCE$ | three correct pages, error on page 4 | 4 |
| $\vdots$ | $\vdots$ | $\vdots$ |

$$\Omega = \{E,\ CE,\ CCE,\ CCCE,\ \ldots\}$$

> **This sample space is infinite.** In theory, we could inspect 1 million pages before finding the first error (extremely unlikely, but not impossible). That is why $k$ can be any positive integer: $k = 1, 2, 3, \ldots$

---

## Step 3 — Probability Distribution

### Building the formula from scratch

For the first error to appear on page $k$, two things must happen:

1. Pages $1, 2, \ldots, k-1$ must all be **correct** — each with probability $(1-p)$
2. Page $k$ must have an **error** — with probability $p$

Since pages are **independent**, we multiply:

$$\boxed{P(X = k) = (1-p)^{k-1} \cdot p} \qquad k = 1, 2, 3, \ldots$$

### Worked examples

| $k$ | Sequence | Probability |
|---|---|---|
| 1 | $E$ | $p$ |
| 2 | $CE$ | $(1-p) \cdot p$ |
| 3 | $CCE$ | $(1-p)^2 \cdot p$ |
| 4 | $CCCE$ | $(1-p)^3 \cdot p$ |
| $k$ | $\underbrace{CC\cdots C}_{k-1}E$ | $(1-p)^{k-1} \cdot p$ |

### Verification — all probabilities sum to 1

$$\sum_{k=1}^{\infty} (1-p)^{k-1} \cdot p = p \sum_{k=1}^{\infty} (1-p)^{k-1} = p \cdot \frac{1}{1-(1-p)} = \frac{p}{p} = 1 \checkmark$$

This uses the formula for an **infinite geometric series**: $\sum_{k=0}^{\infty} r^k = \frac{1}{1-r}$ for $|r| < 1$.

> This is also where the distribution gets its name — the probabilities form a **geometric sequence** with common ratio $(1-p)$.

---

## Step 4 — What is a Success?

$$\text{success} = \text{finding a page with a printing error}$$

We are waiting for this event, counting how many trials it takes.

---

## The Memoryless Property

The geometric distribution has a special and important property:

$$P(X > m + n \mid X > m) = P(X > n)$$

In plain words: **if the first $m$ pages had no error, the probability of needing more than $n$ additional pages is the same as if we had just started.**

> **Example:** Suppose the first 10 pages were all correct. The probability that we need more than 3 more pages is exactly the same as the probability of needing more than 3 pages from the very beginning. The process "forgets" its history.

This is called the **memoryless property** and it is unique to the geometric distribution among discrete distributions.

---

## Key Conditions for the Geometric Model

Use the Geometric distribution when **all three** conditions hold:

1. **Trials are independent** — each page is independent of all others
2. **Constant probability $p$** — the error probability is the same on every page
3. **We are counting trials until first success** — not counting successes in a fixed number of trials

> If you have a fixed number of trials → use **Binomial**  
> If you are waiting for the first success → use **Geometric**