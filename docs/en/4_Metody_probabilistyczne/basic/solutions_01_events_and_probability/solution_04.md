# Solution 1 — Events and Probability

## Task 4 — Weekly Weather Observation


### Setup — Sample Space

From Task 4, each day is one of three states: Sunny ($S$), Cloudy ($C$), Rainy ($R$).

The full sample space for **7 independent days** is:

$$\Omega_7 = \{(w_1, w_2, w_3, w_4, w_5, w_6, w_7) : w_i \in \{S, C, R\}\}$$

$$|\Omega_7| = 3^7 = 2187$$

Each day is **independent** and each state occurs with equal probability $\tfrac{1}{3}$, so each elementary outcome has probability:

$$P(\omega) = \left(\frac{1}{3}\right)^7 = \frac{1}{2187}$$

We label the days: $w_1$ = Monday, $w_2$ = Tuesday, $w_3$ = Wednesday, $w_4$ = Thursday, $w_5$ = Friday, $w_6$ = Saturday, $w_7$ = Sunday.

---

## Event $A$ — Entire Weekend is Sunny

Both Saturday ($w_6$) and Sunday ($w_7$) must be $S$. The remaining 5 days are free.

$$A = \{(w_1,\ldots,w_7) : w_6 = S,\ w_7 = S\}$$

$$|A| = 3^5 = 243 \quad \text{(5 free days, 3 choices each)}$$

$$P(A) = \left(\frac{1}{3}\right)^2 = \frac{1}{9} \approx 11.11\%$$

---

## Event $B$ — Wednesday, Thursday, Friday All Rainy

$w_3 = R$, $w_4 = R$, $w_5 = R$. The remaining 4 days are free.

$$B = \{(w_1,\ldots,w_7) : w_3 = w_4 = w_5 = R\}$$

$$|B| = 3^4 = 81$$

$$P(B) = \left(\frac{1}{3}\right)^3 = \frac{1}{27} \approx 3.70\%$$

---

## Event $C$ — At Least One Sunny Day

Use the complement: no day is sunny means every day is either $C$ or $R$ (2 choices per day).

$$P(\text{no sunny day}) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187}$$

$$P(C) = 1 - \left(\frac{2}{3}\right)^7 = 1 - \frac{128}{2187} = \frac{2059}{2187} \approx 94.15\%$$

---

## Event $D$ — No Rainy Day During the Entire Week

Every day must be either $S$ or $C$ (2 choices per day):

$$D = \{(w_1,\ldots,w_7) : w_i \in \{S, C\} \text{ for all } i\}$$

$$|D| = 2^7 = 128$$

$$P(D) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187} \approx 5.85\%$$

---

## Event $E$ — Exactly Two Sunny Days

We need to choose **which 2 days** are sunny, while the remaining 5 days are each $C$ or $R$.

$$|E| = \binom{7}{2} \times 2^5 = 21 \times 32 = 672$$

$$P(E) = \binom{7}{2} \left(\frac{1}{3}\right)^2 \left(\frac{2}{3}\right)^5 = 21 \times \frac{1}{9} \times \frac{32}{243} = \frac{672}{2187} \approx 30.73\%$$

This follows the **Binomial distribution** $\text{Bin}(7, \tfrac{1}{3})$ with $k=2$ successes:

$$P(E) = \binom{7}{2}\left(\frac{1}{3}\right)^2\left(\frac{2}{3}\right)^5$$

---

## Additional Event

**Event $F$** — At least 4 days are the same weather state (any state).

Use inclusion-exclusion. Let $F_S$, $F_C$, $F_R$ be the events that at least 4 days are Sunny, Cloudy, Rainy respectively. These are mutually exclusive (a week cannot have $\geq 4$ sunny AND $\geq 4$ cloudy days simultaneously since $4+4=8>7$).

For any fixed state $X$, the number of outcomes with **exactly $k$** days of state $X$ is $\binom{7}{k} \cdot 2^{7-k}$, so:

$$P(\text{at least 4 days of state } X) = \sum_{k=4}^{7} \binom{7}{k} \left(\frac{1}{3}\right)^k \left(\frac{2}{3}\right)^{7-k}$$

Computing each term:

| $k$ | $\binom{7}{k}$ | $\left(\tfrac{1}{3}\right)^k\left(\tfrac{2}{3}\right)^{7-k}$ | Product |
|---|---|---|---|
| 4 | 35 | $\tfrac{1}{81} \cdot \tfrac{8}{27} = \tfrac{8}{2187}$ | $\tfrac{280}{2187}$ |
| 5 | 21 | $\tfrac{1}{243} \cdot \tfrac{4}{9} = \tfrac{4}{2187}$ | $\tfrac{84}{2187}$ |
| 6 | 7  | $\tfrac{1}{729} \cdot \tfrac{2}{3} = \tfrac{2}{2187}$ | $\tfrac{14}{2187}$ |
| 7 | 1  | $\tfrac{1}{2187}$ | $\tfrac{1}{2187}$ |

$$P(\text{at least 4 days of state } X) = \frac{280+84+14+1}{2187} = \frac{379}{2187}$$

Since the three states are symmetric and mutually exclusive for the "at least 4" condition:

$$P(F) = 3 \times \frac{379}{2187} = \frac{1137}{2187} = \frac{379}{729} \approx 51.99\%$$

---

## Summary Table

| Event | Description | Probability | Decimal |
|---|---|---|---|
| $A$ | Full weekend sunny | $\tfrac{1}{9}$ | 11.11% |
| $B$ | Wed–Fri all rainy | $\tfrac{1}{27}$ | 3.70% |
| $C$ | At least one sunny day | $\tfrac{2059}{2187}$ | 94.15% |
| $D$ | No rainy day | $\tfrac{128}{2187}$ | 5.85% |
| $E$ | Exactly 2 sunny days | $\tfrac{672}{2187}$ | 30.73% |
| $F$ | At least 4 days same state | $\tfrac{379}{729}$ | 51.99% |

---

## Key Techniques Used

- **Multiplication principle** (independent days): $P(w_i = x \text{ and } w_j = y) = P(w_i=x)\cdot P(w_j=y)$
- **Complement rule**: $P(C) = 1 - P(C^c)$ — much easier than counting directly
- **Binomial distribution**: when counting exactly $k$ successes in $n$ independent trials with success probability $p$:

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$