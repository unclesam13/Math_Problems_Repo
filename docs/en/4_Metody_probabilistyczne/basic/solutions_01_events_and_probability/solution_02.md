# Solution 1 — Events and Probability

## Task 2 — Dice Rolling


### Setup — Sample Spaces

From Task 2 we have:

$$\Omega_1 = \{1,2,3,4,5,6\}, \quad |\Omega_1| = 6$$

$$\Omega_2 = \{(i,j) : i,j \in \{1,\ldots,6\}\}, \quad |\Omega_2| = 36$$

$$\Omega_3 = \{(i,j,k) : i,j,k \in \{1,\ldots,6\}\}, \quad |\Omega_3| = 216$$

Since the dice is **fair**, every elementary outcome has equal probability:

$$P(\omega) = \frac{1}{|\Omega_n|} \quad \text{for each } \omega \in \Omega_n$$

So for $\Omega_1$: $P(\omega) = \tfrac{1}{6}$, for $\Omega_2$: $P(\omega) = \tfrac{1}{36}$, for $\Omega_3$: $P(\omega) = \tfrac{1}{216}$.

---

### Interactive Simulation

Observe how the empirical sum distribution (solid bars) approaches the theoretical shape (outline) as the number of rolls increases.

<iframe src="https://unclesam13.github.io/Math_Problems_Repo/anim/4_Metody_probalistyczne/dice_roll.html" width="100%" height="580" frameborder="0" style="border-radius:4px;"></iframe>

> **Monte Carlo observation:** With 2 dice, roll ×10000 and notice the distribution forms a **triangle peaked at 7**. This is because there are 6 ways to make a sum of 7, more than any other sum — confirming our calculation below.

---

## One dice Roll — Events on $\Omega_1$

Each outcome has probability $\tfrac{1}{6}$.

### Event $A_1$ — result is even

$$A_1 = \{2, 4, 6\}$$

$$P(A_1) = \frac{|A_1|}{|\Omega_1|} = \frac{3}{6} = \frac{1}{2}$$

### Event $B_1$ — result is greater than 4

$$B_1 = \{5, 6\}$$

$$P(B_1) = \frac{2}{6} = \frac{1}{3}$$

### Event $C_1$ — result is at most 3

$$C_1 = \{1, 2, 3\}$$

$$P(C_1) = \frac{3}{6} = \frac{1}{2}$$

---

## Two Dice Rolls — Events on $\Omega_2$

Each ordered pair $(i,j)$ has probability $\tfrac{1}{36}$.

### Event $A_2$ — sum equals 7

All pairs $(i,j)$ with $i+j=7$:

$$A_2 = \{(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)\}$$

$$P(A_2) = \frac{6}{36} = \frac{1}{6}$$

> Sum 7 is the **most likely sum** for two dice — there are more ways to achieve it than any other value.

### Event $B_2$ — both results are the same

$$B_2 = \{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}$$

$$P(B_2) = \frac{6}{36} = \frac{1}{6}$$

### Event $C_2$ — sum is at least 10

Pairs with $i+j \geq 10$:

$$C_2 = \{(4,6),(5,5),(5,6),(6,4),(6,5),(6,6)\}$$

$$P(C_2) = \frac{6}{36} = \frac{1}{6}$$

---

## Three Dice Rolls — Events on $\Omega_3$

Each ordered triple $(i,j,k)$ has probability $\tfrac{1}{216}$.

### Event $A_3$ — sum equals 10

We count all triples $(i,j,k)$ with $i+j+k=10$ and $1 \leq i,j,k \leq 6$.

Using stars and bars with inclusion-exclusion, substituting $i'=i-1,j'=j-1,k'=k-1$ gives $i'+j'+k'=7$ with $0 \leq i',j',k' \leq 5$.

Total unrestricted: $\binom{9}{2} = 36$. Subtract cases where any variable $> 5$: $3 \cdot \binom{3}{2} = 9$.

$$|A_3| = 36 - 9 = 27$$

$$P(A_3) = \frac{27}{216} = \frac{1}{8}$$

### Event $B_3$ — exactly two rolls give the same number

We need exactly one pair of equal values and one different value.

- Choose the repeated value: 6 ways
- Choose the distinct value (different from repeated): 5 ways
- Choose which position holds the distinct value: 3 ways

$$|B_3| = 6 \times 5 \times 3 = 90$$

$$P(B_3) = \frac{90}{216} = \frac{5}{12}$$

### Event $C_3$ — two twos and one three (in any order)

The arrangements of $(2,2,3)$:

$$C_3 = \{(2,2,3),(2,3,2),(3,2,2)\}$$

$$|C_3| = \frac{3!}{2!\,1!} = 3$$

$$P(C_3) = \frac{3}{216} = \frac{1}{72}$$

---

## Additional Event

**Event $D_3$** — all three rolls give different values (no two dice show the same number).

The number of ordered triples with all distinct values is:

$$|D_3| = 6 \times 5 \times 4 = 120$$

$$P(D_3) = \frac{120}{216} = \frac{5}{9}$$

This can also be seen as: the second dice must differ from the first ($\tfrac{5}{6}$) and the third must differ from both ($\tfrac{4}{6}$):

$$P(D_3) = 1 \cdot \frac{5}{6} \cdot \frac{4}{6} = \frac{20}{36} = \frac{5}{9} \checkmark$$

---

## Summary Table

| Event | Description | Probability |
|---|---|---|
| $A_1$ | Even result (1 dice) | $\tfrac{1}{2}$ |
| $B_1$ | Result $> 4$ (1 dice) | $\tfrac{1}{3}$ |
| $C_1$ | Result $\leq 3$ (1 dice) | $\tfrac{1}{2}$ |
| $A_2$ | Sum $= 7$ (2 dice) | $\tfrac{1}{6}$ |
| $B_2$ | Both same (2 dice) | $\tfrac{1}{6}$ |
| $C_2$ | Sum $\geq 10$ (2 dice) | $\tfrac{1}{6}$ |
| $A_3$ | Sum $= 10$ (3 dice) | $\tfrac{1}{8}$ |
| $B_3$ | Exactly one pair (3 dice) | $\tfrac{5}{12}$ |
| $C_3$ | Two 2s and one 3 (3 dice) | $\tfrac{1}{72}$ |
| $D_3$ | All different (3 dice) | $\tfrac{5}{9}$ |