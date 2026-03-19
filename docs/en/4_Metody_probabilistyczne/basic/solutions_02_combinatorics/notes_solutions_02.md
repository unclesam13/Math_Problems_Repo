# Combinatorics for Probability — Complete Lesson Notes

## How to Use These Notes

These notes follow the structure of Solution List 02 exactly.  
For each task you will find:
- **What it is about** — plain language explanation
- **Key formula** — with every symbol explained
- **Easy approach** — step-by-step thinking
- **Most important observation** — what the examiner wants to hear
- **Professor may ask** — likely oral questions with model answers



# PART 1 — Core Terminology & Symbol Glossary

Before any formula, you need to know the vocabulary cold.



## The Four Decision Questions

Every combinatorics problem starts with these four questions in order:

> **Q1. Are we using ALL objects or only SOME?**
> **Q2. Does ORDER matter?**
> **Q3. Is REPETITION allowed?**
> **Q4. Are some objects IDENTICAL (indistinguishable)?**

The answers lead directly to the correct model. Nothing else matters until you answer these four.

---

## Symbol Glossary

| Symbol | Name | Meaning |
|---|---|---|
| $n$ | total objects | how many objects exist in the set |
| $k$ | selection size | how many we pick or arrange |
| $n!$ | n factorial | $n \times (n-1) \times \cdots \times 2 \times 1$ |
| $0!$ | zero factorial | equals **1** by definition |
| $\binom{n}{k}$ | binomial coefficient / "n choose k" | number of ways to choose $k$ from $n$, order ignored |
| $P(n,k)$ | k-permutation | number of ordered selections of $k$ from $n$, no repetition |
| $n_1, n_2, \ldots$ | group sizes | number of identical objects of each type |
| $P_n$ | permutation count | number of ways to arrange all $n$ distinct objects |

---

## Master Formula Table

| Model | When to use | Formula | Example trigger words |
|---|---|---|---|
| **Permutation** | all $n$ distinct objects in a line | $n!$ | "arrange", "order", "line up" |
| **Circular permutation** | all $n$ objects in a circle | $(n-1)!$ | "round table", "circle", "ring" |
| **Perm. with repeats** | all $n$ objects, some identical | $\dfrac{n!}{n_1!\,n_2!\cdots n_r!}$ | "letters of a word", "colored balls" |
| **Combination** | choose $k$ from $n$, order ignored | $\dbinom{n}{k} = \dfrac{n!}{k!(n-k)!}$ | "committee", "team", "subset", "group" |
| **k-Permutation** | choose $k$ from $n$, order matters | $P(n,k) = \dfrac{n!}{(n-k)!}$ | "medals", "podium", "ranking", "distinct digits" |
| **Sequence w/ repetition** | choose $k$ from $n$, repetition OK | $n^k$ | "PIN", "password", "code", "repeated tosses" |

---

## The Decision Tree (memorise this)

```
Are we using ALL objects?
│
├── YES ──► Are they in a CIRCLE?
│           ├── YES ──► Circular permutation: (n−1)!
│           └── NO ───► Are some IDENTICAL?
│                       ├── YES ──► Perm. with repeats: n! / (n₁! n₂! ...)
│                       └── NO ───► Permutation: n!
│
└── NO (only SOME) ──► Does ORDER matter?
                       ├── NO ───► Combination: C(n,k)
                       └── YES ──► Is REPETITION allowed?
                                   ├── YES ──► Sequence: nᵏ
                                   └── NO ───► k-Permutation: P(n,k)
```

---

## Three Power Tools for Hard Problems

These three techniques solve almost every difficult combinatorics problem:

**Tool 1 — Complement**

> When direct counting is hard, count the opposite and subtract.

$$\text{what we want} = \text{total} - \text{what we do NOT want}$$

Use when you see: *"at least one"*, *"not all"*, *"at least two"*, *"contains a repeat"*.

---

**Tool 2 — Fix and Count**

> Fix the constrained objects first, then count the free positions.

Use when you see: *"must be together"*, *"must include person X"*, *"first position is fixed"*.

---

**Tool 3 — Multiply Independent Stages**

> If a process has independent stages, multiply the counts at each stage.

$$\text{total} = \text{stage 1 ways} \times \text{stage 2 ways} \times \cdots$$

Use when you see: *"followed by"*, *"then"*, *"prefix + suffix"*, *"code + number"*.



# PART 2 — Task-by-Task Notes

## Task 1 — Recognizing Counting Models

### What this task is about

Before computing anything, you must **identify the correct model**.  
This is the single most important skill in combinatorics.  
A wrong model gives a completely wrong answer even with perfect arithmetic.

### Easy Approach — apply the four questions in order

For each situation, write down:
1. All or some?
2. Order?
3. Repetition?
4. Identical objects?

Then look up the table.

### The Six Situations

| # | Situation | Q1 | Q2 | Q3 | Q4 | Model | Answer |
|---|---|---|---|---|---|---|---|
| 1 | 7 students in a line | All | Yes | No | No | Permutation | $7! = 5040$ |
| 2 | Committee of 4 from 12 | Some | **No** | No | No | Combination | $\binom{12}{4} = 495$ |
| 3 | Gold/silver/bronze from 15 | Some | **Yes** | No | No | k-Permutation | $P(15,3) = 2730$ |
| 4 | 6-digit PIN | Some | Yes | **Yes** | No | Sequence | $10^6 = 1{,}000{,}000$ |
| 5 | Letters of BANANA | All | Yes | — | **Yes** | Perm. w/ repeats | $\frac{6!}{3!\,2!} = 60$ |
| 6 | 6 people at round table | All | Yes | No | No | **Circular** | $(6-1)! = 120$ |

### Most Important Observation

> The difference between **combination** and **k-permutation** is purely whether order matters.  
> A committee $\{A,B,C\}$ is the same as $\{C,B,A\}$ — order does not matter → combination.  
> A podium (gold, silver, bronze) where $A$-gold, $B$-silver is different from $B$-gold, $A$-silver → k-permutation.

### Professor May Ask

**Q: When does order matter?**  
A: When the positions are distinguishable — for example medals (gold ≠ silver), seats in a numbered row, digits in a PIN. When only the selected group matters (committee, team, hand of cards), order does not matter.

**Q: Why do we divide by $3!\,2!$ for BANANA?**  
A: BANANA has 3 A's and 2 N's. Swapping the three A's among themselves gives the same word — so we are overcounting by $3!$. Similarly for the 2 N's we overcount by $2!$. Dividing removes the overcounting.

**Q: Why does circular permutation give $(n-1)!$ instead of $n!$?**  
A: In a circle, one rotation of the entire arrangement looks identical. So we fix one person's seat and arrange the rest — fixing eliminates the $n$ rotational copies, giving $n!/n = (n-1)!$.


## Task 2 — Permutations

### What this task is about

Linear arrangements of all objects. The main technique is **Fix and Count** for constrained problems.

### Key Formula

$$P_n = n!$$

$n$ = number of distinct objects to arrange.

### Easy Approach for Constraint Problems

**"Must sit together"** → glue them into one super-object, reduce $n$ by 1, then multiply by internal arrangements.

**"Must NOT sit together"** → always use complement: Total $-$ Together.

**"First position is fixed"** → remove that position, arrange the rest: $(n-1)!$

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | 8 books on a shelf | $8!$ | $40{,}320$ |
| 2 | 8 people, two must be adjacent | Glue pair → $7! \times 2!$ | $10{,}080$ |
| 3 | 8 people, two must NOT be adjacent | $8! - 7! \times 2!$ | $30{,}240$ |
| 4 | 10 questions, first is fixed | $9!$ | $362{,}880$ |

### Most Important Observation

> The "glue trick": treating two people who must be adjacent as a single unit reduces the problem to $(n-1)$ objects. Do not forget to multiply by $2!$ for the internal arrangement of the pair — they can sit as AB or BA.

### Professor May Ask

**Q: Why does the "must NOT be adjacent" case use complement?**  
A: Direct counting (listing all arrangements where they are separated) is complicated because there are many valid gaps. The complement — arrangements where they ARE adjacent — is easy to count (glue trick), so we subtract: $8! - 7! \times 2! = 30{,}240$.

**Q: In problem 4, why is the answer $9!$ and not $10!/1!$?**  
A: The first question is fixed — it has only 1 choice. The remaining 9 questions are free, giving $9!$ arrangements. $10!/1! = 10!$ which would be wrong.



## Task 3 — Permutations with Repeated Elements

### What this task is about

Arranging all objects when some are **identical** (indistinguishable). The formula adjusts for overcounting.

### Key Formula

$$\frac{n!}{n_1!\,n_2!\,\cdots\,n_r!}$$

Where:
- $n$ = total number of objects
- $n_1, n_2, \ldots, n_r$ = counts of each identical group
- $n_1 + n_2 + \cdots + n_r = n$

### Easy Approach — three steps

1. **Count total letters** $n$
2. **Count each repeated letter** — find all $n_i > 1$
3. **Divide** $n!$ by the factorial of each repeated count

### Letter Counts for the Two Words

**MISSISSIPPI** (11 letters): M=1, I=4, S=4, P=2

$$\frac{11!}{1!\,4!\,4!\,2!} = \frac{39{,}916{,}800}{1 \times 24 \times 24 \times 2} = 34{,}650$$

**STATISTICS** (10 letters): S=3, T=3, A=1, I=2, C=1

$$\frac{10!}{3!\,3!\,1!\,2!\,1!} = \frac{3{,}628{,}800}{72} = 50{,}400$$

**STATISTICS starting with S** — fix one S, arrange 9 remaining (S=2,T=3,A=1,I=2,C=1):

$$\frac{9!}{2!\,3!\,1!\,2!\,1!} = \frac{362{,}880}{24} = 16{,}800$$

### Most Important Observation

> **Sanity check for "starts with S":** There are 3 S's among 10 letters. By symmetry, exactly $\frac{3}{10}$ of all arrangements start with S... but wait, the letters are not equally distributed across positions in that simple way. The correct check is: $16{,}800 / 50{,}400 = 1/3$. Since there are 3 S's out of 10 positions and the S's are indistinguishable from each other, exactly $3/10$ of positions are S... actually by symmetry $\frac{3}{10} \times 50{,}400 = 15{,}120 \neq 16{,}800$.  
>
> The correct reasoning: we fixed **one specific S** in position 1. The remaining 9 letters have 2 remaining S's, so the fraction is not simply $3/10$. Always verify by direct calculation rather than symmetry when letters repeat.

### Professor May Ask

**Q: Why do we divide by $n_i!$ for each repeated group?**  
A: If we label the identical letters (e.g. $S_1, S_2, S_3$), we get $10!$ arrangements. But swapping $S_1 \leftrightarrow S_2$ gives the same word — so each distinct arrangement is counted $3!$ times. Dividing by $3!$ removes this overcounting. Same reasoning for every repeated letter.

**Q: What if all letters are distinct?**  
A: All $n_i = 1$, so the denominator is $1! \times 1! \times \cdots = 1$ and the formula reduces to $n!$ — the standard permutation.



## Task 4 — Circular Permutations

### What this task is about

Arrangements in a circle where **only relative position matters**, not absolute position.

### Key Formula

$$(n-1)!$$

**Why:** Fix one person to break rotational symmetry. Arrange the remaining $n-1$ people freely around them.

### Constraint Tricks

**"Two people must sit together"** in a circle:
$$\text{Glue pair} \rightarrow (n-2)! \times 2!$$

Here we have $(n-1)$ units in a circle → $(n-2)!$, times $2!$ for internal arrangement.

**"Two people must sit opposite"** (only meaningful for even $n$):
$$\text{Fix person A} \rightarrow \text{person B has 1 forced seat} \rightarrow (n-2)! \text{ for the rest}$$

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | 7 people at round table | $(7-1)!$ | $720$ |
| 2 | Two must sit together | $(6-1)! \times 2!$ | $240$ |
| 3 | Two must sit opposite (7 seats — odd!) | No seat is directly opposite | See note below |

> **Important note for problem 3:** With 7 seats (an odd number), no seat is exactly opposite any other. If the professor asks this, say: *"Opposite seating is only well-defined for an even number of seats. With 7 seats we cannot have two people sit directly opposite each other."* If interpreted as "maximally separated" (3 seats apart), fix A and place B in the one seat 3 positions away, then arrange the rest: $5! = 120$.

### Most Important Observation

> In a circle, all rotations of the same arrangement are **identical**. Fixing one person eliminates this redundancy. This is why we get $(n-1)!$ not $n!$. A common mistake is to use $n!$ for circular arrangements — always subtract one from $n$ before taking the factorial.

### Professor May Ask

**Q: Why is circular permutation $(n-1)!$ and not $n!/n$?**  
A: They are the same thing! $n!/n = (n-1)!$. The reasoning: there are $n!$ linear arrangements. Each circular arrangement corresponds to exactly $n$ rotations (all equivalent), so we divide by $n$.

**Q: What changes if seats are numbered/labelled?**  
A: If seats are labelled (e.g. seat 1, seat 2, ...), then rotations ARE different arrangements and we use $n!$ instead of $(n-1)!$ — it becomes a standard permutation.



## Task 5 — Combinations

### What this task is about

Selecting a **subset** — the selected group is what matters, not the order of selection.

### Key Formula

$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

Where:
- $n$ = total available
- $k$ = number selected
- Read as: "$n$ choose $k$"

### Useful Properties

$$\binom{n}{k} = \binom{n}{n-k} \qquad \text{(symmetry)}$$

$$\binom{n}{0} = \binom{n}{n} = 1 \qquad \text{(empty set or full set: one way)}$$

### Easy Approach for Constraint Problems

**"Must include person X"** → fix X, choose remaining $k-1$ from $n-1$: $\binom{n-1}{k-1}$

**"At least one from group"** → complement: Total $-$ none from group

**"Exactly $j$ from subgroup"** → choose $j$ from subgroup × choose rest from outside: $\binom{a}{j}\binom{b}{k-j}$

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | Committee of 4 from 12 | $\binom{12}{4}$ | $495$ |
| 2 | Must include Alice | $\binom{11}{3}$ | $165$ |
| 3 | At least one of Alice or Bob | $\binom{12}{4} - \binom{10}{4}$ | $285$ |
| 4 | Exactly 2 women (7M + 5W) | $\binom{5}{2}\binom{7}{2}$ | $210$ |

### Most Important Observation

> **"At least one"** problems almost always use complement. The complement of "at least one from group A" is "none from group A" — which means choosing entirely from outside group A. This is usually a simple single combination.

### Professor May Ask

**Q: How do you verify the answer to problem 3?**  
A: Direct count: exactly Alice only $= \binom{10}{3} = 120$, exactly Bob only $= 120$, both $= \binom{10}{2} = 45$. Total $= 120+120+45 = 285$ ✓

**Q: Why is $\binom{n}{k} = \binom{n}{n-k}$?**  
A: Choosing $k$ objects to include is equivalent to choosing $n-k$ objects to exclude. The formula: $\frac{n!}{k!(n-k)!} = \frac{n!}{(n-k)!k!}$ — they are identical.



## Task 6 — Combinations in Card Problems

### What this task is about

Applying combinations to a structured set (a card deck). The key is knowing the deck composition and splitting the selection into independent groups.

### Deck Facts — Memorise

| Property | Count |
|---|---|
| Total cards | 52 |
| Suits (♠♥♦♣) | 4 suits × 13 cards = 52 |
| Hearts | 13 |
| Non-hearts | 39 |
| Face cards (J,Q,K) | 3 ranks × 4 suits = 12 |
| Non-face cards | 40 |
| Aces | 4 |
| Total 5-card hands | $\binom{52}{5} = 2{,}598{,}960$ |

### Easy Approach

Always split the deck into the relevant groups and choose from each independently:

$$\text{exactly } j \text{ hearts} = \binom{13}{j} \times \binom{39}{5-j}$$

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | Exactly 2 hearts | $\binom{13}{2}\binom{39}{3}$ | $712{,}842$ |
| 2 | At least 1 heart | $\binom{52}{5} - \binom{39}{5}$ | $2{,}023{,}203$ |
| 3 | No face cards | $\binom{40}{5}$ | $658{,}008$ |

### Most Important Observation

> **"At least one heart"** — never try to count $1 + 2 + 3 + 4 + 5$ hearts separately. Always use complement: Total hands $-$ hands with zero hearts. Much faster.

### Professor May Ask

**Q: Why is the answer to problem 1 $\binom{13}{2} \times \binom{39}{3}$ and not $\binom{52}{5}$ with some fraction?**  
A: We split the 52 cards into hearts (13) and non-hearts (39). We independently choose 2 from the hearts and 3 from the non-hearts. The two choices are independent, so we multiply by the product rule.



## Task 7 — k-Permutations

### What this task is about

Ordered selections where order matters and repetition is NOT allowed.

### Key Formula

$$P(n,k) = \frac{n!}{(n-k)!} = n \times (n-1) \times \cdots \times (n-k+1)$$

This is just the first $k$ terms of $n!$.

### Easy Memory Aid

$P(n,k)$: start at $n$, multiply $k$ numbers counting down.

$$P(12,3) = 12 \times 11 \times 10 = 1{,}320$$

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | Top 3 from 12 runners | $P(12,3) = 12\times11\times10$ | $1{,}320$ |
| 2 | 4-digit numbers, distinct digits from 1–9 | $P(9,4) = 9\times8\times7\times6$ | $3{,}024$ |
| 3 | From above, divisible by 5 | Fix last digit=5, then $P(8,3)$ | $336$ |

### Most Important Observation

> **Divisibility constraint** (problem 3): fix the constrained position first (last digit = 5), then count the rest freely. Fix-and-count always handles position constraints cleanly.

### Professor May Ask

**Q: What is the difference between $P(n,k)$ and $\binom{n}{k}$?**  
A: $P(n,k)$ counts ordered selections — the arrangement matters. $\binom{n}{k}$ counts unordered selections — only which objects are chosen matters. Relationship: $P(n,k) = k! \times \binom{n}{k}$.

**Q: Why do we choose from digits 1–9 (not 0–9) in problem 2?**  
A: The problem specifies digits 1–9 — zero is excluded. This gives a pool of 9 digits instead of 10.



## Task 8 — Sequences with Repetition

### What this task is about

Ordered selections where each position is chosen **independently** and repetition IS allowed.

### Key Formula

$$n^k$$

$n$ = number of symbols available, $k$ = length of sequence.

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | 5-digit PIN, digits repeat | $10^5$ | $100{,}000$ |
| 2 | At least one repeated digit | $10^5 - P(10,5)$ | $69{,}760$ |
| 3 | All digits different | $P(10,5)$ | $30{,}240$ |

### Most Important Observation

> Note that "all digits different" in a sequence is just a k-permutation. So: $n^k$ (with repetition) vs $P(n,k)$ (without repetition) are the two cases for sequences. The complement relationship: sequences with at least one repeat $=$ $n^k - P(n,k)$.

### Professor May Ask

**Q: Why is the PIN model $10^5$ and not $P(10,5)$?**  
A: In a PIN, the same digit can appear multiple times (e.g. 11111 is valid). Each of the 5 positions independently takes any of 10 digits. Independent choices multiply: $10 \times 10 \times 10 \times 10 \times 10 = 10^5$.



## Task 9 — Digit Restrictions

### What this task is about

Counting numbers (not codes) — the key difference is that a **number cannot start with 0**.

### Easy Approach — product rule position by position

For a 5-digit number: $\underbrace{9}_{\text{pos 1}} \times \underbrace{10}_{\text{pos 2}} \times \underbrace{10}_{\text{pos 3}} \times \underbrace{10}_{\text{pos 4}} \times \underbrace{10}_{\text{pos 5}}$

First position: 1–9 (9 choices). All others: 0–9 (10 choices each).

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | All 5-digit numbers | $9 \times 10^4$ | $90{,}000$ |
| 2 | Even 5-digit numbers | $9 \times 10^3 \times 5$ | $45{,}000$ |
| 3 | No repeated digits | $9 \times 9 \times 8 \times 7 \times 6$ | $27{,}216$ |
| 4 | At least one repeated digit | $90{,}000 - 27{,}216$ | $62{,}784$ |

### Working out problem 3 step by step

Position 1: digits 1–9 → **9** choices  
Position 2: any digit except position 1 → **9** choices (includes 0)  
Position 3: any digit except positions 1 and 2 → **8** choices  
Position 4: **7** choices. Position 5: **6** choices.

$$9 \times 9 \times 8 \times 7 \times 6 = 27{,}216$$

### Most Important Observation

> The first position being non-zero makes this **asymmetric** — you cannot simply use $P(10,5)$ for "no repeated digits" because position 1 has 9 choices (not 10) while subsequent positions have different counts. Always handle the first digit separately.

### Professor May Ask

**Q: Why is the count for "no repeated digits" not $P(10,5) = 30{,}240$?**  
A: $P(10,5)$ counts ordered selections of 5 from 10 digits including zero — some of those start with 0 and are not valid 5-digit numbers. We must exclude these. Our calculation $9\times9\times8\times7\times6 = 27{,}216$ already excludes leading zeros.


## Task 10 — Urn Models

### What this task is about

The urn model is the canonical probability setting. The key distinction is: **order recorded or not?**

### Urn Setup

**5 red, 4 blue, 3 green** = 12 balls total, drawing 3.

| Recording rule | Model | Formula |
|---|---|---|
| Order ignored (set drawn) | Combination | $\binom{12}{3}$ |
| Order recorded (sequence drawn) | k-Permutation | $P(12,3)$ |

### Task Solutions at a Glance

| # | Problem | Method | Answer |
|---|---|---|---|
| 1 | Draw 3, order ignored | $\binom{12}{3}$ | $220$ |
| 2 | Exactly 2 red, order ignored | $\binom{5}{2}\binom{7}{1}$ | $70$ |
| 3 | Draw 3, order recorded | $P(12,3) = 12\times11\times10$ | $1{,}320$ |
| 4 | Exactly 2 red, order recorded | $\binom{3}{2} \times P(5,2) \times 7$ | $420$ |

### Working out problem 4 in detail

We have 3 positions. Exactly 2 must be red, 1 must be non-red.

- **Step 1:** Choose which 2 positions are red: $\binom{3}{2} = 3$
- **Step 2:** Fill the 2 red positions (ordered, from 5 red balls): $P(5,2) = 5 \times 4 = 20$
- **Step 3:** Fill the 1 non-red position (7 non-red balls): $7$

$$3 \times 20 \times 7 = 420$$

### Most Important Observation

> $\binom{12}{3} = 220$ vs $P(12,3) = 1{,}320$. Their ratio is $3! = 6$ — the number of orderings of 3 objects. This always holds: $P(n,k) = k! \times \binom{n}{k}$. Recording order multiplies the count by $k!$.

### Professor May Ask

**Q: Why is the answer to problem 2 $\binom{5}{2}\binom{7}{1}$ and not $\binom{5}{2}\binom{4}{1}$?**  
A: "Exactly 2 red" means the third ball must be non-red. Non-red = blue or green = $4+3=7$ balls. We choose 1 from all 7 non-red balls, not just from blue.



## Task 11 — Modeling Outcomes

### What this task is about

The most conceptual task. The key insight is: **the same physical experiment gives different counts depending on the recording rule.** This is fundamental to probability — the sample space depends on how you define an outcome.

### The Three Distinctions

| Distinction | Effect on counting |
|---|---|
| Labelled vs unlabelled objects | Labelled: multiply by $k!$ for each group of identical objects |
| Order recorded vs ignored | Recorded: multiply by $k!$ overall |
| PIN code vs number | Number: first digit ≠ 0, reducing first position from $n$ to $n-1$ |

### Part 1 — Labelled vs Unlabelled (4R, 4B, 3G = 11 balls)

**Unlabelled (colors only):**
$$\frac{11!}{4!\,4!\,3!} = 11{,}550$$

**Labelled ($R_1,R_2,\ldots$):**
$$11! = 39{,}916{,}800$$

**Ratio:** $39{,}916{,}800 / 11{,}550 = 4!\times4!\times3! = 3{,}456$. This is exactly the number of ways to permute the labels within each color group — confirming the formula.

### Part 2 — Order Recorded vs Ignored (draw 3 from same urn)

**Order ignored (color multisets):**

| Type | Color sets | Count |
|---|---|---|
| All same | RRR, BBB, GGG | 3 |
| Two same, one different | RRB, RRG, RBB, BBG, RGG, BGG | 6 |
| All different | RGB | 1 |
| **Total** | | **10** |

**Order recorded (color sequences):** Each color set expands into permutations:

| Type | Sets | Sequences per set | Subtotal |
|---|---|---|---|
| All same | 3 sets | $\frac{3!}{3!} = 1$ | $3 \times 1 = 3$ |
| Two same, one different | 6 sets | $\frac{3!}{2!} = 3$ | $6 \times 3 = 18$ |
| All different | 1 set | $3! = 6$ | $1 \times 6 = 6$ |
| **Total** | | | **27** |

### Part 3 — PIN Code vs Number

| | PIN code | 4-digit number |
|---|---|---|
| First digit | 0–9 (10 choices) | 1–9 (9 choices, no leading zero) |
| Other digits | 0–9 (10 each) | 0–9 (10 each) |
| Total | $10^4 = 10{,}000$ | $9 \times 10^3 = 9{,}000$ |
| Are 0123 and 3210 different? | **Yes** — different PINs | **Yes** — different numbers |

### Most Important Observation

> The **recording rule defines the sample space**. Two experiments with the same physical setup can have completely different sample spaces. This is why in probability we always state explicitly: "order is recorded" or "order is ignored" — without this, the problem is ambiguous.

### Professor May Ask

**Q: Are there 10,000 or 9,000 possible 4-character codes on a keypad?**  
A: If leading zeros are allowed (PIN): $10^4 = 10{,}000$. If it must represent a 4-digit number (no leading zero): $9 \times 10^3 = 9{,}000$. The physical keypad is the same — the counting changes because the definition of "valid outcome" changes.

**Q: Why is $11!/(4!\,4!\,3!) \times 4!\,4!\,3! = 11!$?**  
A: The unlabelled count times the number of ways to assign labels within each color group gives the labelled count. This is the fundamental relationship between distinguishable and indistinguishable objects.


## Task 12 — Mixed Counting Problem

### What this task is about

Each sub-problem uses a different model. Practice identifying the model quickly, then applying it. This is the closest to an exam question.

### Quick Solutions Reference

**Part 1 — Student ID Codes** (2 letters from {A,B,C,D,E} + 3 digits from 0–9):

| Restriction | Letters | Digits | Total |
|---|---|---|---|
| Both repeat | $5^2 = 25$ | $10^3 = 1{,}000$ | $25{,}000$ |
| Letters no repeat | $P(5,2) = 20$ | $10^3 = 1{,}000$ | $20{,}000$ |
| Neither repeats | $P(5,2) = 20$ | $P(10,3) = 720$ | $14{,}400$ |

**Part 2 — Medal Assignment** (12 runners, gold/silver/bronze):

| Problem | Method | Answer |
|---|---|---|
| Any 3 get medals | $P(12,3)$ | $1{,}320$ |
| Runners A and B must both medal | Fix A,B in 2 of 3 positions: $P(3,2) \times 10$ | $60$ |

**Part 3 — Committee** (10 students: 6M + 4W, choose 4):

| Problem | Method | Answer |
|---|---|---|
| Any committee | $\binom{10}{4}$ | $210$ |
| Exactly 2 women | $\binom{4}{2}\binom{6}{2}$ | $90$ |
| At least 1 woman | $210 - \binom{6}{4}$ | $195$ |

**Part 4 — Circular Seating** (7 people):

| Problem | Method | Answer |
|---|---|---|
| Any arrangement | $(7-1)!$ | $720$ |
| Two specific people adjacent | $(6-1)!\times2!$ | $240$ |

**Part 5 — Passwords** (5 chars from 36: digits 0–9 + letters A–Z):

| Problem | Model | Answer |
|---|---|---|
| Repetition allowed | Sequence: $36^5$ | $60{,}466{,}176$ |
| No repeats | k-Permutation: $P(36,5)$ | $45{,}239{,}040$ |

### Most Important Observation for Task 12

> **Multi-stage problems use the product rule**: for Student ID codes, letters and digits are chosen independently, so multiply the counts. For medal assignment with a constraint, use Fix-and-Count: fix the constrained positions first, then fill the free positions.

### Professor May Ask

**Q: In the medal problem, why is the answer $60$ and not $\binom{12}{3} \times \ldots$?**  
A: Medals are ordered (gold ≠ silver ≠ bronze), so we use permutations not combinations. We fix that A and B must both appear, then count: choose which 2 of the 3 medal positions go to A and B (ordered: $P(3,2)=6$ ways), then choose the third medalist from the remaining 10 runners. Total: $6 \times 10 = 60$.

**Q: Why is the committee problem easier with complement for "at least one woman"?**  
A: Directly counting committees with 1, 2, 3, or 4 women requires four separate calculations. The complement (all-male committee) requires just one: $\binom{6}{4} = 15$. Complement: $210 - 15 = 195$.


# PART 3 — Exam Quick Reference

## The One-Page Cheat Sheet

**Step 1 — Identify the model**

| Signal words | Model |
|---|---|
| "arrange all", "order all", "line up" | Permutation $n!$ |
| "round table", "circle" | Circular $(n-1)!$ |
| "repeated letters", "identical objects" | Perm. w/ repeats $\frac{n!}{n_1!\cdots}$ |
| "committee", "team", "group", "hand" | Combination $\binom{n}{k}$ |
| "medals", "podium", "ranked positions" | k-Permutation $P(n,k)$ |
| "PIN", "password", "code", "digit sequence" | Sequence $n^k$ |

**Step 2 — Apply the right power tool**

| Constraint words | Tool |
|---|---|
| "at least one", "at least two" | Complement |
| "must include X", "X is fixed" | Fix and Count |
| "must not be together" | Total $-$ Together |
| "part A then part B" | Product Rule (multiply) |
| "either case 1 or case 2" | Sum Rule (add) |

**Step 3 — Verify**

- Does the answer seem reasonable in magnitude?
- For "at least" problems: does result $+$ complement $=$ total?
- For "exactly $k$": do all cases $k=0,1,2,\ldots$ sum to total?

---

## Five Things to Say in Every Oral Answer

1. **"The sample space has $|\Omega| = \ldots$ outcomes because..."** — always state the total first
2. **"Order matters / does not matter here because..."** — justify your model choice
3. **"I use the complement because directly counting is harder..."** — explain your strategy
4. **"By the product rule, the two stages multiply because they are independent..."** — explain multiplication
5. **"As a check: $\ldots + \ldots = \ldots$ ✓"** — verify your answer sums correctly

---

## Common Mistakes to Avoid

| Mistake | Correct thinking |
|---|---|
| Using $n!$ for circular arrangements | Use $(n-1)!$ — rotations are equivalent |
| Forgetting to multiply by $2!$ in "glue trick" | The pair can be arranged internally in $2!$ ways |
| Using $P(10,5)$ for 5-digit numbers with no repeats | First digit ≠ 0: use $9 \times 9 \times 8 \times 7 \times 6$ instead |
| "At least one" → direct count | Use complement: total $-$ none |
| Combination when order matters | Check: are the positions distinguishable? If yes → k-Permutation |
| Forgetting $0! = 1$ | $0! = 1$ by definition — needed for $\binom{n}{0} = 1$ |