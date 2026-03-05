# Solution 3 – Classical Probability

## Given

A person completes a job in **4, 5, or 6 hours** and may make **0, 1, or 2 errors**.

Thus there are:

$$
3 \times 3 = 9
$$

equally likely elementary outcomes.

Each outcome is a pair:

$$
(\text{time}, \text{errors})
$$



## Sample Space

$$
\Omega =
\{
(4,0),(4,1),(4,2),
(5,0),(5,1),(5,2),
(6,0),(6,1),(6,2)
\}
$$

Each event has probability

$$
\frac{1}{9}
$$



## 1. Job completed in 4 hours

Possible outcomes:

$$
(4,0),(4,1),(4,2)
$$

Number of favorable outcomes:

$$
3
$$

Probability:

$$
P = \frac{3}{9} = \frac{1}{3}
$$



## 2. Job completed flawlessly in 6 hours

Outcome:

$$
(6,0)
$$

Probability:

$$
P = \frac{1}{9}
$$



## 3. Job completed in at most 5 hours

Possible times: $4$ or $5$.

Outcomes:

$$
6
$$

Probability:

$$
P = \frac{6}{9} = \frac{2}{3}
$$



## 4. Job completed in at most 5 hours and with at most one error

Allowed outcomes:

$$
(4,0),(4,1),(5,0),(5,1)
$$

Number of outcomes:

$$
4
$$

Probability:

$$
P = \frac{4}{9}
$$