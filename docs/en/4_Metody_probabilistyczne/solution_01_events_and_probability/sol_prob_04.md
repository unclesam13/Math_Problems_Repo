# Solution 4 – Parallel System Reliability

## Given

Two elements $a_1$ and $a_2$ are connected in **parallel**.

Let:

$$
P(A_1) = P(A_2) = p
$$

and

$$
P(A_1 \cap A_2) = p^2
$$

Find the probability that the current flows for at least time $t$.



## Understanding the System

A parallel system works if **at least one element works**.

Thus the event is:

$$
A = A_1 \cup A_2
$$



## Probability Formula

Using the union formula:

$$
P(A_1 \cup A_2) =
P(A_1) + P(A_2) - P(A_1 \cap A_2)
$$

Substituting the values:

$$
P(A) = p + p - p^2
$$



## Final Result

$$
P(A) = 2p - p^2
$$