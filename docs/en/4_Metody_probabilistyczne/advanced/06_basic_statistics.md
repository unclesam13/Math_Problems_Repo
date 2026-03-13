# TASK LIST NO. 6: Basic Statistics and Their Distributions

## Task 1 (Frequency Distribution)
From a general population, a sample of size $n=50$ was drawn (measurement results). The following raw results were obtained:

$$3.6, 5.0, 4.0, 4.7, 5.2, 5.9, 4.5, 5.3, 5.5, 3.9,$$

$$5.6, 3.5, 5.4, 5.2, 4.1, 5.0, 3.1, 5.8, 4.8, 4.4,$$

$$4.6, 5.1, 4.7, 3.0, 5.5, 6.1, 3.8, 4.9, 5.6, 6.1,$$

$$5.9, 4.2, 6.4, 5.3, 4.5, 4.9, 4.0, 5.2, 3.3, 5.4,$$

$$4.7, 6.4, 5.1, 3.4, 5.2, 6.2, 4.4, 4.3, 5.8, 3.7.$$

Based on this data:

1. Construct a **frequency distribution table**, assuming the number of classes $k=7$.
2. Determine the range $R$ and the class width $b$.

## Task 2 (Measures of Location)
For the sample from Task 1, after arranging the results in ascending order determine:

1. The **Median** ($m_e$) – the middle value.
2. The **Mode** ($m_o$) – the most frequent value.
3. Compare whether in this case $m_e \approx \bar{x}$ (where $\bar{x} = 4.844$).


## Task 3
In a certain chemical experiment (or processor production process), the amount of pure substance was investigated. For 5 measurements, the following results were obtained: $3.5, 3.4, 2.1, 5.4, 1.1$.

Calculate:

1. The arithmetic mean of the sample $\bar{x}$.
2. The sample variance $s^2$ (using the formula for a small sample).
3. The standard deviation $s$.

## Task 4
A vehicle (or a data packet in a network) traveled a path consisting of three sections of the same length but with different speeds: $v_1=50, v_2=60, v_3=70$ km/h. Calculate the average speed over the entire route.

*Hint: Use the harmonic mean, not the arithmetic mean.*

## Task 5
Two six-element samples are given (e.g., access times to two different disks):

* Sample I: $80, 40, 40, 80, 40, 80$
* Sample II: $40, 80, 120, 80, 120, 40$

Calculate the coefficients of variation $v = \frac{s}{\bar{x}}$ for both samples. Which disk operates more stably (has a smaller relative dispersion)?

## Task 6
A sample of size 36 was drawn from a population with a normal distribution $N(\mu, \sigma)$. The sample mean was $\bar{x} = 150$, and the population standard deviation is known to be $\sigma = 12$. Construct a two-sided confidence interval for the population mean $\mu$ at a confidence level of 0.95. For this purpose, use the fact that the statistic:

$$
U = \frac{\bar{X} - \mu}{\sigma} \sqrt{n}
$$

follows a standard normal distribution $N(0,1)$.

## Task 7
A small sample (10 elements) was drawn from a population with a normal distribution. Since we do not know the population standard deviation $\sigma$, we must use the sample standard deviation $S$ (calculated using the formula divided by $n$). The statistic:

$$
t = \frac{\bar{X} - \mu}{S} \sqrt{n-1}
$$

follows the Student's t-distribution. Read from the tables the critical values needed to construct a two-sided confidence interval at a confidence level of 0.95.

## Task 8
To investigate the sample variance (dispersion), the following statistic is used:

$$
\chi^2 = \frac{nS^2}{\sigma^2}
$$

> *Note: The symbol $S^2$ denotes the sample variance calculated with the formula dividing by $n$ (according to the definition in Krysicki's textbook).*

15 measurements were taken. Read from the chi-square distribution tables the critical values that cut off symmetrical areas in the tails (5% probability for each tail), between which this statistic will fall with a probability of 0.90.

## Task 9
Given a 3-element population with values {2, 4, 6}. List all possible 2-element samples (sampling with replacement), calculate the mean for each, and then show that the expected value of these sample means equals the mean of the entire population. In this way, you will demonstrate numerically that the sample mean is an unbiased estimator.

## Task 10
For a small sample: $0.18, 0.56, 0.87, 1.37, 2.46$, determine the values of the empirical distribution function $S_n(x)$.