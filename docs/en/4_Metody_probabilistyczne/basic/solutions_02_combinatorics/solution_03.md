# Task 3 — Permutations with Repeated Elements
 
**1. Distinct arrangements of MISSISSIPPI**
 
Count the letters: M=1, I=4, S=4, P=2. Total letters: $1+4+4+2 = 11$.
 
$$\frac{11!}{1!\,4!\,4!\,2!} = \frac{39{,}916{,}800}{1 \times 24 \times 24 \times 2} = \frac{39{,}916{,}800}{1152} = 34{,}650$$
 
**2. Distinct arrangements of STATISTICS**
 
Count the letters: S=3, T=3, A=1, I=2, C=1. Total: $3+3+1+2+1 = 10$.
 
$$\frac{10!}{3!\,3!\,1!\,2!\,1!} = \frac{3{,}628{,}800}{6 \times 6 \times 1 \times 2 \times 1} = \frac{3{,}628{,}800}{72} = 50{,}400$$
 
**3. Arrangements of STATISTICS starting with S**
 
Fix S in position 1. Remaining letters: S=2, T=3, A=1, I=2, C=1 (9 letters left).
 
$$\frac{9!}{2!\,3!\,1!\,2!\,1!} = \frac{362{,}880}{2 \times 6 \times 1 \times 2 \times 1} = \frac{362{,}880}{24} = 16{,}800$$
 
> **Sanity check:** $16{,}800 / 50{,}400 = 1/3$. Since there are 3 S's among 10 letters, by symmetry exactly $1/3$ of all arrangements start with S. ✓