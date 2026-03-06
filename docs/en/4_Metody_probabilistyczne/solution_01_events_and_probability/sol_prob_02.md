# # Solution 1 – Task 2


## Given

An electrical circuit consists of element $a_1$ connected **in series** with a block of two elements $a_2$ and $a_3$ connected **in parallel**.

Let $A_i$ denote the event that element $a_i$ is functional at time $t$.

Describe the event

$$
A
$$

meaning that **current flows through the circuit without interruption**, using set operations.



## Understanding the System

For current to flow through the system:

- element $a_1$ must work (series connection)
- at least one of $a_2$ or $a_3$ must work (parallel connection)

Parallel connection corresponds to **union** of events.

Series connection corresponds to **intersection**.



## Step-by-Step Reasoning

The parallel block works if:

$$
A_2 \cup A_3
$$

The whole system works if:

- $a_1$ works
- and the parallel block works

Thus the system event is

$$
A = A_1 \cap (A_2 \cup A_3)
$$



## Final Result

$$
A = A_1 \cap (A_2 \cup A_3)
$$