# TASK LIST NO. 3: Parameters of Random Variable Distribution
(Expected value, variance, moments, correlation)

## Task 1
For a random variable $X$ with the probability function given by the table:

| $x_i$ | -2 | 2 | 4 |
| :--- | :--- | :--- | :--- |
| $p_i$ | 0.5 | 0.3 | 0.2 |

Determine:

1. The expected value $E(X)$ (mean).
2. The variance $D^2(X)$ (using the formula $D^2(X) = E(X^2) - (EX)^2$).
3. The standard deviation $\sigma$.
4. The median $x_{0.5}$ (middle value).

## Task 2
The monthly cost $U$ of running a certain system depends on the number $X$ of active users (employees) according to the formula:

$$
U = 15000X + 10000\sqrt{X}
$$

The number of employees $X$ is a random variable with the distribution:

| $x_i$ | 2 | 3 | 4 | 5 |
| :--- | :--- | :--- | :--- | :--- |
| $p_i$ | 0.10 | 0.25 | 0.40 | 0.25 |

Calculate the predicted average monthly cost, i.e., the expected value of the variable $U$.

*Hint: Calculate $u_i$ for each $x_i$, and then apply the formula for the expected value.*

## Task 3
A random variable $X$ (e.g., measurement error) has a distribution with the density:

$$
f(x) = \begin{cases}6x(1-x) & \text{for } 0 < x < 1 \\0 & \text{for other } x\end{cases}
$$

Calculate the average (expected) value and the variance of this variable. Then calculate the variance of the linearly dependent variable $Y = 2X - 1$ (use the property of variance: $D^2(aX+b) = a^2 D^2(X)$).

## Task 4
A random variable $X$ has a distribution with the density:

$$
f(x) = \begin{cases}\frac{1}{2}x & \text{for } 0 \leqslant x \leqslant 2 \\0 & \text{otherwise}\end{cases}
$$

Determine the mode (the value for which the density is greatest) and the median (the value that divides the area under the density graph into two equal halves).

## Task 5
The height of people in a certain group is a random variable $X$ with a mean $EX = 170$ cm and a standard deviation $\sigma_X = 5$ cm. The mass of these people is a variable $Y$ with a mean $EY = 65$ kg and a standard deviation $\sigma_Y = 5$ kg.

Which feature (height or weight) is more "stable" (has a smaller relative dispersion)?

*Hint: Calculate the coefficient of variation $v = \frac{\sigma}{EX}$ for both variables.*

## Task 6
The probability of not exceeding the daily electricity consumption limit by a certain plant is $p=0.8$. We observe this plant for $n=5$ days. Let $X$ denote the number of days in which the limit was not exceeded.

1. What type of distribution is this? Provide the formula for the probability $P(X=k)$.
2. Calculate the expected value and variance of the variable $X$, using the ready-made formulas for this distribution ($EX=np$, $D^2X=npq$).

## Task 7
The time (in minutes) between consecutive subscriber calls at a telephone exchange is a random variable with an exponential distribution with the parameter (expected value) $\lambda = 2$.

1. Calculate the average waiting time for a call ($EX$).
2. Calculate the probability that the time between calls will be shorter than 3 minutes ($P(X<3)$).

## Task 8
A machine produces weights. Mass measurement errors have a normal distribution with an expected value $\mu=0$ g and a standard deviation $\sigma=0.01$ g. Calculate the probability that the measurement error (in terms of modulus) does not exceed $0.02$ g.

*Hint: Use the cumulative distribution function of the standardized normal distribution $\Phi(u)$. Note that $P(|X|<a) = P(-a < X < a)$.*

## Task 9
Given is a two-dimensional random variable $(X, Y)$ with the distribution given in the table (representing, for example, test results at two different moments in time):

| $y_k \backslash x_i$ | 8 | 9 | 10 | 11 |
| :--- | :--- | :--- | :--- | :--- |
| **1.2** | 0.10 | 0.04 | 0 | 0 |
| **1.3** | 0.05 | 0.11 | 0.20 | 0 |
| **1.4** | 0 | 0.10 | 0.15 | 0.10 |
| **1.5** | 0 | 0 | 0.05 | 0.10 |

Calculate the linear correlation coefficient $\rho$ between variables $X$ and $Y$.

*Hint: Calculate sequentially: means $EX, EY$, variances $D^2X, D^2Y$, and the mixed moment $E(XY) = \sum x_i y_k p_{ik}$. Covariance is $cov(X,Y) = E(XY) - EX \cdot EY$.*

## Task 10

Let $X$ and $Y$ be independent random variables with zero expected values ($EX=0, EY=0$). Show that the following equality holds:

$$E(X^3 Y) = E(X^3)E(Y)$$

Does the variable $Z = X^3 Y$ have an expected value equal to 0? What does this mean in the context of random signals (noise)?