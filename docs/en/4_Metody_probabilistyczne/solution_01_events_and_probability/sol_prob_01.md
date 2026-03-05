# Solution 1 - Task 1

## Given

$\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}$

This is the sample space of the experiment, so there are five possible elementary outcomes.

$A = \{\omega_1, \omega_3, \omega_5\}$

$B = \{\omega_2, \omega_3, \omega_4\}$

Need to find (in this order):

1. $A \cup B$  
2. $A \cap B$  
3. $B \setminus A$  
4. $A \setminus B$

## My approach

First I wrote the elements of $A$ and $B$ next to each other to see which outcomes overlap.

I immediately noticed that $\omega_3$ appears in both sets - that's the intersection. Helps to imagine two circles (Venn diagram) with $\omega_3$ in the overlap.

To avoid confusion I remind myself:

- $\cup$ = "or" - everything in $A$ or $B$
- $\cap$ = "and" - only what's in both
- $B \setminus A$ = in $B$ but not in $A$ (order matters - I used to mix this up)

## 1. $A \cup B$

Take all elements from both sets, no duplicates.

$A$: $\omega_1, \omega_3, \omega_5$  
$B$: $\omega_2, \omega_3, \omega_4$

$$
A \cup B = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\} = \Omega
$$

That's the whole sample space - every outcome is in at least one of the events.

## 2. $A \cap B$

Only elements that appear in both sets. From the lists above, only $\omega_3$.

$$
A \cap B = \{\omega_3\}
$$

## 3. $B \setminus A$

Elements in $B$ but not in $A$. From $B = \{\omega_2, \omega_3, \omega_4\}$ remove $\omega_3$.

$$
B \setminus A = \{\omega_2, \omega_4\}
$$

## 4. $A \setminus B$

Elements in $A$ but not in $B$. From $A = \{\omega_1, \omega_3, \omega_5\}$ remove $\omega_3$.

$$
A \setminus B = \{\omega_1, \omega_5\}
$$

Note: $B \setminus A \neq A \setminus B$ - different elements get removed.

## Result

$$
A \cup B = \Omega
$$

$$
A \cap B = \{\omega_3\}
$$

$$
B \setminus A = \{\omega_2, \omega_4\}
$$

$$
A \setminus B = \{\omega_1, \omega_5\}
$$

## Sanity check

All results are subsets of $\Omega$ - no extra elements.

The three parts $(A \cap B)$, $(B \setminus A)$, $(A \setminus B)$ don't overlap and together give $A \cup B = \Omega$.