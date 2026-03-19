# Task 8 — Sequences with Repetition
 
**1. 5-digit PIN codes (digits may repeat)**
 
Each of 5 positions: 10 choices (0–9), independently:
 
$$10^5 = 100{,}000$$
 
**2. Codes with at least one repeated digit**
 
Complement: all digits different. Choose and arrange 5 distinct digits from 10:
 
$$P(10,5) = 10 \times 9 \times 8 \times 7 \times 6 = 30{,}240$$
 
$$\text{At least one repeat} = 100{,}000 - 30{,}240 = 69{,}760$$
 
**3. Codes with all digits different**
 
As computed above:
 
$$P(10,5) = 30{,}240$$
 