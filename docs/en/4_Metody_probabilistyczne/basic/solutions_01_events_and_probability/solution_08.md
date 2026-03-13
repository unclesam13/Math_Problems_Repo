# Solution 8 — Events and Probability

## Task 8 - Events and Probabilities in Card Drawing

### Setup — Sample Spaces and Probabilities

From Task 3, drawing from a standard **52-card deck**:

$$\Omega_1 = \{\text{all 52 cards}\}, \qquad P(\omega) = \frac{1}{52}$$

$$\Omega_2: \text{ two draws \textbf{with replacement}}, \qquad |\Omega_2| = 2704, \qquad P(\omega) = \frac{1}{2704}$$

$$\Omega_2': \text{ two draws \textbf{without replacement}}, \qquad |\Omega_2'| = 2652, \qquad P(\omega) = \frac{1}{2652}$$

Deck composition reminder:
- 4 suits × 13 ranks = 52 cards
- Hearts: 13 cards, Kings: 4 cards, Aces: 4 cards
- Face cards (J, Q, K): $3 \times 4 = 12$ cards, so non-face cards: $52 - 12 = 40$

---

## One Card Drawn — Events on $\Omega_1$

### Event $A_1$ — Card is a Heart

$$A_1 = \{\text{13 heart cards}\}$$

$$P(A_1) = \frac{13}{52} = \frac{1}{4}$$

### Event $B_1$ — Card is a King

$$B_1 = \{K\spadesuit,\ K\heartsuit,\ K\diamondsuit,\ K\clubsuit\}$$

$$P(B_1) = \frac{4}{52} = \frac{1}{13}$$

### Event $C_1$ — Card is Not a Face Card

Face cards: J, Q, K — three ranks × four suits = 12 cards. Non-face cards: $52 - 12 = 40$.

$$P(C_1) = \frac{40}{52} = \frac{10}{13}$$

Using the complement: $P(C_1) = 1 - \frac{12}{52} = 1 - \frac{3}{13} = \frac{10}{13}$ ✓

---

## Two Cards With Replacement — Events on $\Omega_2$

Draws are **independent**: $P(c_2 \mid c_1) = P(c_2)$.

### Event $A_2$ — Both Cards are Hearts

$$P(A_2) = P(c_1 = \heartsuit) \times P(c_2 = \heartsuit) = \frac{13}{52} \times \frac{13}{52} = \frac{1}{4} \times \frac{1}{4} = \frac{1}{16}$$

### Event $B_2$ — Both Cards Have the Same Rank

The first card can be anything. The second must match its rank — 4 cards of any rank exist in 52:

$$P(B_2) = 1 \times \frac{4}{52} = \frac{1}{13}$$

Equivalently: $\tfrac{13 \times 4 \times 4}{52 \times 52} = \tfrac{208}{2704} = \tfrac{1}{13}$ ✓

### Event $C_2$ — At Least One Card is an Ace

Complement: neither card is an Ace. There are $52 - 4 = 48$ non-Ace cards.

$$P(\text{no Ace}) = \frac{48}{52} \times \frac{48}{52} = \left(\frac{12}{13}\right)^2 = \frac{144}{169}$$

$$P(C_2) = 1 - \frac{144}{169} = \frac{25}{169} \approx 14.79\%$$

---

## Two Cards Without Replacement — Events on $\Omega_2'$

Draws are **dependent**: removing $c_1$ changes the remaining deck.

### Event $A_3$ — Both Cards are Hearts

$$P(A_3) = P(c_1 = \heartsuit) \times P(c_2 = \heartsuit \mid c_1 = \heartsuit)$$

After drawing one heart, 12 hearts remain out of 51 cards:

$$P(A_3) = \frac{13}{52} \times \frac{12}{51} = \frac{156}{2652} = \frac{1}{17} \approx 5.88\%$$

Compare with replacement: $\tfrac{1}{16} = 6.25\%$ — slightly lower because one heart is gone.

### Event $B_3$ — Both Cards Have the Same Rank

After drawing $c_1$ of any rank, 3 cards of that rank remain out of 51:

$$P(B_3) = 1 \times \frac{3}{51} = \frac{1}{17} \approx 5.88\%$$

Compare with replacement: $\tfrac{1}{13} \approx 7.69\%$ — lower because one card of the rank is removed.

### Event $C_3$ — One King and One Queen (Any Order)

Two mutually exclusive orderings:

$$P(\text{King then Queen}) = \frac{4}{52} \times \frac{4}{51} = \frac{16}{2652}$$

$$P(\text{Queen then King}) = \frac{4}{52} \times \frac{4}{51} = \frac{16}{2652}$$

$$P(C_3) = \frac{16}{2652} + \frac{16}{2652} = \frac{32}{2652} = \frac{8}{663} \approx 1.21\%$$

---

## Additional Event on $\Omega_2'$

**Event $D$** — the two cards together contain **exactly one Ace and one King** (in any order):

$$P(\text{Ace then King}) = \frac{4}{52} \times \frac{4}{51} = \frac{16}{2652}$$

$$P(\text{King then Ace}) = \frac{4}{52} \times \frac{4}{51} = \frac{16}{2652}$$

$$P(D) = \frac{32}{2652} = \frac{8}{663} \approx 1.21\%$$

Interestingly $P(D) = P(C_3)$ — this makes sense by symmetry, since Kings and Queens are symmetric groups of 4 cards, just as Kings and Aces are.

---

## Summary Table

| Event | Description | Space | Probability | Decimal |
|---|---|---|---|---|
| $A_1$ | Heart | $\Omega_1$ | $\tfrac{1}{4}$ | 25.00% |
| $B_1$ | King | $\Omega_1$ | $\tfrac{1}{13}$ | 7.69% |
| $C_1$ | Not a face card | $\Omega_1$ | $\tfrac{10}{13}$ | 76.92% |
| $A_2$ | Both Hearts | $\Omega_2$ | $\tfrac{1}{16}$ | 6.25% |
| $B_2$ | Same rank | $\Omega_2$ | $\tfrac{1}{13}$ | 7.69% |
| $C_2$ | At least one Ace | $\Omega_2$ | $\tfrac{25}{169}$ | 14.79% |
| $A_3$ | Both Hearts | $\Omega_2'$ | $\tfrac{1}{17}$ | 5.88% |
| $B_3$ | Same rank | $\Omega_2'$ | $\tfrac{1}{17}$ | 5.88% |
| $C_3$ | One King, one Queen | $\Omega_2'$ | $\tfrac{8}{663}$ | 1.21% |
| $D$ | One Ace, one King | $\Omega_2'$ | $\tfrac{8}{663}$ | 1.21% |

---

## Key Insight — Independence vs Dependence

| | With Replacement ($\Omega_2$) | Without Replacement ($\Omega_2'$) |
|---|---|---|
| Draws | Independent | Dependent |
| Rule | $P(c_2 \mid c_1) = P(c_2)$ | $P(c_2 \mid c_1) \neq P(c_2)$ |
| Both Hearts | $\tfrac{13}{52} \times \tfrac{13}{52} = \tfrac{1}{16}$ | $\tfrac{13}{52} \times \tfrac{12}{51} = \tfrac{1}{17}$ |
| Same rank | $\tfrac{4}{52} = \tfrac{1}{13}$ | $\tfrac{3}{51} = \tfrac{1}{17}$ |

Without replacement always gives **lower** probability for matching events — removing one card from the pool makes a second match harder.

---

## Key Techniques Used

- **Multiplication rule for independent events**: $P(A \cap B) = P(A) \cdot P(B)$ when draws are with replacement
- **Multiplication rule for dependent events**: $P(A \cap B) = P(A) \cdot P(B \mid A)$ when draws are without replacement
- **Complement rule**: essential for "at least one" events like $C_2$
- **Addition of mutually exclusive events**: $P(A \cup B) = P(A) + P(B)$ for ordered pair events like $C_3$ and $D$
- **Symmetry argument**: explains why $P(C_3) = P(D)$ without recomputing