# TASK LIST NO. 10: Advanced Statistical Methods

## Task 1 (Runs Test - Randomness of a Sample)
A sample of size $n=20$ of a certain feature $X$ was taken. The values, ordered according to the sequence of observation (in time), are as follows:

$$15.79, 15.84, 16.28, 16.33, 16.38, 16.41, 16.75,$$

$$16.87, 16.98, 17.00, 17.00, 17.35, 17.48, 17.56,$$

$$17.98, 18.12, 18.28, 18.28, 18.32, 18.53.$$

1. Determine the median $m_e$ of this sample.
2. Create a sequence of symbols, writing $a$ if $x_i < m_e$ and $b$ if $x_i > m_e$ (elements equal to the median are omitted).
3. Verify the hypothesis of the randomness of the sample (lack of trend/cyclicity) using the **runs test** at a significance level of $\alpha=0.05$.
*(Data from Task 3.87, Krysicki Part II, p. 143)*.

## Task 2
We have two sorting algorithms (A and B). 5 independent time measurements were performed for each of them. The results do not follow a normal distribution (outliers are present).

* Algorithm A: $12, 18, 14, 15, 13$
* Algorithm B: $19, 21, 23, 20, 22$

Verify the hypothesis that algorithm A is faster than B using the rank-sum test (Mann-Whitney-Wilcoxon).

## Task 3
Data on failures depending on the hardware manufacturer were collected in a table (contingency table):

| Manufacturer \ Failure Type | Overheating | Disk Error | Memory Error |
| :--- | :---: | :---: | :---: |
| **Manufacturer X** | 20 | 10 | 15 |
| **Manufacturer Y** | 30 | 50 | 25 |

Check at the significance level $\alpha=0.05$ whether the type of failure depends on the manufacturer.

## Task 4
We are testing the performance of 3 different frameworks (X, Y, Z). Since the data are strongly asymmetric, instead of classical analysis of variance (ANOVA), we use the non-parametric Kruskal-Wallis test.

**Performance benchmark results (points):**

| Framework X | Framework Y | Framework Z |
| :---: | :---: | :---: |
| 45 | 52 | 68 |
| 48 | 55 | 70 |
| 42 | 58 | 75 |
| 50 | 60 | 72 |
| 46 | 54 | 78 |
*(Sample sizes: $n_x=5, n_y=5, n_z=5$.)*

For the ranking data from the table, verify the hypothesis that all frameworks have the same median performance.

## Task 5
We have two datasets on network traffic (before and after firewall implementation). We want to check if the **entire distribution** (not just the mean) has changed.

**Packet delay measurements (in ms):**

**Before implementation ($n=10$):**

$$12, 15, 18, 14, 13, 16, 12, 19, 15, 17$$

*(Ordered data: 12, 12, 13, 14, 15, 15, 16, 17, 18, 19)*

**After implementation ($m=10$):**

$$18, 22, 20, 19, 21, 25, 23, 20, 24, 28$$

*(Ordered data: 18, 19, 20, 20, 21, 22, 23, 24, 25, 28)*

Based on the empirical distribution functions of both samples, calculate the $D_{n,m}$ statistic and verify the hypothesis of identical distributions (Kolmogorov-Smirnov test).
Verify the hypothesis at significance level ( \alpha = 0.05 ).

## Task 6
We investigate code compilation time ($Y$) depending on the number of files ($X_1$) and the number of lines of code in a file ($X_2$).

**Data from 8 software projects:**

| Project | Number of files ($x_1$) | Thousands of LOC ($x_2$) | Compilation time in sec. ($y$) |
| :---: | :---: | :---: | :---: |
| 1 | 2 | 5 | 12 |
| 2 | 4 | 10 | 25 |
| 3 | 3 | 8 | 19 |
| 4 | 6 | 15 | 40 |
| 5 | 8 | 20 | 55 |
| 6 | 2 | 4 | 10 |
| 7 | 5 | 12 | 32 |
| 8 | 7 | 18 | 48 |

For the given data, determine the equation of the regression plane:

$$
y = a x_1 + b x_2 + c
$$

## Task 7
The number of transistors in processors grows exponentially: $y = a \cdot e^{bx}$. Having historical data, reduce this problem to linear regression by taking logarithms ($\ln y = \ln a + bx$) and determine the growth parameters.

**Historical data of processor development (simplified):**

| Year ($t$) | Time variable $x = t - 1970$ | Transistor count ($y$) |
| :---: | :---: | :---: |
| 1970 | 0 | 2 000 |
| 1975 | 5 | 8 000 |
| 1980 | 10 | 30 000 |
| 1985 | 15 | 120 000 |
| 1990 | 20 | 500 000 |

## Task 8
Processor production generates a certain percentage of defects. Instead of taking a fixed sample of 100 units, we take units one by one. After each extraction, we decide: "good batch", "bad batch", or "continue sampling".

Construct a sequential test (Wald test) to verify the hypothesis $p=0.01$ against $p=0.10$. Assume Type I error risk $\alpha = 0.05$ and Type II error risk $\beta = 0.10$.

## Task 9
For a simple sample $x_1, ..., x_n$ from an exponential distribution (failure-free operation time) with density $f(x) = \frac{1}{\lambda} \exp\left(-\frac{x}{\lambda}\right)$, where $\lambda$ is the expected value, determine the estimator of the parameter $\lambda$ using the maximum likelihood method (MLE).

## Task 10
We have 3 servers. We want to check if they operate equally stably (if they have the same variance of response times) before comparing their average times.
The sample data is as follows:
* Server 1 ($s_1^2 = 1.4$): $n_1 = 20$
* Server 2 ($s_2^2 = 1.8$): $n_2 = 20$
* Server 3 ($s_3^2 = 1.2$): $n_3 = 20$

Verify the hypothesis $H_0: \sigma_1^2 = \sigma_2^2 = \sigma_3^2$ at $\alpha=0.05$ (e.g., using Bartlett's test).
