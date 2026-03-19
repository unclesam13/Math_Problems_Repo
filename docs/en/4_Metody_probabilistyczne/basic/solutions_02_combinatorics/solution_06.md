# Task 6 — Combinations in Card Problems
 
A standard deck: 52 cards, 13 hearts, 12 face cards (J,Q,K in each of 4 suits), 40 non-face cards.
 
**1. 5-card hand with exactly 2 hearts**
 
Choose 2 hearts from 13, then 3 non-hearts from remaining 39:
 
$$\binom{13}{2} \times \binom{39}{3} = 78 \times 9{,}139 = 712{,}842$$
 
**2. 5-card hand with at least one heart**
 
Complement: no hearts at all (choose 5 from 39 non-hearts):
 
$$\binom{52}{5} - \binom{39}{5} = 2{,}598{,}960 - 575{,}757 = 2{,}023{,}203$$
 
**3. 5-card hand with no face cards**
 
Face cards: J, Q, K = 3 ranks × 4 suits = 12 cards. Non-face cards: $52 - 12 = 40$.
 
Choose 5 from the 40 non-face cards:
 
$$\binom{40}{5} = \frac{40 \times 39 \times 38 \times 37 \times 36}{120} = 658{,}008$$