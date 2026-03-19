# Task 9 — Digit Restrictions
 
**1. How many 5-digit numbers exist?**
 
First digit: 1–9 (cannot be 0) → 9 choices. Remaining 4 digits: 0–9 → 10 choices each.
 
$$9 \times 10^4 = 90{,}000$$
 
> **Note:** 5-digit numbers range from 10000 to 99999 — exactly 90,000 numbers. ✓
 
**2. How many are even?**
 
Last digit must be even: $\{0,2,4,6,8\}$ — 5 choices. First digit: 1–9 → 9 choices. Middle 3 digits: 10 choices each.
 
$$9 \times 10 \times 10 \times 10 \times 5 = 45{,}000$$
 
**3. How many contain no repeated digits?**
 
First digit: 9 choices (1–9). 
Second: 9 choices (0–9 minus first digit).
Third: 8 choices. Fourth: 7. Fifth: 6.
 
$$9 \times 9 \times 8 \times 7 \times 6 = 27{,}216$$
 
**4. How many contain at least one repeated digit?**
 
Complement of (3):
 
 $$90{,}000 - 27{,}216 = 62{,}784$$