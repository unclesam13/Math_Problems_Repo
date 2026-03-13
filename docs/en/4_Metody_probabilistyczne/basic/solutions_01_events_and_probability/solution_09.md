# Solution 9 — Events and Probability

## Task 9 - Events and Probabilities in Weekly Weather Observation

### Setup — Sample Space and Probability Model

From Task 4, the sample space for **7 independent days** with states $\{S, C, R\}$:

$$\Omega_7 = \{(w_1, w_2, w_3, w_4, w_5, w_6, w_7) : w_i \in \{S, C, R\}\}, \qquad |\Omega_7| = 3^7 = 2187$$

Days are labelled: $w_1$ = Mon, $w_2$ = Tue, $w_3$ = Wed, $w_4$ = Thu, $w_5$ = Fri, $w_6$ = Sat, $w_7$ = Sun.

Each state occurs with probability $\tfrac{1}{3}$ per day, and days are **independent**, so:

$$P(w_i = x) = \frac{1}{3} \quad \text{for any } x \in \{S,C,R\},\ \text{any } i$$

$$P(\omega) = \left(\frac{1}{3}\right)^7 = \frac{1}{2187} \quad \text{for each elementary outcome}$$

---

## Event $A$ — Entire Weekend is Sunny

Both Saturday ($w_6 = S$) and Sunday ($w_7 = S$). The 5 weekdays are free.

By independence:

$$P(A) = P(w_6 = S) \cdot P(w_7 = S) = \frac{1}{3} \cdot \frac{1}{3} = \frac{1}{9} \approx 11.11\%$$

Equivalently: $|A| = 1 \cdot 1 \cdot 3^5 = 243$, so $P(A) = \tfrac{243}{2187} = \tfrac{1}{9}$ ✓

---

## Event $B$ — Wednesday, Thursday, Friday All Rainy

$w_3 = R$, $w_4 = R$, $w_5 = R$. The remaining 4 days are free.

$$P(B) = P(w_3 = R) \cdot P(w_4 = R) \cdot P(w_5 = R) = \left(\frac{1}{3}\right)^3 = \frac{1}{27} \approx 3.70\%$$

---

## Event $C$ — At Least One Sunny Day During the Week

Direct counting is tedious — use the **complement**: no day is sunny means each day is $C$ or $R$ (2 choices).

$$P(\text{no sunny day}) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187}$$

$$P(C) = 1 - \frac{128}{2187} = \frac{2059}{2187} \approx 94.15\%$$

The high probability confirms intuition — with 7 days and $P(S) = \tfrac{1}{3}$, at least one sunny day is very likely.

---

## Event $D$ — No Rainy Day During the Entire Week

Every day must be $S$ or $C$:

$$P(D) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187} \approx 5.85\%$$

Note: $P(D) = P(\text{no sunny day from Event } C\text{'s complement})$ — by symmetry of the three states, the probability of "no $X$" is the same for any state $X \in \{S, C, R\}$.

---

## Event $E$ — Exactly Two Sunny Days

This follows a **Binomial distribution** $X \sim \text{Bin}(7, \tfrac{1}{3})$ where $X$ = number of sunny days.

$$P(E) = P(X = 2) = \binom{7}{2}\left(\frac{1}{3}\right)^2\left(\frac{2}{3}\right)^5$$

Computing each factor:

$$\binom{7}{2} = 21, \qquad \left(\frac{1}{3}\right)^2 = \frac{1}{9}, \qquad \left(\frac{2}{3}\right)^5 = \frac{32}{243}$$

$$P(E) = 21 \times \frac{1}{9} \times \frac{32}{243} = \frac{21 \times 32}{2187} = \frac{672}{2187} \approx 30.73\%$$

For reference, the full Binomial distribution $\text{Bin}(7, \tfrac{1}{3})$:

| $k$ (sunny days) | $\binom{7}{k}$ | $P(X=k)$ | Approx |
|---|---|---|---|
| 0 | 1 | $\tfrac{128}{2187}$ | 5.85% |
| 1 | 7 | $\tfrac{448}{2187}$ | 20.48% |
| **2** | **21** | $\mathbf{\tfrac{672}{2187}}$ | **30.73%** |
| 3 | 35 | $\tfrac{560}{2187}$ | 25.60% |
| 4 | 35 | $\tfrac{280}{2187}$ | 12.80% |
| 5 | 21 | $\tfrac{84}{2187}$ | 3.84% |
| 6 | 7 | $\tfrac{14}{2187}$ | 0.64% |
| 7 | 1 | $\tfrac{1}{2187}$ | 0.05% |
| **Total** | **128** | $\mathbf{1}$ | **100%** |

The most likely number of sunny days is $k=2$, and the **expected** number is $E[X] = 7 \cdot \tfrac{1}{3} = \tfrac{7}{3} \approx 2.33$ days.

---

## Additional Event

**Event $F$** — Monday and Tuesday have **different** weather states.

$$P(w_1 \neq w_2) = 1 - P(w_1 = w_2)$$

By independence, $P(w_1 = w_2) = \sum_{x \in \{S,C,R\}} P(w_1=x)\cdot P(w_2=x) = 3 \times \tfrac{1}{3} \times \tfrac{1}{3} = \tfrac{1}{3}$

$$P(F) = 1 - \frac{1}{3} = \frac{2}{3} \approx 66.67\%$$

Intuitively: given Monday's state (any), Tuesday has a $\tfrac{2}{3}$ chance of being different.

---

## Summary Table

| Event | Description | Probability | Decimal |
|---|---|---|---|
| $A$ | Full weekend sunny ($w_6=w_7=S$) | $\tfrac{1}{9}$ | 11.11% |
| $B$ | Wed–Fri all rainy | $\tfrac{1}{27}$ | 3.70% |
| $C$ | At least one sunny day | $\tfrac{2059}{2187}$ | 94.15% |
| $D$ | No rainy day | $\tfrac{128}{2187}$ | 5.85% |
| $E$ | Exactly 2 sunny days | $\tfrac{672}{2187}$ | 30.73% |
| $F$ | Mon and Tue different states | $\tfrac{2}{3}$ | 66.67% |

---

## Key Techniques Used

- **Multiplication rule for independent events**: days are independent so probabilities multiply directly
- **Complement rule**: essential for Event $C$ — "at least one" is always easier via complement
- **Binomial distribution** $\text{Bin}(n, p)$: models the number of successes in $n$ independent trials each with success probability $p$:
$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$
- **Symmetry**: since $P(S) = P(C) = P(R) = \tfrac{1}{3}$, events about "no $S$", "no $C$", "no $R$" all have the same probability $\left(\tfrac{2}{3}\right)^7$
- **Law of total probability**: used implicitly in Event $F$ — summing over all possible states of $w_1$