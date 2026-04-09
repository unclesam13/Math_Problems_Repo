# Task 11 — Modeling Outcomes
 
### Part 1 — Distinguishable vs Indistinguishable
 
Balls: 4 red, 4 blue, 3 green → 11 total.
 
**1. Arrangements if same-color balls are indistinguishable**
 
Permutation with repeated elements:
 
$$\frac{11!}{4!\,4!\,3!} = \frac{39{,}916{,}800}{24 \times 24 \times 6} = \frac{39{,}916{,}800}{3{,}456} = 11{,}550$$
 
**2. Arrangements if every ball is individually labeled ($R_1,\ldots,R_4, B_1,\ldots,B_4, G_1,G_2,G_3$)**
 
All 11 objects are now distinct — standard permutation:
 
$$11! = 39{,}916{,}800$$
 
**3. Why are the answers different?**
 
When balls are labeled, swapping $R_1$ and $R_2$ produces a **new** arrangement. When they are indistinguishable, swapping any two red balls gives the **same** arrangement. The labeled count overcounts each color-pattern by $4! \times 4! \times 3!$ — dividing by this factor gives the unlabeled count.
 
---
 
### Part 2 — Recording Order vs Ignoring Order

Three balls drawn without replacement from the same box (11 balls: 4R, 4B, 3G).

**1. Only the set of colors recorded (order ignored)**

We list all achievable color combinations of 3 balls. Each row is a multiset — only
how many of each color matters, not which order they were drawn.

| Reds | Blues | Greens | Color set |
|---|---|---|---|
| 3 | 0 | 0 | RRR |
| 0 | 3 | 0 | BBB |
| 0 | 0 | 3 | GGG |
| 2 | 1 | 0 | RRB |
| 2 | 0 | 1 | RRG |
| 1 | 2 | 0 | RBB |
| 0 | 2 | 1 | BBG |
| 1 | 0 | 2 | RGG |
| 0 | 1 | 2 | BGG |
| 1 | 1 | 1 | RGB |

All combinations satisfy the urn constraints (≤4R, ≤4B, ≤3G), so all 10 are valid.

$$\text{Total distinct color sets} = 10$$

**2. Sequence of colors recorded (order matters)**

Now $RBG$ and $BRG$ are different outcomes. Each color set from part (1) expands
into multiple ordered sequences depending on how many repeated colors it contains.
We use the permutation with repeated elements formula $\dfrac{3!}{n_R!\,n_B!\,n_G!}$
for each group:

| Type | Color sets | Sequences per set | Subtotal |
|---|---|---|---|
| All same color | RRR, BBB, GGG | $\dfrac{3!}{3!} = 1$ | $3 \times 1 = 3$ |
| Two of one, one different | RRB, RRG, RBB, BBG, RGG, BGG | $\dfrac{3!}{2!} = 3$ | $6 \times 3 = 18$ |
| All different | RGB | $3! = 6$ | $1 \times 6 = 6$ |

$$\text{Total distinct color sequences} = 3 + 18 + 6 = \boxed{27}$$

**3. Why does recording order change the count?**

When order is ignored, $\{R,B,G\}$ is a single outcome — we only care *which* colors
were drawn. When order is recorded, $RBG$, $RBG$, $BRG$, $BGR$, $GRB$, $GBR$ are
**six separate outcomes** — we care about *when* each color appeared. This is why
the same physical experiment gives 10 outcomes under one recording rule and 27 under
another: the recording rule defines what counts as "the same result."
 
---
 
### Part 3 — PIN Code vs Number
 
**1. PIN codes (digits 0–9, repetition allowed)**
 
$$10^4 = 10{,}000$$
 
**2. 4-digit numbers (first digit ≠ 0)**
 
$$9 \times 10^3 = 9{,}000$$
 
**3. Why counted differently?**
 
A PIN code is a sequence of symbols — "0123" is a valid PIN. A 4-digit number cannot start with 0 (that would make it a 3-digit number). So the model is the same (sequences with repetition) but with an additional constraint on the first position.
 
**4. Why are 1234 and 4321 different outcomes?**
 
A PIN is an **ordered sequence** — the order in which digits appear is part of the information. Entering 1234 is a different action from entering 4321, and they unlock different things. Order is always recorded in PINs.
 
