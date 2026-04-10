# Probability Distributions — Complete Lesson Notes

> These notes cover every task in Task List 03.
> Each section gives you: the concept in plain language, all formulas with symbols explained,
> the most important observation, likely professor questions with model answers,
> and a prepared script for presenting during the lesson.

---

# PART 1 — Core Terminology & Symbol Glossary

---

## The Five Distributions — When to Use Each

| Distribution | Keyword | Use when |
|---|---|---|
| **Binomial** | "fixed $n$ trials" | counting successes in $n$ independent trials, 2 outcomes |
| **Hypergeometric** | "without replacement" | drawing from a finite population, no replacement |
| **Geometric** | "first success" | counting trials until the first success occurs |
| **Poisson** | "rate $\lambda$" | counting events arriving in a time or space interval |
| **Multinomial** | "more than 2 categories" | generalisation of binomial to $r \geq 2$ outcome types |

---

## Master Symbol Glossary

| Symbol | Name | Meaning |
|---|---|---|
| $n$ | number of trials | total independent repetitions of the experiment |
| $k$ | count of successes | how many times the event of interest occurred |
| $p$ | success probability | probability of success on one trial |
| $q = 1-p$ | failure probability | probability of failure on one trial |
| $N$ | population size | total objects in the finite population |
| $K$ | successes in population | how many "special" objects exist in the whole population |
| $n$ (hyper) | sample size | how many objects we draw from the population |
| $\lambda$ | lambda — rate | average number of events per interval (Poisson) |
| $e$ | Euler's number | $e \approx 2.71828$, base of natural logarithm |
| $r$ | number of categories | how many distinct outcome types (Multinomial) |
| $k_i$ | count of category $i$ | how many trials produced outcome type $i$ |
| $p_i$ | probability of category $i$ | probability of one trial falling in category $i$ |
| $X$ | random variable | numerical outcome of the experiment |
| $P(X=k)$ | probability mass function | probability that $X$ takes value exactly $k$ |
| $E[X]$ | expected value | average value of $X$ over many repetitions |
| $\text{Var}(X)$ | variance | spread of $X$ around its mean |

---

## All Formulas in One Place

$$\textbf{Binomial:} \quad P(X=k) = \binom{n}{k} p^k (1-p)^{n-k}$$

$$E[X] = np \qquad \text{Var}(X) = np(1-p)$$

---

$$\textbf{Hypergeometric:} \quad P(X=k) = \frac{\dbinom{K}{k}\dbinom{N-K}{n-k}}{\dbinom{N}{n}}$$

$$E[X] = n\frac{K}{N} \qquad \text{Var}(X) = n\frac{K}{N}\frac{N-K}{N}\frac{N-n}{N-1}$$

---

$$\textbf{Geometric:} \quad P(X=k) = (1-p)^{k-1} \cdot p$$

$$E[X] = \frac{1}{p} \qquad \text{Var}(X) = \frac{1-p}{p^2}$$

---

$$\textbf{Poisson:} \quad P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}$$

$$E[X] = \lambda \qquad \text{Var}(X) = \lambda$$

---

$$\textbf{Multinomial:} \quad P(X_1=k_1,\ldots,X_r=k_r) = \frac{n!}{k_1!\cdots k_r!}\, p_1^{k_1}\cdots p_r^{k_r}$$

---

## The Three Power Tools

These solve almost every hard problem:

**Tool 1 — Complement**
$$P(\text{at least one}) = 1 - P(\text{none})$$
Use when you see: *"at least one"*, *"at least two"*, *"no later than"*

**Tool 2 — Independent trials multiply**
$$P(A \cap B) = P(A) \cdot P(B) \quad \text{when } A, B \text{ independent}$$
Use when: trials are independent and you need a sequence of results

**Tool 3 — Scale $\lambda$ with time**
$$\lambda_t = \lambda \cdot t \quad \text{(Poisson only)}$$
Use when the time window changes from what is given

---

# PART 2 — Task-by-Task Notes

---

## Task 1 — Binomial Model (Quality Control)

### What this task is about

We introduce the Binomial model through the simplest possible concrete example:
inspecting 3 screws where each is independently good or defective with fixed probability $p$.

### Easy Approach

Think of the experiment as a sequence of coin flips — except instead of H/T we have G/D.
With 3 flips there are $2^3 = 8$ outcomes. List them all, assign probabilities by multiplying individual probabilities, and observe the pattern.

### Key Concepts

**Bernoulli trial** — any experiment with exactly two possible outcomes (success / failure).
A single screw inspection is one Bernoulli trial.

**Binomial experiment** — repeating the same Bernoulli trial $n$ times independently.
Inspecting 3 screws is a Binomial experiment with $n = 3$.

**Why do we multiply probabilities?**
Because inspections are **independent** — the result of screw 1 tells us nothing about screw 2.
For independent events: $P(A \cap B) = P(A) \cdot P(B)$.

**What does $\binom{n}{k}$ count in the Binomial formula?**
The number of different sequences of $n$ trials that contain exactly $k$ successes.
For $k=1$ in $n=3$: the defective screw can be in position 1, 2, or 3 — that is $\binom{3}{1} = 3$ sequences.

### Most Important Observation

> **"Success" does not mean "good outcome."**
> In probability, success = the event we are counting.
> Here we count defectives, so defective = success.
> This is a naming convention, not a value judgement.

The Binomial formula is essentially:

$$P(X=k) = \underbrace{\binom{n}{k}}_{\text{how many sequences}} \times \underbrace{p^k}_{\text{prob. of } k \text{ successes}} \times \underbrace{(1-p)^{n-k}}_{\text{prob. of } n-k \text{ failures}}$$

### Four Conditions — Memorise These

1. **Fixed $n$** — number of trials decided in advance
2. **Two outcomes** — success or failure only
3. **Constant $p$** — same probability every trial
4. **Independent** — one trial does not affect another

### Professor May Ask

**Q: Why does the sum $q^3 + 3q^2p + 3qp^2 + p^3 = 1$?**
A: Because this is the binomial expansion of $(q+p)^3 = 1^3 = 1$.
The coefficients 1, 3, 3, 1 are exactly $\binom{3}{0}, \binom{3}{1}, \binom{3}{2}, \binom{3}{3}$.
This confirms all probabilities sum to 1.

**Q: What happens if the screws are not independent?**
A: The Binomial model breaks down. For example, if a machine fault causes consecutive screws to all be defective together, successive results are correlated — we cannot simply multiply probabilities.

**Q: How does the distribution change as $p$ increases?**
A: The distribution shifts right — higher values of $k$ become more probable.
At $p = 0.5$ the distribution is symmetric. At $p > 0.5$ it is skewed left.

### 🎤 Presentation Script

*"In Task 1 we build the Binomial model from scratch by looking at 3 screws, each independently defective with probability $p$. I start by writing down all 8 possible outcomes — three-letter sequences of G and D. Then I assign probabilities by multiplying, because the inspections are independent. For example, GDG has probability $q \cdot p \cdot q = q^2 p$. What I notice is that the probability only depends on how many defectives there are, not on their positions. That pattern — multiplying $p^k$ and $q^{n-k}$ then accounting for the number of orderings with $\binom{n}{k}$ — is exactly the Binomial formula. The key thing to remember is that success here means defective, which sounds wrong but is just the label for whatever we are counting."*

---

## Task 2 — Hypergeometric Model (Sampling from a Batch)

### What this task is about

We draw 4 components without replacement from a batch of 20 (5 defective, 15 good).
The key is understanding why this is NOT Binomial and how the formula counts favorable outcomes.

### Easy Approach

Think of the formula as three separate counting steps:
1. How many ways to choose the defective ones from the defective pool? → $\binom{K}{k}$
2. How many ways to choose the good ones from the good pool? → $\binom{N-K}{n-k}$
3. How many total samples exist? → $\binom{N}{n}$

Divide favorable by total.

### Key Concept — Why NOT Binomial?

| Feature | Binomial | Hypergeometric |
|---|---|---|
| Replacement | With | **Without** |
| Draws | Independent | **Dependent** |
| $p$ stays constant | Yes | **No — changes each draw** |

After drawing one defective component, only 4 defective remain out of 19 total.
The probability is no longer $5/20$ — it changed to $4/19$.
Dependent draws → cannot use Binomial → use Hypergeometric.

### The Formula Broken Down

$$P(X=k) = \frac{\binom{K}{k} \cdot \binom{N-K}{n-k}}{\binom{N}{n}}$$

| Part | What it counts |
|---|---|
| $\binom{K}{k}$ | ways to pick $k$ defectives from the $K$ defective ones |
| $\binom{N-K}{n-k}$ | ways to pick the remaining $n-k$ good ones from the $N-K$ good ones |
| $\binom{N}{n}$ | all possible samples of size $n$ from the full $N$ |

The numerator counts favorable outcomes. The denominator counts all outcomes. This is classical probability: $P = \text{favorable} / \text{total}$.

### Most Important Observation

> **The 5% rule:** If $n/N < 0.05$ (sample is less than 5% of population), the hypergeometric is well approximated by Binomial with $p = K/N$. Here $4/20 = 20\%$ — too large to approximate. We must use hypergeometric.

### Professor May Ask

**Q: Why does the hypergeometric have a finite maximum for $k$?**
A: You can only draw as many defectives as exist — so $k \leq \min(n, K)$.
You also cannot draw more good components than exist — so $k \geq \max(0, n-(N-K))$.
These bounds come from the population constraints.

**Q: What is the expected number of defectives in the sample?**
A: $E[X] = n \cdot \frac{K}{N} = 4 \cdot \frac{5}{20} = 1$. We expect on average 1 defective in a sample of 4 from a batch that is 25% defective.

**Q: How do you verify your distribution table is correct?**
A: Check that all probabilities sum to 1: $1365 + 2275 + 1050 + 150 + 5 = 4845 = \binom{20}{4}$ ✓

### 🎤 Presentation Script

*"Task 2 introduces the Hypergeometric distribution. The setup looks similar to Task 1 — we are counting defective items — but there is one crucial difference: we draw without replacement. That single word changes everything. Without replacement, each draw changes what remains in the warehouse. After pulling out one defective component, only 4 defective ones remain among 19. So the probability of success changes with every draw — the trials are dependent — and we cannot use Binomial. Instead, I use the Hypergeometric formula, which works by pure counting: how many ways can I pick exactly $k$ defectives from the defective pool, times how many ways to fill the rest from the good pool, divided by all possible samples."*

---

## Task 3 — Geometric Model (Waiting for the First Event)

### What this task is about

We inspect pages until the first error appears. The number of pages inspected is the random variable. The experiment has no fixed endpoint — it ends when the first success occurs.

### Easy Approach

Build the formula from logic:
- First error on page $k$ means pages 1 through $k-1$ were all correct, then page $k$ had an error.
- Each page is independent.
- Probability = $(1-p)^{k-1} \cdot p$

That's it. There is nothing more to the formula.

### Key Concept — The Infinite Sample Space

$$\Omega = \{E,\ CE,\ CCE,\ CCCE,\ \ldots\}$$

The sample space is **countably infinite** — theoretically you could check millions of pages without finding an error. This is fine mathematically because even though the sum has infinitely many terms, it converges to 1:

$$\sum_{k=1}^{\infty}(1-p)^{k-1}p = 1$$

This is a geometric series (which is also where the distribution gets its name).

### Most Important Observation — The Memoryless Property

> **The geometric distribution has no memory.**
>
> If you have already checked 10 pages with no error, your situation is exactly the same as someone who just started. The past gives no information about the future.
>
> Formally: $P(X > m+n \mid X > m) = P(X > n)$

This is unique to the geometric distribution among discrete distributions.

### Professor May Ask

**Q: What is the expected number of pages until the first error?**
A: $E[X] = \frac{1}{p}$. If $p = 0.1$, we expect to check $\frac{1}{0.1} = 10$ pages on average before the first error. This is intuitive — if errors are rare, we wait longer.

**Q: How is the geometric different from the binomial?**
A: Binomial has a fixed number of trials $n$ and counts successes. Geometric has no fixed $n$ — it counts trials until the first success. They are answers to opposite questions.

**Q: Why is the geometric series sum equal to 1?**
A: $\sum_{k=1}^{\infty}(1-p)^{k-1}p = p \cdot \frac{1}{1-(1-p)} = \frac{p}{p} = 1$. The formula $\sum_{k=0}^{\infty}r^k = \frac{1}{1-r}$ for $|r|<1$ applies with $r = 1-p$.

### 🎤 Presentation Script

*"Task 3 is about waiting. Instead of asking 'how many defectives in 10 trials', we ask 'how many pages until the first error'. The number of pages inspected is now the random variable, and it can be any positive integer — 1, 2, 3, and so on to infinity. The formula is simple to derive from first principles: to get the first error on page $k$, pages 1 to $k-1$ must be correct and page $k$ must be wrong. Multiply those independent probabilities and you get $(1-p)^{k-1} \cdot p$. One property of this distribution that is worth highlighting is the memoryless property — after any number of error-free pages, the distribution of future waiting time is the same as at the beginning. The past tells you nothing about when the next error will arrive."*

---

## Task 4 — Poisson Model (Arrival of Events)

### What this task is about

We count random events (error reports) arriving in a fixed time window.
There is no fixed number of trials — events happen spontaneously at a constant average rate $\lambda$.

### Easy Approach

The Poisson distribution has one parameter: $\lambda$ (the average rate).
Once you know $\lambda$ for your interval, plug into:

$$P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}$$

The only "trick" is: if the time window changes, scale $\lambda$ proportionally first.

### Key Concept — What is $\lambda$?

$\lambda$ (lambda) is the **average number of events per interval**. It is both the mean AND the variance of the Poisson distribution.

$$E[X] = \lambda \qquad \text{Var}(X) = \lambda$$

This is a special property of the Poisson — no other common distribution has mean equal to variance.

### Scaling $\lambda$

$$\lambda_t = \lambda \cdot t$$

| Original | Time window | New $\lambda$ |
|---|---|---|
| 3 per hour | 2 hours | 6 |
| 3 per hour | 30 min | 1.5 |
| 5 per hour | 1 hour | 5 |
| 5 per hour | 12 min | 1 |

### Most Important Observation

> **Poisson as a limit of Binomial:**
> When $n$ is very large and $p$ is very small, but $np = \lambda$ stays fixed,
> the Binomial distribution converges to Poisson.
> This is why Poisson works for rare events that can theoretically happen many times
> (phone calls, radioactive decays, website requests).

### Professor May Ask

**Q: Why is $P(X=0) = e^{-\lambda}$?**
A: Substitute $k=0$: $P(X=0) = \frac{\lambda^0 e^{-\lambda}}{0!} = \frac{1 \cdot e^{-\lambda}}{1} = e^{-\lambda}$.
This is the probability of receiving zero events — it decreases exponentially as $\lambda$ grows.

**Q: Why does Var$(X) = \lambda$ for the Poisson distribution?**
A: This is a mathematical consequence of the Poisson's derivation as a limit of Binomials with $np = \lambda$ and $p \to 0$. The variance $np(1-p) \to np = \lambda$.

**Q: What is the most probable value of $X$?**
A: The mode of Poisson$(\lambda)$ is $\lfloor \lambda \rfloor$ (floor of $\lambda$). When $\lambda$ is an integer, both $\lambda$ and $\lambda-1$ are modes — the distribution has two equally likely most probable values.

### 🎤 Presentation Script

*"Task 4 introduces the Poisson distribution, which models random arrivals. The setup is different from everything before — there is no experiment with a fixed number of trials. Instead, events arrive spontaneously in a time window, and we count how many. The entire distribution is determined by just one number: $\lambda$, the average rate. For this problem $\lambda = 3$ reports per hour. The formula $P(X=k) = \lambda^k e^{-\lambda} / k!$ gives the probability of exactly $k$ arrivals. Two things to emphasise: first, $e^{-\lambda}$ is the normalising constant that makes all probabilities sum to 1. Second, $\lambda$ scales linearly with time — if the window changes from 1 hour to 2 hours, $\lambda$ doubles to 6."*

---

## Task 5 — Multinomial Model (Categories of Outcomes)

### What this task is about

Rolling a die 5 times, grouping results into 3 categories (small/medium/large).
The Multinomial is the natural generalization of the Binomial to more than 2 outcomes.

### Easy Approach

The Multinomial formula has two parts:

**Part 1 — the multinomial coefficient** $\frac{n!}{k_1! k_2! k_3!}$

This is identical to "permutations with repeated elements" from combinatorics.
It counts how many orderings of the $n$ trials produce the exact counts $(k_1, k_2, k_3)$.

**Part 2 — the probability** $p_1^{k_1} p_2^{k_2} p_3^{k_3}$

This is the probability of any one specific ordering (they are all equal by independence).

Multiply them together.

### Key Concept — Connection to Binomial

Set $r = 2$, $p_1 = p$, $p_2 = 1-p$:

$$\frac{n!}{k_1! k_2!} p^{k_1}(1-p)^{k_2} = \binom{n}{k_1} p^{k_1}(1-p)^{n-k_1}$$

This is exactly the Binomial formula. The Binomial is a special case of the Multinomial with $r = 2$.

### Most Important Observation

> **The multinomial coefficient is the same formula as "permutations with repeated elements."**
>
> Arranging 5 items where 3 are type S, 2 are type L, 1 is type M:
> $$\frac{5!}{3! \cdot 2! \cdot 1!} = 60 \text{ arrangements}$$
> This is not a coincidence — the multinomial coefficient literally counts the arrangements of a sequence.

### Professor May Ask

**Q: What must always be true about $p_1 + p_2 + \cdots + p_r$?**
A: It must equal 1. The categories are exhaustive (every outcome falls in exactly one category) and mutually exclusive (no outcome can be in two categories simultaneously). So the probabilities must sum to 1.

**Q: What must always be true about $k_1 + k_2 + k_3$?**
A: It must equal $n$. Every trial produces exactly one outcome, so the counts must sum to the total number of trials.

**Q: What is the expected number of "small" outcomes in 5 rolls?**
A: $E[X_1] = n \cdot p_1 = 5 \cdot \frac{1}{3} \approx 1.67$. Each $X_i$ follows a Binomial$(n, p_i)$ distribution marginally.

### 🎤 Presentation Script

*"Task 5 introduces the Multinomial distribution as a generalization of Binomial. Instead of two outcomes per trial, we now have three — we group die rolls into small (1–2), medium (3–4), and large (5–6). The formula has two parts. First, the multinomial coefficient $\frac{5!}{k_1! k_2! k_3!}$ — this counts how many orderings of 5 rolls produce the given counts, and it is the same formula as permutations with repeated elements from combinatorics. Second, the probability part $p_1^{k_1} p_2^{k_2} p_3^{k_3}$ — this is the probability of any one specific ordering. We multiply because each ordering has equal probability due to independence. Two constraints must always hold: the $p_i$ must sum to 1 (categories cover everything) and the $k_i$ must sum to $n$ (every trial is accounted for)."*

---

## Task 6 — Binomial Calculation

### What this task is about

$n = 10$, $p = 0.04$, $X \sim \text{Bin}(10, 0.04)$. Compute two probabilities.

### Easy Approach

**Exactly 2:** directly apply the Binomial formula.

**At least 1:** always use complement — computing $P(X=0)$ is one step vs. summing $P(X=1)$ through $P(X=10)$.

### Step-by-Step

$$P(X=2) = \binom{10}{2}(0.04)^2(0.96)^8 = 45 \times 0.0016 \times 0.7214 = 0.0519$$

$$P(X \geq 1) = 1 - P(X=0) = 1 - (0.96)^{10} = 1 - 0.6648 = 0.3352$$

### Most Important Observation

> **Always use complement for "at least one."**
> $P(X \geq 1) = 1 - P(X=0)$ converts 10 calculations into 1.
> This works for any distribution, not just Binomial.

### Professor May Ask

**Q: What is $\binom{10}{2}$ and what does it represent here?**
A: $\binom{10}{2} = 45$. It represents the number of ways exactly 2 of the 10 parts can be the defective ones — which 2 positions (out of 10) contain defectives.

**Q: Why is $(0.96)^8$ in the formula for $P(X=2)$?**
A: Because $n - k = 10 - 2 = 8$ parts must be good (not defective), each with probability $0.96$. Since they are independent, their probabilities multiply: $(0.96)^8$.

### 🎤 Presentation Script

*"Task 6 is a direct application of the Binomial formula. We have 10 parts, each defective with probability 0.04 independently. For exactly 2 defectives I apply the formula directly: $\binom{10}{2}$ gives 45 orderings, $(0.04)^2$ is the probability of 2 defectives, and $(0.96)^8$ is the probability that the other 8 are good. For at least one defective, I use the complement — the only way to have no defectives at all is if all 10 are good, which has probability $(0.96)^{10} = 0.665$. Subtracting from 1 gives $0.335$. This complement trick converts 10 separate calculations into just one."*

---

## Task 7 — Hypergeometric Calculation

### What this task is about

15 bulbs (12 working, 3 defective), draw 5 without replacement. Find $P(X=2)$.

### Easy Approach

Three numbers to compute: $\binom{3}{2}$, $\binom{12}{3}$, $\binom{15}{5}$. Then divide.

$$P(X=2) = \frac{\binom{3}{2}\binom{12}{3}}{\binom{15}{5}} = \frac{3 \times 220}{3003} = 0.2198$$

### Most Important Observation

> **$k$ cannot exceed the number of defective bulbs in the box.**
> We only have 3 defective bulbs, so $k \leq 3$ — even though we draw 5.
> The maximum is $\min(n, K) = \min(5, 3) = 3$.

### Professor May Ask

**Q: Why is the denominator $\binom{15}{5}$ and not $15^5$?**
A: Because we draw without replacement and order does not matter — we are forming a set of 5 bulbs, not a sequence. $\binom{15}{5}$ counts the number of distinct sets of 5 from 15.

**Q: Can we use Binomial as an approximation here?**
A: The sample is $5/15 = 33\%$ of the population — far above the 5% threshold. The Binomial approximation would be inaccurate. We must use Hypergeometric.

### 🎤 Presentation Script

*"Task 7 is a direct calculation using the Hypergeometric formula. The box has 15 bulbs: 12 working and 3 defective. We draw 5 without replacement. To find $P(X=2)$, I count: there are $\binom{3}{2} = 3$ ways to choose 2 of the 3 defective bulbs, times $\binom{12}{3} = 220$ ways to fill the remaining 3 spots from the working bulbs. The denominator is $\binom{15}{5} = 3003$, the total number of samples. Dividing gives approximately 22%. One thing to highlight: $k$ cannot exceed 3 here even though we draw 5, because there are only 3 defective bulbs in the box."*

---

## Task 8 — Geometric Calculation

### What this task is about

$p = 0.1$, compilations until first error. Compute $P(X=4)$ and $P(X \leq 3)$.

### Easy Approach

**Exactly on 4th:** plug $k=4$ into $(1-p)^{k-1} \cdot p$.

**No later than 3rd:** use complement — $P(X \leq 3) = 1 - (0.9)^3$.

### Step-by-Step

$$P(X=4) = (0.9)^3 \times 0.1 = 0.729 \times 0.1 = 0.0729$$

$$P(X \leq 3) = 1 - (0.9)^3 = 1 - 0.729 = 0.271$$

### Most Important Observation

> **The complement trick for Geometric is especially powerful:**
> $$P(X \leq k) = 1 - (1-p)^k$$
> The complement of "first success within $k$ trials" is "all $k$ trials fail."
> This gives a closed-form answer without summing any series.

### Professor May Ask

**Q: What is the expected number of compilations until the first error?**
A: $E[X] = \frac{1}{p} = \frac{1}{0.1} = 10$. On average, 10 compilations are needed.

**Q: Does knowing the first 3 compilations were error-free change anything about the 4th?**
A: No — this is the memoryless property. Each compilation is independent with $P(\text{error}) = 0.1$ regardless of history.

### 🎤 Presentation Script

*"Task 8 applies the Geometric distribution to program compilation. Each compilation independently fails with probability 0.1. For the first error on exactly the 4th compilation: the first three must be error-free and the fourth must fail. That gives $(0.9)^3 \times 0.1 = 0.0729$. For the error occurring no later than the 3rd compilation, I use the complement: instead of summing three terms, I note that the complement is 'all 3 compilations are error-free', which has probability $(0.9)^3 = 0.729$. Subtracting from 1 gives 0.271. The complement formula $P(X \leq k) = 1 - (1-p)^k$ is much faster than direct summation, especially for larger bounds."*

---

## Task 9 — Poisson Calculation

### What this task is about

$\lambda = 5$ requests per hour. Compute $P(X=3)$ and $P(X \geq 1)$.

### Easy Approach

Compute $e^{-5} = 0.006738$ once at the start — reuse it for all calculations.

**Exactly 3:** $\frac{5^3 \times 0.006738}{3!} = \frac{125 \times 0.006738}{6} = 0.1404$

**At least 1:** $1 - e^{-5} = 1 - 0.006738 = 0.9933$

### Most Important Observation

> **$P(X=0) = e^{-\lambda}$** — the probability of zero events.
> This is always the simplest Poisson probability to compute — just $e^{-\lambda}$.
> The complement gives "at least one event": $1 - e^{-\lambda}$.
> For large $\lambda$ this is very close to 1 — events are almost certain to occur.

### Professor May Ask

**Q: What does $e^{-5}$ represent intuitively?**
A: It is the probability that zero events occur in the interval. With an average of 5 per hour, receiving none is very unlikely: $e^{-5} \approx 0.0067 = 0.67\%$.

**Q: If we observed 0 requests this hour, what does that tell us about $\lambda$?**
A: It suggests $\lambda$ might be smaller than assumed — but even with $\lambda = 5$ there is a 0.67% chance of observing zero. A single observation is not enough to revise $\lambda$ significantly.

### 🎤 Presentation Script

*"Task 9 applies the Poisson distribution. We have $\lambda = 5$ requests per hour. The first thing I do is compute $e^{-5} \approx 0.006738$ — I will need this for every calculation. For exactly 3 requests: $\frac{5^3 \times e^{-5}}{3!} = \frac{125 \times 0.00674}{6} \approx 0.140$. For at least one request, I use the complement — zero requests has probability $e^{-5} \approx 0.0067$, so at least one has probability $0.9933$. With an average of 5 per hour, it is almost impossible to receive no requests at all — 99.3% of the time at least one will arrive."*

---

## Task 10 — Multinomial Calculation

### What this task is about

6 candy selections with replacement, three flavors (40%, 35%, 25%). Find $P(X_1=3, X_2=2, X_3=1)$.

### Easy Approach

Three steps:
1. Multinomial coefficient: $\frac{6!}{3!\,2!\,1!} = 60$
2. Probability part: $(0.40)^3 \times (0.35)^2 \times (0.25)^1 = 0.064 \times 0.1225 \times 0.25$
3. Multiply: $60 \times 0.00196 = 0.1176$

### Most Important Observation

> **The multinomial coefficient is "permutations with repeated elements."**
> Arranging the sequence S,S,S,L,L,M (3 identical S's, 2 identical L's, 1 M):
> $$\frac{6!}{3!\,2!\,1!} = 60$$
> These 60 orderings all have the same probability because trials are independent.
> We multiply 60 by that common probability.

### Professor May Ask

**Q: What must $k_1 + k_2 + k_3$ equal, and why?**
A: It must equal $n = 6$. Every selection produces exactly one candy flavor, so the counts across all categories must add up to the total number of selections.

**Q: What is the probability of getting all 6 strawberry?**
A: $\frac{6!}{6!\,0!\,0!}(0.40)^6(0.35)^0(0.25)^0 = 1 \times (0.40)^6 \approx 0.0041$. The coefficient is 1 because there is only one ordering of 6 identical strawberries.

### 🎤 Presentation Script

*"Task 10 is the final calculation task, applying the Multinomial distribution. We select 6 candies with replacement from a box with three flavors: 40% strawberry, 35% lemon, 25% mint. We want the probability of getting exactly 3 strawberry, 2 lemon, and 1 mint. First I check: $3+2+1=6$ ✓. Then I compute the multinomial coefficient: $\frac{6!}{3!\,2!\,1!} = 60$ — this is exactly the permutations-with-repeats formula from combinatorics, counting how many orderings of 6 selections produce these exact counts. Then the probability of any one such ordering: $(0.40)^3 \times (0.35)^2 \times (0.25)^1 \approx 0.00196$. Multiplying: $60 \times 0.00196 \approx 0.1176$. About 12% chance."*

---

# PART 3 — Exam Quick Reference

---

## Distribution Recognition Card

| You see this... | Use this |
|---|---|
| "inspects/tests $n$ items", "flips coin $n$ times", fixed $n$ | **Binomial** |
| "without replacement", "finite batch", "draws from box" | **Hypergeometric** |
| "until first success", "until first error", "waiting for" | **Geometric** |
| "per hour", "per page", "arrival rate", "on average $\lambda$" | **Poisson** |
| "three categories", "more than two outcomes per trial" | **Multinomial** |

---

## Complement Rule — Apply in These Situations

| Problem says... | Compute instead... |
|---|---|
| at least one | $1 - P(\text{none})$ |
| at least two | $1 - P(\text{none}) - P(\text{exactly one})$ |
| no later than $k$ | $1 - P(\text{later than } k) = 1 - (1-p)^k$ for Geometric |
| more than zero | $1 - P(X=0) = 1 - e^{-\lambda}$ for Poisson |

---

## Five Things to Say in Every Oral Answer

1. **Name the distribution** and state its parameter(s): *"$X$ follows a Binomial distribution with $n=10$ and $p=0.04$"*
2. **Verify the conditions**: *"The four Binomial conditions hold because..."*
3. **State the formula**: write it out with the specific values substituted
4. **Explain your strategy**: *"I use the complement because at-least-one problems are easier this way..."*
5. **Interpret the answer**: *"So there is a 33.5% chance that at least one part is defective, which is reasonable given..."*

---

## Common Mistakes to Avoid

| Mistake | Correct thinking |
|---|---|
| Using Binomial when sampling without replacement | Check: is the population finite and sample $> 5\%$ of it? → Hypergeometric |
| Forgetting to use complement for "at least one" | $P(X \geq 1) = 1 - P(X=0)$ always |
| Using old $\lambda$ when time window changes | Always rescale: $\lambda_t = \lambda \cdot t$ |
| Forgetting $0! = 1$ and $\lambda^0 = 1$ | $P(X=0) = e^{-\lambda}$ exactly |
| Confusing geometric $P(X=k)$ with $P(X \leq k)$ | $P(X=k) = (1-p)^{k-1}p$, $P(X \leq k) = 1-(1-p)^k$ |
| Not checking $k_1 + \cdots + k_r = n$ in Multinomial | Always verify the counts sum to $n$ before computing |