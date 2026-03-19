# Task 2 — Permutations
 
**1. Arranging 8 different books on a shelf**
 
All 8 distinct books, order matters, linear arrangement:
 
$$P_8 = 8! = 40{,}320$$
 
**2. 8 people in a row - two particular people MUST sit together**
 
Treat the pair as a single "super-person". Now we arrange 7 units:
 
$$7! \text{ arrangements of units} \times 2! \text{ arrangements within the pair} = 7! \times 2 = 5040 \times 2 = 10{,}080$$
 
**3. 8 people in a row - two particular people must NOT sit together**
 
Use the complement:
 
$$\text{Total} - \text{together} = 8! - 7! \times 2! = 40{,}320 - 10{,}080 = 30{,}240$$
 
**4. 10 questions - first question is fixed**
 
The first position is determined. The remaining 9 questions can be ordered freely:
 
$$9! = 362{,}880$$
 