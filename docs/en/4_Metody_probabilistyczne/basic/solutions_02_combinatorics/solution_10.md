# Task 10 — Urn Models
 
Urn: **5 red**, **4 blue**, **3 green** = 12 balls total.
 
**1. Three balls drawn without replacement, order ignored**
 
This is a combination — choosing a set of 3 from 12:
 
$$\binom{12}{3} = \frac{12 \times 11 \times 10}{6} = 220$$
 
**2. Samples containing exactly 2 red balls**
 
Choose 2 red from 5, then 1 non-red from remaining 7:
 
$$\binom{5}{2} \times \binom{7}{1} = 10 \times 7 = 70$$
 
**3. Three balls drawn, order of colors recorded**
 
This is a sequence (ordered selection) without replacement. Order matters, no repetition:
 
$$P(12,3) = 12 \times 11 \times 10 = 1{,}320$$
 
**4. Ordered outcomes with exactly 2 red balls**
 
Choose which 2 positions (out of 3) hold red balls: $\binom{3}{2} = 3$ ways.
 
Choose 2 distinct red balls from 5 (order matters for the positions): $P(5,2) = 20$ ways.
 
Choose 1 non-red ball from 7: $7$ ways.
 
$$3 \times 20 \times 7 = 420$$
 
> **Alternatively:** Think step by step. The ordered triple must have red in 2 positions and non-red in 1 position. Number of arrangements of the positions: $\binom{3}{2}=3$. Red balls fill those 2 ordered positions: $5 \times 4 = 20$. Non-red fills the remaining: $7$. Total: $3 \times 20 \times 7 = 420$ ✓
 