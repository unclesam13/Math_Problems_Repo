# Task 4 — Poisson Model (Arrival of Events)

## The Setup

A web service receives on average **3 error reports per hour**.

We want to find the probability of receiving exactly $k$ reports in a 1-hour window.

---

## Step 1 — Describe the Random Experiment

We are counting the number of **random arrivals** in a **fixed time interval**.

This is different from all previous models:

| Previous models | Poisson model |
|---|---|
| We had a fixed number of trials $n$ | We have a fixed **time window** |
| We counted successes among $n$ trials | We count **events arriving** in the window |
| Each trial was a deliberate action | Events arrive **spontaneously** |

> **Typical Poisson scenarios:**  
> Phone calls arriving at a call center · Emails received per day · Customers entering a shop per hour · Typos per page · Radioactive particle decays per second · Website requests per minute

The key idea: events happen **randomly and independently** at a constant average rate.

---

## Step 2 — Sample Space $\Omega$

The number of reports in one hour can be any non-negative integer — there is no upper limit:

$$\Omega = \{0, 1, 2, 3, 4, \ldots\} = \mathbb{N}_0$$

> **Why no upper limit?** In principle, the service could receive 100 reports in one hour (extremely unlikely, but not impossible). Unlike the Binomial where $k \leq n$, the Poisson has no built-in ceiling.

---

## Step 3 — Probability Distribution Formula

$$\boxed{P(X = k) = \frac{\lambda^k \cdot e^{-\lambda}}{k!}} \qquad k = 0, 1, 2, \ldots$$

### Every symbol explained

| Symbol | Name | Value here | Meaning |
|---|---|---|---|
| $\lambda$ | lambda | 3 | average number of events per interval |
| $k$ | observed count | 0, 1, 2, ... | the value we are computing the probability for |
| $e$ | Euler's number | $\approx 2.71828$ | base of the natural logarithm |
| $e^{-\lambda}$ | decay factor | $e^{-3} \approx 0.0498$ | ensures all probabilities sum to 1 |
| $k!$ | $k$ factorial | varies | corrects for the ordering of $k$ identical events |

### Where does $e^{-\lambda}$ come from?

It is the normalising constant that makes all probabilities sum to 1:

$$\sum_{k=0}^{\infty} \frac{\lambda^k e^{-\lambda}}{k!} = e^{-\lambda} \sum_{k=0}^{\infty} \frac{\lambda^k}{k!} = e^{-\lambda} \cdot e^{\lambda} = 1 \checkmark$$

The last step uses the Taylor series expansion: $e^{\lambda} = \sum_{k=0}^{\infty} \frac{\lambda^k}{k!}$

---

## Step 4 — Interpret $\lambda$

$\lambda$ is the **average rate** — the expected number of events per interval.

**For this problem:** $\lambda = 3$ reports per hour.

### Scaling $\lambda$ to different time windows

$\lambda$ scales **linearly** with the length of the interval:

| Time window | $\lambda$ | Calculation |
|---|---|---|
| 1 hour | 3 | given |
| 2 hours | 6 | $3 \times 2$ |
| 30 minutes | 1.5 | $3 \times 0.5$ |
| 20 minutes | 1 | $3 \times \frac{1}{3}$ |
| 1 minute | 0.05 | $3 \times \frac{1}{60}$ |

> **Whenever the problem changes the time window, always rescale $\lambda$ first before computing anything.**

### Quick probability table for $\lambda = 3$

| $k$ | $P(X = k)$ | Approx |
|---|---|---|
| 0 | $e^{-3}$ | 0.0498 |
| 1 | $3e^{-3}$ | 0.1494 |
| 2 | $\frac{9}{2}e^{-3}$ | 0.2240 |
| 3 | $\frac{27}{6}e^{-3}$ | 0.2240 |
| 4 | $\frac{81}{24}e^{-3}$ | 0.1680 |
| 5 | $\frac{243}{120}e^{-3}$ | 0.1008 |

> Notice that $P(X=2) = P(X=3)$ — this happens because $\lambda = 3$ is an integer, so the distribution peaks at both $k = \lambda - 1$ and $k = \lambda$.

---

## Key Conditions for the Poisson Model

Use the Poisson distribution when:

1. **Events occur randomly** in a continuous interval (time, area, volume, length)
2. **Events are independent** — one report arriving does not affect when the next arrives
3. **Constant average rate** $\lambda$ — the rate does not change over time
4. **Two events cannot happen at exactly the same instant** (technically: probability of two simultaneous events is zero)

> **Poisson as a limit of Binomial:** The Poisson distribution can be derived as the limit of $\text{Bin}(n, p)$ when $n \to \infty$ and $p \to 0$ while $np = \lambda$ stays constant. This is why Poisson is often used as an approximation for Binomial when $n$ is large and $p$ is very small.