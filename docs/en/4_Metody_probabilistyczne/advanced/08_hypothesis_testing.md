# TASK LIST NO. 8: Verification of Statistical Hypotheses

## Task 1
To determine whether the current standard for the service life of certain electronic components, which is 150 days, is not too high, 65 components working under normal conditions were randomly examined. The average service life obtained was $\bar{x} = 139$ days, and the standard deviation was $s = 9.8$ days.

At the significance level $\alpha=0.01$, verify the hypothesis that the standard is overstated (Hypothesis $H_0: m = 150$ versus $H_1: m < 150$).

## Task 2
We compare two algorithms or two devices (e.g., scales). For the first series of $n_1=10$ measurements, a mean of $\bar{x}_1 = 5.25$ and a variance of $s_1^2 = 0.06$ were obtained. For the second series of $n_2=5$ measurements, $\bar{x}_2 = 5.58$ and a variance of $s_2^2 = 0.07$ were obtained.

Assuming that the variances are equal (though unknown), verify at the level $\alpha=0.05$ the hypothesis that both series come from a population with the same mean ($H_0: m_1 = m_2$).

## Task 3
The scatter of delays (jitter) in a network was investigated. 50 shots (measurements) were fired at a target. It turned out that the variance of these distances is equal to $s^2 = 107.3$.

Assuming that the distribution of distances is normal, verify at the level $\alpha=0.05$ the hypothesis that the variance $\sigma^2 = 100$, against the alternative hypothesis $\sigma^2 > 100$.

## Task 4
In a certain enterprise (e.g., a server room), two methods of handling orders were developed. To check if both methods yield equally stable results (equal variances), measurements were taken.

* Method 1: $n_1=5$, variance $s_1^2 = 0.248$.
* Method 2: $n_2=5$, variance $s_2^2 = 2.172$.

At the level $\alpha=0.05$, verify the hypothesis $H_0: \sigma_1^2 = \sigma_2^2$.

## Task 5
The defectiveness of the production of certain products (e.g., erroneous data packets) was 10%. A new technology was introduced. A sample of $n=900$ items was drawn, and 50 defective items were found in it.

Can it be claimed at the significance level $\alpha=0.05$ that the new technology has reduced defectiveness?

## Task 6
The number of yeast cells in 400 squares was observed under a microscope (in computer science: the number of requests to a server per unit of time). The results were grouped in the following table:

| Number of cells ($x_i$) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Number of squares ($n_i$) | 20 | 43 | 53 | 86 | 70 | 54 | 37 | 21 | 10 | 4 | 2 |

At the level $\alpha=0.05$, verify the hypothesis that the distribution of the number of cells is a Poisson distribution.

## Task 7
The results of a 5-element sample are: $0.18; 0.56; 0.87; 1.37; 2.46$.

At the significance level $\alpha=0.05$, verify the hypothesis that this sample comes from a population with an exponential distribution $f(x) = e^{-x}$ for $x>0$.

## Task 8
A sample of $n=20$ of a certain feature (e.g., application response time) was taken. The values were ordered in ascending order:

$$121.3, 124.1, 128.8, 134.8, 136.4, 141.6, 143.0, 143.0, 143.0, 146.5,$$

$$146.5, 147.9, 153.6, 154.7, 157.5, 158.1, 159.7, 161.5, 172.8, 173.7$$

Verify the hypothesis of normality of the distribution at the level $\alpha=0.10$, using the Shapiro-Wilk test.

## Task 9
The execution times of a certain task were measured. The results were ordered in the sequence they were obtained (over time). The full sequence of residuals for $n=20$ measurements is as follows:

$$
+, +, -, -, +, +, +, -, -, -, -, +, +, -, -, +, +, -, +, -
$$

Parameters for verification:

* Number of positives ($n_1$): 10
* Number of negatives ($n_2$): 10
* Number of runs ($k$): 10

Verify the hypothesis of randomness at level $\alpha=0.05$.

## Task 10
For 7 pairs of measurements (e.g., performance before and after a driver update), it was noted whether the result improved (+) or worsened (-). The sequence obtained was:
$+, -, +, +, +, +, -$.

Verify the hypothesis that the update has no effect on performance (probability of improvement $p=0.5$).