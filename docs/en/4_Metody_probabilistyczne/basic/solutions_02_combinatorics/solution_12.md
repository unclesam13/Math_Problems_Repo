# Task 12 — Mixed Counting Problem
 
### Part 1 — Student ID Codes
 
Format: 2 letters from $\{A,B,C,D,E\}$ + 3 digits from $\{0,...,9\}$.
 
**1. Letters and digits may repeat**
 
Letters: $5^2 = 25$. Digits: $10^3 = 1{,}000$.
 
$$25 \times 1{,}000 = 25{,}000$$
 
**2. Letters may not repeat, digits may repeat**
 
Letters: $P(5,2) = 5 \times 4 = 20$. Digits: $10^3 = 1{,}000$.
 
$$20 \times 1{,}000 = 20{,}000$$
 
**3. Neither letters nor digits may repeat**
 
Letters: $P(5,2) = 20$. Digits: $P(10,3) = 10 \times 9 \times 8 = 720$.
 
$$20 \times 720 = 14{,}400$$
 
---
 
### Part 2 — Medal Assignment
 
**1. Medals for 12 runners (gold, silver, bronze)**
 
Order matters, no repetition, select 3 from 12:
 
$$P(12,3) = 12 \times 11 \times 10 = 1{,}320$$
 
**2. Two particular runners (say A and B) must BOTH receive medals**
 
A and B take 2 of the 3 medal positions. Choose which 2 positions they get: $P(3,2) = 6$ ways to assign gold/silver/bronze to A and B (ordered). Then choose 1 of remaining 10 runners for the third medal: $10$ ways.
 
$$6 \times 10 = 60$$
 
> **Alternatively:** Choose the third medalist from the remaining 10 runners: 10 ways. Assign 3 medals to A, B, and the third person: $3! = 6$ ways. Total: $10 \times 6 = 60$ ✓
 
---
 
### Part 3 — Committee Selection
 
10 students: 6 men, 4 women. Committee of 4.
 
**1. Total committees**
 
$$\binom{10}{4} = \frac{10 \times 9 \times 8 \times 7}{24} = 210$$
 
**2. Exactly two women**
 
$$\binom{4}{2} \times \binom{6}{2} = 6 \times 15 = 90$$
 
**3. At least one woman**
 
Complement: all-male committees:
 
$$\binom{6}{4} = 15$$
 
$$\text{At least one woman} = 210 - 15 = 195$$
 
---
 
### Part 4 — Circular Seating
 
**1. 7 people around a round table**
 
$$(7-1)! = 6! = 720$$
 
**2. Two particular people sit next to each other**
 
Treat the pair as one unit → 6 units in a circle. Arrange the pair internally:
 
$$(6-1)! \times 2! = 5! \times 2 = 120 \times 2 = 240$$
 
---
 
### Part 5 — Passwords
 
Characters: digits $0–9$ (10) + letters $A–Z$ (26) = **36 characters total**. Password length: 5.
 
**1. Repetition allowed**
 
$$36^5 = 60{,}466{,}176$$
 
**2. No character may repeat**
 
$$P(36,5) = 36 \times 35 \times 34 \times 33 \times 32 = 45{,}239{,}040$$
 
**3. Counting model used**
 
- With repetition: **sequence with repetition** ($n^k = 36^5$)
- Without repetition: **k-permutation** ($P(n,k) = P(36,5)$)
 
Both use ordered selection because passwords are ordered (the password "AB123" is different from "321BA").
 
---
 
## Summary of Key Patterns
 
| Situation | Recognizing Signal | Model |
|---|---|---|
| "arrange all in a row" | all objects, order matters | Permutation $n!$ |
| "arrange around a table" | circular, relative position | $(n-1)!$ |
| "letters repeat in word" | identical objects | $\frac{n!}{n_1!\cdots}$ |
| "choose a committee/team" | subset, order irrelevant | Combination $\binom{n}{k}$ |
| "gold, silver, bronze" | distinct positions/ranks | k-Permutation $P(n,k)$ |
| "PIN code / password" | each position independent | Sequence $n^k$ |
| "at least one / at least two" | complement is easier | Total $-$ complement |
| "A and B must both be included" | fix them, count the rest | Fix + count remaining |
| "A and B must not be together" | complement: together case | Total $-$ together |