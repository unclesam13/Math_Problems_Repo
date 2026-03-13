# TASK LIST NO. 2: Random Variables (One-dimensional and Two-dimensional)

## Task 1
A test was conducted in a student group. Let $X$ denote the grade (on the grading scale 2–5) of a randomly selected student. Is $X$ a random variable?

If we assume that the group consists of 10 people, and their grades form the set $\{5, 4, 3, 3, 4, 5, 3, 3, 4, 2\}$, how should this random variable be defined, and what is the probability of obtaining individual grades?

## Task 2
Assuming that the ratio of very good, good, satisfactory, and failing grades is $1:3:4:2$, determine for the random variable $X$ defined there:

1. the probability mass function and its graph,
2. the cumulative distribution function (CDF) and its graph,
3. the probability $P(X < 3.5)$.

## Task 3
The monthly cost $u$ of running an example laboratory depends on the number $x$ of employees hired. Let us assume that this dependence is of the form:

$$
u = 15000x + 10000\sqrt{x}
$$

The number of employees is treated as a random variable $X$ with the distribution:

| $x_i$ | 2 | 3 | 4 | 5 |
| :--- | :--- | :--- | :--- | :--- |
| $p_i$ | 0.10 | 0.25 | 0.40 | 0.25 |

Determine the probability function of costs (random variable $U$).

## Task 4
In many situations (e.g., in computer science and electronics), it can be assumed that the time $X$ of failure-free operation of a tested device is a continuous random variable with the density:

$$
f(x) = \begin{cases}\frac{1}{\lambda} \exp\left(-\frac{x}{\lambda}\right) & \text{for } x > 0 \\0 & \text{for other } x\end{cases}
$$

(this is the so-called exponential distribution). Let the parameter $\lambda = 10$ (e.g., hours).

1. Calculate the probability that the device will operate without failure from 5 to 10 hours: $P(5 \leqslant X \leqslant 10)$.
2. Determine the cumulative distribution function of this random variable.

## Task 5
Select constants $A$ and $B$ such that the function defined by the formula:

$$
F(x) = A + B \arctan x \quad \text{for } -\infty < x < \infty
$$

is the cumulative distribution function of a certain continuous random variable $X$. Then determine the density of this variable.

## Task 6
A certain mechanism consists of two gears: a large one and a small one. Technical conditions during the assembly of the device are violated if both gears have positive thickness deviations ("plus") or if both have negative deviations ("minus"). Consider zero-one random variables $X$ and $Y$:

* $X=1$, if the large gear is "plus", $X=0$ if "minus".
* $Y=1$, if the small gear is "plus", $Y=0$ if "minus".

The probabilities of these events occurring are as follows:
$P(X=0, Y=0) = P(X=1, Y=1) = \frac{1}{4}$ (failure/bad assembly)
$P(X=0, Y=1) = P(X=1, Y=0) = \frac{1}{4}$ (good assembly)

Determine the joint distribution table of this two-dimensional variable and calculate the probability that the assembly is correct.

## Task 7
The two-dimensional random variable $(X, Y)$ has a distribution defined in the table:

| $Y \backslash X$ | 1 | 2 | 3 |
| :--- | :--- | :--- | :--- |
| **2** | 0.1 | 0.2 | 0.3 |
| **4** | 0.1 | 0.1 | 0.2 |

Determine the cumulative distribution function of the marginal distribution of the random variable $Y$.

## Task 8
Two people from city A are trying to establish a telephone connection with city B. Let $X$ denote the number of attempts by the first person, and $Y$ – the number of attempts by the second person. We assume that each person connects independently. It is known that the probability distributions of the number of attempts for both persons are as follows:

* For person 1 ($X$): $P(X=1)=0.6$, $P(X=2)=0.4$
* For person 2 ($Y$): $P(Y=1)=0.5$, $P(Y=2)=0.5$

Determine the joint distribution of the two-dimensional variable $(X, Y)$ (table), assuming the independence of attempts by both persons.

## Task 9
Select the constant $c$ such that the function:

$$
f(x, y) = \begin{cases}cxy & \text{for } 0 \leqslant x \leqslant 2 \land 0 \leqslant y \leqslant 1 \\0 & \text{for other } (x, y)\end{cases}
$$

is the density of the two-dimensional random variable $(X, Y)$.

## Task 10
For the density function from Task 9 (after determining $c$), determine the marginal densities $f_1(x)$ and $f_2(y)$. Check whether the variables $X$ and $Y$ are independent (i.e., whether $f(x,y) = f_1(x) \cdot f_2(y)$).
