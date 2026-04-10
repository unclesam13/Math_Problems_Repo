# Task 1 — Binomial Model (Quality Control)

## The Setup

A factory produces screws. Each screw is either **good** or **defective**.

- The probability that any single screw is defective is $p$
- Each inspection is **independent** — what happened to the previous screw tells us nothing about the next one
- We inspect **3 screws** in a row

---

## Step 1 — Describe the Random Experiment

We are repeating the same trial (inspect one screw) **3 times** under identical conditions.

Each trial has exactly **two possible outcomes**:

| Symbol | Meaning |
|---|---|
| $D$ | defective screw |
| $G$ | good screw |

This is called a **Bernoulli trial** — any experiment with exactly two outcomes (success/failure, yes/no, defective/good).

---

## Step 2 — Build the Sample Space $\Omega$

Each outcome is an **ordered sequence of 3 letters**, one for each screw inspected.

We list all $2^3 = 8$ possibilities:

$$\Omega = \{GGG,\ GGD,\ GDG,\ DGG,\ GDD,\ DGD,\ DDG,\ DDD\}$$

> **Why ordered?** Because we inspect screw 1, then screw 2, then screw 3. The sequence $GDG$ (good, then defective, then good) is a different outcome from $DGG$ (defective first, then two good ones). The order records *when* each result happened.

---

## Step 3 — Assign Probabilities

Let $q = 1 - p$ be the probability that a screw is **good**.

Since inspections are **independent**, the probability of any sequence is the **product** of the individual probabilities.

For example:

$$P(GDG) = P(G) \cdot P(D) \cdot P(G) = q \cdot p \cdot q = q^2 p$$

The full table:

| Outcome | Number of defectives | Probability |
|---|---|---|
| $GGG$ | 0 | $q^3$ |
| $GGD$ | 1 | $q^2 p$ |
| $GDG$ | 1 | $q^2 p$ |
| $DGG$ | 1 | $q^2 p$ |
| $GDD$ | 2 | $q\,p^2$ |
| $DGD$ | 2 | $q\,p^2$ |
| $DDG$ | 2 | $q\,p^2$ |
| $DDD$ | 3 | $p^3$ |

**Verification** — all 8 probabilities must sum to 1:

$$q^3 + 3q^2p + 3qp^2 + p^3 = (q + p)^3 = 1^3 = 1 \checkmark$$

This works because $(q+p)^3$ expands by the **binomial theorem** — and the coefficients $1, 3, 3, 1$ are exactly $\binom{3}{0}, \binom{3}{1}, \binom{3}{2}, \binom{3}{3}$.

---

## Step 4 — Define Success

> **In probability, "success" means the event we are counting — not necessarily the desirable outcome.**

Here we are counting **defective screws**, so:

$$\text{success} = \text{finding a defective screw}$$

This feels counterintuitive at first — in real life, a defective screw is bad news. But in the mathematical model, "success" is simply the label for the outcome we track.

---

## The Binomial Random Variable

Let $X$ = number of defective screws in 3 inspections.

$$X \sim \text{Bin}(n,\, p) = \text{Bin}(3,\, p)$$

The probability of exactly $k$ defectives:

$$P(X = k) = \binom{3}{k} p^k (1-p)^{3-k} \qquad k = 0, 1, 2, 3$$

| $k$ | $\binom{3}{k}$ | $P(X = k)$ |
|---|---|---|
| 0 | 1 | $q^3$ |
| 1 | 3 | $3q^2p$ |
| 2 | 3 | $3qp^2$ |
| 3 | 1 | $p^3$ |

> **What does $\binom{3}{k}$ count?**  
> The number of different sequences of 3 inspections that contain exactly $k$ defectives.  
> For $k=1$: the defective screw can be in position 1, 2, or 3 — that is $\binom{3}{1} = 3$ sequences.

---

## Key Conditions for the Binomial Model

Use the Binomial distribution when **all four** conditions hold:

1. **Fixed number of trials** $n$ — we inspect exactly 3 screws, not "until we find one"
2. **Two outcomes per trial** — good or defective, nothing else
3. **Constant probability** $p$ — same for every screw
4. **Independent trials** — one screw's result does not affect another's

If any condition fails, the Binomial model does not apply.