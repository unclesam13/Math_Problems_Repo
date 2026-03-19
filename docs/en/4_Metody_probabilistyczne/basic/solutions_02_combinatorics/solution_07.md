# Task 7 — k-Permutations (Ordered Selections Without Repetition)
 
**1. First three places among 12 runners**
 
Order matters (gold≠silver≠bronze), no repetition, select 3 from 12:
 
$$P(12,3) = \frac{12!}{9!} = 12 \times 11 \times 10 = 1{,}320$$
 
**2. 4-digit numbers with distinct digits from 1–9**
 
Digits: $\{1,2,...,9\}$ — 9 options. Order matters, no repetition, choose 4:
 
$$P(9,4) = \frac{9!}{5!} = 9 \times 8 \times 7 \times 6 = 3{,}024$$
 
**3. From above, how many are divisible by 5?**
 
Divisible by 5 → last digit must be 5. Fix last digit = 5.
 
Choose and arrange the first 3 digits from the remaining 8 digits (1–9 excluding 5):
 
$$P(8,3) = 8 \times 7 \times 6 = 336$$