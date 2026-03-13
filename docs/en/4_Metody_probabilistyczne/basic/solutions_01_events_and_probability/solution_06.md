# Solution 1 — Events and Probability

## Task 6 - Events and Probabilities in Coin Tossing

### Setup — Sample Spaces and Probabilities

From Task 1, the sample spaces for a **fair coin** are:

$$\Omega_1 = \{H, T\}, \qquad |\Omega_1| = 2, \qquad P(\omega) = \frac{1}{2}$$

$$\Omega_2 = \{HH, HT, TH, TT\}, \qquad |\Omega_2| = 4, \qquad P(\omega) = \frac{1}{4}$$

$$\Omega_3 = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}, \qquad |\Omega_3| = 8, \qquad P(\omega) = \frac{1}{8}$$

Since the coin is **fair** and tosses are **independent**, every elementary outcome has equal probability $\tfrac{1}{2^n}$ in $\Omega_n$.

---

## One Coin Toss — Events on $\Omega_1$

### Event $A_1$ — Result is Heads

$$A_1 = \{H\}$$

$$P(A_1) = \frac{1}{2}$$

### Event $B_1$ — Result is Tails

$$B_1 = \{T\}$$

$$P(B_1) = \frac{1}{2}$$

### Event $C_1$ — Result is Not Tails

$C_1$ is the complement of $B_1$:

$$C_1 = \Omega_1 \setminus B_1 = \{H\}$$

$$P(C_1) = 1 - P(B_1) = 1 - \frac{1}{2} = \frac{1}{2}$$

Note that $C_1 = A_1$ — "not tails" is the same event as "heads" in this experiment.

---

## Two Coin Tosses — Events on $\Omega_2$

### Event $A_2$ — Exactly One Head

$$A_2 = \{HT, TH\}$$

$$P(A_2) = \frac{2}{4} = \frac{1}{2}$$

Alternatively via the Binomial formula with $n=2$, $k=1$, $p=\tfrac{1}{2}$:

$$P(A_2) = \binom{2}{1}\left(\frac{1}{2}\right)^1\left(\frac{1}{2}\right)^1 = 2 \cdot \frac{1}{4} = \frac{1}{2} \checkmark$$

### Event $B_2$ — At Least One Head

Use the complement — no heads means all tails:

$$P(\text{no heads}) = P(\{TT\}) = \frac{1}{4}$$

$$B_2 = \{HH, HT, TH\}$$

$$P(B_2) = 1 - \frac{1}{4} = \frac{3}{4}$$

### Event $C_2$ — Both Tosses Give the Same Result

$$C_2 = \{HH, TT\}$$

$$P(C_2) = \frac{2}{4} = \frac{1}{2}$$

---

## Three Coin Tosses — Events on $\Omega_3$

### Event $A_3$ — Exactly Two Heads

$$A_3 = \{HHT, HTH, THH\}$$

$$P(A_3) = \frac{3}{8}$$

Via Binomial with $n=3$, $k=2$, $p=\tfrac{1}{2}$:

$$P(A_3) = \binom{3}{2}\left(\frac{1}{2}\right)^2\left(\frac{1}{2}\right)^1 = 3 \cdot \frac{1}{8} = \frac{3}{8} \checkmark$$

### Event $B_3$ — At Least One Tail

Use the complement — all heads:

$$P(\text{all heads}) = P(\{HHH\}) = \frac{1}{8}$$

$$B_3 = \Omega_3 \setminus \{HHH\} = \{HHT, HTH, HTT, THH, THT, TTH, TTT\}$$

$$P(B_3) = 1 - \frac{1}{8} = \frac{7}{8}$$

### Event $C_3$ — All Three Tosses Give the Same Result

$$C_3 = \{HHH, TTT\}$$

$$P(C_3) = \frac{2}{8} = \frac{1}{4}$$

This can also be seen as: the second toss must match the first ($p = \tfrac{1}{2}$) AND the third must match the first ($p = \tfrac{1}{2}$):

$$P(C_3) = 1 \cdot \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4} \checkmark$$

---

## Additional Event on $\Omega_3$

**Event $D_3$** — the number of Heads is **strictly greater** than the number of Tails (i.e. at least 2 heads):

$$D_3 = \{HHT, HTH, THH, HHH\}$$

$$|D_3| = \binom{3}{2} + \binom{3}{3} = 3 + 1 = 4$$

$$P(D_3) = \frac{4}{8} = \frac{1}{2}$$

This is intuitive — by symmetry of a fair coin, heads majority and tails majority are equally likely, each with probability $\tfrac{1}{2}$ (the case of a tie is impossible with an odd number of tosses).

---

## Summary Table

| Event | Description | Subset | Probability |
|---|---|---|---|
| $A_1$ | Heads | $\{H\}$ | $\tfrac{1}{2}$ |
| $B_1$ | Tails | $\{T\}$ | $\tfrac{1}{2}$ |
| $C_1$ | Not Tails | $\{H\}$ | $\tfrac{1}{2}$ |
| $A_2$ | Exactly one Head | $\{HT, TH\}$ | $\tfrac{1}{2}$ |
| $B_2$ | At least one Head | $\{HH,HT,TH\}$ | $\tfrac{3}{4}$ |
| $C_2$ | Both same result | $\{HH, TT\}$ | $\tfrac{1}{2}$ |
| $A_3$ | Exactly two Heads | $\{HHT,HTH,THH\}$ | $\tfrac{3}{8}$ |
| $B_3$ | At least one Tail | $\Omega_3 \setminus \{HHH\}$ | $\tfrac{7}{8}$ |
| $C_3$ | All same result | $\{HHH, TTT\}$ | $\tfrac{1}{4}$ |
| $D_3$ | More Heads than Tails | $\{HHT,HTH,THH,HHH\}$ | $\tfrac{1}{2}$ |

---

## Key Techniques Used

- **Classical probability**: $P(A) = \tfrac{|A|}{|\Omega|}$ when all outcomes are equally likely
- **Complement rule**: $P(A) = 1 - P(A^c)$ — essential for "at least one" events like $B_2$ and $B_3$
- **Binomial distribution**: for exactly $k$ heads in $n$ fair tosses:
$$P(X = k) = \binom{n}{k} \left(\frac{1}{2}\right)^n$$
- **Symmetry argument**: used for $C_3$ (conditional probability) and $D_3$ (heads vs tails majority)