# Task 1 - Recognizing Counting Models

## Quick Reference — Counting Models
 
| Model | Formula | Order? | Repetition? | All objects? |
|---|---|---|---|---|
| Permutation | $n!$ | ✓ | ✗ | ✓ |
| Circular permutation | $(n-1)!$ | ✓ | ✗ | ✓ |
| Perm. with repeats | $\dfrac{n!}{n_1!\,n_2!\cdots}$ | ✓ | — | ✓ |
| Combination | $\dbinom{n}{k}$ | ✗ | ✗ | ✗ |
| k-Permutation | $\dfrac{n!}{(n-k)!}$ | ✓ | ✗ | ✗ |
| Sequence w/ repetition | $n^k$ | ✓ | ✓ | ✗ |
 
---
 
For each situation, the key questions are: *All objects? Order? Repetition? Identical objects?*
 
**1. Arranging 7 students in a line**
 
All 7 students, order matters, no repetition, all distinct.
 
$$\boxed{\text{Permutation}} \qquad P_7 = 7! = 5040$$
 
**2. Choosing 4 members of a committee from 12 people**
 
Only some chosen, order does NOT matter (a committee is a set), no repetition.
 
$$\boxed{\text{Combination}} \qquad \binom{12}{4} = 495$$
 
**3. Assigning gold, silver, bronze medals among 15 athletes**
 
Only 3 chosen from 15, order DOES matter (gold ≠ silver ≠ bronze), no repetition.
 
$$\boxed{\text{k-Permutation}} \qquad P(15,3) = \frac{15!}{12!} = 15 \times 14 \times 13 = 2730$$
 
**4. Forming a 6-digit PIN code**
 
Order matters, repetition IS allowed, selecting from 10 digits.
 
$$\boxed{\text{Sequence with repetition}} \qquad 10^6 = 1{,}000{,}000$$
 
**5. Arranging the letters of the word BANANA**
 
All 6 letters used, order matters, but some letters are identical:
- B: 1 time, A: 3 times, N: 2 times
 
$$\boxed{\text{Permutation with repeated elements}} \qquad \frac{6!}{1!\,3!\,2!} = \frac{720}{12} = 60$$
 
**6. Seating 6 people around a round table**
 
All 6, circular arrangement, only relative position matters.
 
$$\boxed{\text{Circular permutation}} \qquad (6-1)! = 5! = 120$$
 