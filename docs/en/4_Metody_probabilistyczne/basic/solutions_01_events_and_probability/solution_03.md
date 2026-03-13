# Solution 1 — Events and Probability

## Task 3 — Card Drawing

## Setup — Sample Spaces

From Task 3, drawing from a standard **52-card deck**:

$$\Omega_1 = \{\text{all 52 cards}\}, \qquad |\Omega_1| = 52$$

$$\Omega_2 = \{(c_1, c_2) : c_1, c_2 \in \text{deck}\}, \qquad |\Omega_2| = 52 \times 52 = 2704 \quad \text{(with replacement)}$$

$$\Omega_2' = \{(c_1, c_2) : c_1 \neq c_2,\ c_1, c_2 \in \text{deck}\}, \qquad |\Omega_2'| = 52 \times 51 = 2652 \quad \text{(without replacement)}$$

Since the deck is **well-shuffled**, every elementary outcome is equally likely:

$$P(\omega) = \frac{1}{52} \text{ in } \Omega_1, \qquad P(\omega) = \frac{1}{2704} \text{ in } \Omega_2, \qquad P(\omega) = \frac{1}{2652} \text{ in } \Omega_2'$$

A standard deck has:
- **4 suits**: ♠ Spades, ♥ Hearts, ♦ Diamonds, ♣ Clubs — each with **13 cards**
- **13 ranks**: A, 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K — each appearing **4 times**
- **Face cards**: J, Q, K — 3 ranks × 4 suits = **12 face cards**
- **Aces**: 4 cards (one per suit)

---

### Interactive Simulation

Switch between modes and watch the empirical frequencies converge to theoretical probabilities.

<iframe src="https://unclesam13.github.io/Math_Problems_Repo/anim/4_Metody_probalistyczne/card_draw.html" width="100%" height="560" frameborder="0" style="border-radius:4px;"></iframe>

> **Monte Carlo observation:** Run ×5000 draws and watch the event tracker bars match the theoretical values. Notice how $P(\text{Heart}) = \tfrac{1}{4} = 25\%$ emerges clearly from the data.

---

## One Card Drawn — Events on $\Omega_1$

Each card has probability $\tfrac{1}{52}$.

### Event $A_1$ — card is a Heart

There are 13 hearts in the deck:

$$A_1 = \{\text{all } 13 \text{ heart cards}\}$$

$$P(A_1) = \frac{13}{52} = \frac{1}{4}$$

### Event $B_1$ — card is a King

There are 4 kings (one per suit):

$$B_1 = \{K♠, K♥, K♦, K♣\}$$

$$P(B_1) = \frac{4}{52} = \frac{1}{13}$$

### Event $C_1$ — card is not a face card

Face cards are J, Q, K — that is $3 \times 4 = 12$ cards. So non-face cards number:

$$|C_1| = 52 - 12 = 40$$

$$P(C_1) = \frac{40}{52} = \frac{10}{13}$$

---

## Two Cards With Replacement — Events on $\Omega_2$

Each ordered pair $(c_1, c_2)$ has probability $\tfrac{1}{2704}$.

Since the card is **returned** between draws, the two draws are **independent**.

### Event $A_2$ — both cards are Hearts

$$P(A_2) = P(c_1 \text{ is Heart}) \times P(c_2 \text{ is Heart}) = \frac{13}{52} \times \frac{13}{52} = \frac{1}{4} \times \frac{1}{4} = \frac{1}{16}$$

### Event $B_2$ — both cards have the same rank

Fix the first card (any rank). The second must match its rank — there are 4 cards of any given rank out of 52:

$$P(B_2) = 1 \times \frac{4}{52} = \frac{1}{13}$$

Alternatively: there are $13 \times 4^2 = 208$ favorable pairs (choose rank: 13 ways, each card in pair: 4 ways each):

$$P(B_2) = \frac{13 \times 4 \times 4}{52 \times 52} = \frac{208}{2704} = \frac{1}{13}$$

### Event $C_2$ — at least one card is an Ace

Use the complement — neither card is an Ace:

$$P(\text{no Ace}) = \frac{48}{52} \times \frac{48}{52} = \left(\frac{12}{13}\right)^2 = \frac{144}{169}$$

$$P(C_2) = 1 - \frac{144}{169} = \frac{25}{169} \approx 14.8\%$$

---

## Two Cards Without Replacement — Events on $\Omega_2'$

Each ordered pair $(c_1, c_2)$ with $c_1 \neq c_2$ has probability $\tfrac{1}{2652}$.

Since the card is **not returned**, the draws are **dependent** — the second draw depends on what was drawn first.

### Event $A_3$ — both cards are Hearts

$$P(A_3) = P(c_1 \text{ is Heart}) \times P(c_2 \text{ is Heart} \mid c_1 \text{ is Heart})$$

$$= \frac{13}{52} \times \frac{12}{51} = \frac{156}{2652} = \frac{1}{17} \approx 5.88\%$$

Compare with replacement: $\tfrac{1}{16} = 6.25\%$ — slightly lower because one Heart is removed.

### Event $B_3$ — both cards have the same rank

$$P(B_3) = P(c_1 \text{ any rank}) \times P(c_2 \text{ same rank as } c_1 \mid c_1)$$

$$= 1 \times \frac{3}{51} = \frac{1}{17} \approx 5.88\%$$

After drawing one card of a given rank, only 3 of the remaining 51 cards share that rank.

### Event $C_3$ — one King and one Queen (in any order)

There are two orderings: (King first, Queen second) or (Queen first, King second):

$$P(C_3) = P(\text{King then Queen}) + P(\text{Queen then King})$$

$$= \frac{4}{52} \times \frac{4}{51} + \frac{4}{52} \times \frac{4}{51} = 2 \times \frac{16}{2652} = \frac{32}{2652} = \frac{8}{663} \approx 1.21\%$$

---

## Additional Event

**Event $D_3$** (without replacement) — the two cards form a **pair of Aces**:

$$P(D_3) = \frac{4}{52} \times \frac{3}{51} = \frac{12}{2652} = \frac{1}{221} \approx 0.45\%$$

This is a well-known result in poker — the probability of being dealt pocket Aces.

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
| $D_3$ | Pair of Aces | $\Omega_2'$ | $\tfrac{1}{221}$ | 0.45% |

---

## Key Insight — With vs Without Replacement

The fundamental difference:

- **With replacement**: draws are **independent** — $P(c_2 \mid c_1) = P(c_2)$
- **Without replacement**: draws are **dependent** — removing $c_1$ changes the probabilities for $c_2$

This is why probabilities are slightly **lower** without replacement when both favorable outcomes compete for the same pool of cards (e.g. $P(A_3) < P(A_2)$ for both Hearts).