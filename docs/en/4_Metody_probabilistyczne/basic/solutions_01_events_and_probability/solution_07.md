# Solution 1 — Events and Probability

## Task 7 - Events and Probabilities in Die Rolling

### Setup — Sample Spaces and Probabilities

From Task 2, the sample spaces for a **fair six-sided die** are:

$$\Omega_1 = \{1,2,3,4,5,6\}, \qquad |\Omega_1| = 6, \qquad P(\omega) = \frac{1}{6}$$

$$\Omega_2 = \{(i,j) : i,j \in \{1,\ldots,6\}\}, \qquad |\Omega_2| = 36, \qquad P(\omega) = \frac{1}{36}$$

$$\Omega_3 = \{(i,j,k) : i,j,k \in \{1,\ldots,6\}\}, \qquad |\Omega_3| = 216, \qquad P(\omega) = \frac{1}{216}$$



## One Die Roll — Events on $\Omega_1$

### Event $A_1$ — Result is Even

$$A_1 = \{2, 4, 6\}$$

$$P(A_1) = \frac{3}{6} = \frac{1}{2}$$

### Event $B_1$ — Result is Greater Than 4

$$B_1 = \{5, 6\}$$

$$P(B_1) = \frac{2}{6} = \frac{1}{3}$$

### Event $C_1$ — Result is At Most 3

$$C_1 = \{1, 2, 3\}$$

$$P(C_1) = \frac{3}{6} = \frac{1}{2}$$

Note that $A_1$ and $C_1$ are **not** mutually exclusive — the outcome $2$ belongs to both. However $P(A_1 \cap C_1) = P(\{2\}) = \tfrac{1}{6}$.

---

## Two Die Rolls — Events on $\Omega_2$

### Event $A_2$ — Sum Equals 7

All ordered pairs $(i,j)$ with $i + j = 7$:

$$A_2 = \{(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)\}$$

$$P(A_2) = \frac{6}{36} = \frac{1}{6}$$

Sum 7 is the **most probable sum** for two dice — more pairs produce it than any other value. The full distribution of sums is:

| Sum | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Ways | 1 | 2 | 3 | 4 | 5 | **6** | 5 | 4 | 3 | 2 | 1 |
| Prob | $\tfrac{1}{36}$ | $\tfrac{2}{36}$ | $\tfrac{3}{36}$ | $\tfrac{4}{36}$ | $\tfrac{5}{36}$ | $\mathbf{\tfrac{6}{36}}$ | $\tfrac{5}{36}$ | $\tfrac{4}{36}$ | $\tfrac{3}{36}$ | $\tfrac{2}{36}$ | $\tfrac{1}{36}$ |

### Event $B_2$ — Both Results Are the Same (Doubles)

$$B_2 = \{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}$$

$$P(B_2) = \frac{6}{36} = \frac{1}{6}$$

### Event $C_2$ — Sum is At Least 10

Pairs with $i + j \geq 10$:

| Sum | Pairs |
|---|---|
| 10 | $(4,6),(5,5),(6,4)$ |
| 11 | $(5,6),(6,5)$ |
| 12 | $(6,6)$ |

$$|C_2| = 3 + 2 + 1 = 6$$

$$P(C_2) = \frac{6}{36} = \frac{1}{6}$$

---

## Three Die Rolls — Events on $\Omega_3$

### Event $A_3$ — Sum Equals 10

We count triples $(i,j,k)$ with $i+j+k = 10$ and $1 \leq i,j,k \leq 6$.

Substitute $i' = i-1,\ j' = j-1,\ k' = k-1$, so $i'+j'+k' = 7$ with $0 \leq i',j',k' \leq 5$.

**Stars and bars** (unrestricted): $\binom{7+2}{2} = \binom{9}{2} = 36$

**Subtract** cases where any variable exceeds 5 (say $i' \geq 6$, let $i'' = i'-6$, then $i''+j'+k'=1$): $\binom{3}{2} = 3$ solutions, and there are 3 such variables, giving $3 \times 3 = 9$ cases to subtract.

No variable can exceed 5 twice simultaneously (since $6+6=12>7$), so no over-subtraction.

$$|A_3| = 36 - 9 = 27$$

$$P(A_3) = \frac{27}{216} = \frac{1}{8}$$

### Event $B_3$ — Exactly Two Rolls Give the Same Number

We need exactly one **pair** and one **distinct** value (no triple).

- Choose the **repeated value**: $6$ ways
- Choose the **distinct value** (must differ): $5$ ways
- Choose **which position** holds the distinct value: $3$ ways (position 1, 2, or 3)

$$|B_3| = 6 \times 5 \times 3 = 90$$

$$P(B_3) = \frac{90}{216} = \frac{5}{12}$$

**Verification** — the three cases for $\Omega_3$ are:
- All three the same: $6$ triples
- Exactly two the same: $90$ triples
- All different: $6 \times 5 \times 4 = 120$ triples
- Total: $6 + 90 + 120 = 216$ ✓

### Event $C_3$ — Two Twos and One Three (Any Order)

The distinct arrangements of $(2,2,3)$ are:

$$C_3 = \{(2,2,3),\ (2,3,2),\ (3,2,2)\}$$

$$|C_3| = \frac{3!}{2!\,1!} = 3$$

$$P(C_3) = \frac{3}{216} = \frac{1}{72}$$

---

## Additional Event

**Event $D_3$** — the **maximum** of the three rolls equals 6 (at least one die shows 6).

Use the complement — no die shows 6, so each die shows 1–5:

$$P(\text{no six}) = \left(\frac{5}{6}\right)^3 = \frac{125}{216}$$

$$P(D_3) = 1 - \frac{125}{216} = \frac{91}{216} \approx 42.13\%$$

---

## Summary Table

| Event | Description | Favorable outcomes | Probability |
|---|---|---|---|
| $A_1$ | Even result | 3 | $\tfrac{1}{2}$ |
| $B_1$ | Result $> 4$ | 2 | $\tfrac{1}{3}$ |
| $C_1$ | Result $\leq 3$ | 3 | $\tfrac{1}{2}$ |
| $A_2$ | Sum $= 7$ | 6 | $\tfrac{1}{6}$ |
| $B_2$ | Doubles | 6 | $\tfrac{1}{6}$ |
| $C_2$ | Sum $\geq 10$ | 6 | $\tfrac{1}{6}$ |
| $A_3$ | Sum $= 10$ | 27 | $\tfrac{1}{8}$ |
| $B_3$ | Exactly one pair | 90 | $\tfrac{5}{12}$ |
| $C_3$ | Two 2s and one 3 | 3 | $\tfrac{1}{72}$ |
| $D_3$ | At least one 6 | 91 | $\tfrac{91}{216}$ |

---

## Key Techniques Used

- **Classical probability**: $P(A) = \tfrac{|A|}{|\Omega|}$ for equally likely outcomes
- **Systematic listing**: essential for two-dice sums — the triangular table avoids missing cases
- **Stars and bars with inclusion-exclusion**: for counting integer solutions with upper bounds (Event $A_3$)
- **Multinomial counting**: $\tfrac{n!}{k_1!\,k_2!\cdots}$ for arrangements with repeated elements (Event $C_3$)
- **Complement rule**: much cleaner for "at least one" events like $B_3$ (verification) and $D_3$
- **Partition verification**: checking that all cases sum to $|\Omega|$ is a powerful error-detection tool