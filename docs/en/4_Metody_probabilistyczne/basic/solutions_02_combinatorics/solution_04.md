# Task 4 — Circular Permutations
 
**1. 7 people around a round table**
 
Fix one person to eliminate rotational equivalence:
 
$$(7-1)! = 6! = 720$$
 
**2. 7 people — two particular people MUST sit together**
 
Glue the pair into one unit → 6 units around a circle. Then arrange the pair internally:
 
$$(6-1)! \times 2! = 5! \times 2 = 120 \times 2 = 240$$
 
**3. 7 people — two particular people must sit OPPOSITE each other**
 
This requires an even number of seats for "exactly opposite" to be well-defined. With 7 seats (odd), there is no seat directly opposite any given seat. 
 
> **Note:** If interpreted as "as far apart as possible" — seats are labelled $1,2,...,7$ around the circle. Fix person A in seat 1. The seat most nearly opposite is seat 4 (distance 3). Person B has only 1 forced position. The remaining 5 people fill seats freely:
 
$$5! = 120$$
 
Alternatively, if the problem intends a **6-person** table (which is the standard version):
 
Fix person A. Person B can sit in the 1 seat directly opposite. The remaining 4 people arrange freely:
 
$$1 \times 4! = 24$$


### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | 7 people at round table | $(7-1)!$ | $720$ |
| 2 | Two must sit together | $(6-1)! \times 2!$ | $240$ |
| 3 | Two must sit opposite (7 seats — odd!) | No seat is directly opposite | See note below |


### Most Important Observation

> In a circle, all rotations of the same arrangement are **identical**. Fixing one person eliminates this redundancy. This is why we get $(n-1)!$ not $n!$. A common mistake is to use $n!$ for circular arrangements — always subtract one from $n$ before taking the factorial.