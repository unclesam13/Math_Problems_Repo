# Task 5 — Combinations
 
**1. Committees of 4 from 12 students**
 
$$\binom{12}{4} = \frac{12!}{4!\,8!} = \frac{12 \times 11 \times 10 \times 9}{4 \times 3 \times 2 \times 1} = \frac{11{,}880}{24} = 495$$
 
**2. Committees containing a particular student (call them Alice)**
 
Alice is fixed. Choose remaining 3 from 11:
 
$$\binom{11}{3} = \frac{11 \times 10 \times 9}{6} = 165$$
 
**3. Committees containing at least one of two particular students (Alice or Bob)**
 
Use the complement — committees with **neither** Alice nor Bob (choose 4 from remaining 10):
 
$$\binom{10}{4} = 210$$
 
$$\text{At least one of Alice/Bob} = \binom{12}{4} - \binom{10}{4} = 495 - 210 = 285$$
 
**Verification using direct count:**
 
- Exactly Alice only: $\binom{10}{3} = 120$
- Exactly Bob only: $\binom{10}{3} = 120$
- Both Alice and Bob: $\binom{10}{2} = 45$
- Total: $120 + 120 + 45 = 285$ ✓
 
**4. Exactly two women — group has 7 men and 5 women**
 
Choose 2 women from 5, then 2 men from 7:
 
$$\binom{5}{2} \times \binom{7}{2} = 10 \times 21 = 210$$
 