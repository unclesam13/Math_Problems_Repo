# TASK LIST NO. 7: Point and Interval Estimation

## Task 1
Find the confidence interval for the unknown mean value $\mu$ of a population, in the case where $\sigma$ is known, based on an $n$-element simple sample $X_1, ..., X_n$.

Data: From a population with a standard deviation $\sigma=0.14$, a sample of $n=100$ elements was taken (e.g., voltage measurements on a processor). The sample mean was $\bar{x}=2.5$. Determine the 95% confidence interval for the mean (assume $1-\alpha = 0.95$, which gives $u_{\alpha} = 1.96$).

## Task 2
The durability of 10 randomly selected structural elements was measured (or e.g., battery life of 10 laptops). The following results were obtained: $383, 284, 339, 340, 305, 386, 378, 335, 344, 346$.

Assuming that the distribution of the feature is normal, determine the 95% confidence interval for the mean durability.

*Hint: Since $n=10$ is small ($n<30$) and we do not know $\sigma$, calculate $s$ from the sample and use the Student's t-distribution*.

## Task 3
To determine the electron charge, 26 measurements were made using the Millikan method. A mean of $\bar{x} = 1.574 \cdot 10^{-19}$ and a standard deviation of $s = 0.043 \cdot 10^{-19}$ were obtained.

Determine the confidence interval for the mean charge at a confidence level of $0.99$.

## Task 4
A 300-element sample was taken from a population of cotton fibers and their lengths were measured. The mean $\bar{x}=27.43$ mm and variance $s^2=51.598$ were calculated.

Find the 95% realization of the confidence interval for the unknown average fiber length.

*Hint: With such a large $n$ ($n=300$), the Student's t-distribution is practically identical to the normal distribution, so the statistic $u_{\alpha}$ can be used*.

## Task 5
Measurements of sea depth (or e.g., network latency) are made in a certain specific location.

How many independent measurements must be made to assume with a confidence level of $0.95$ that the absolute error of estimating the mean will not exceed $10$ m, if the error distribution is normal with a variance of $\sigma^2 = 180$ $m^2$? 

## Task 6
Among 120 randomly selected employees of a certain plant, 17 did not meet the work performance standard (in IT: 17 out of 120 servers did not meet SLA requirements).

Determine the 95% realization of the confidence interval for the fraction $p$ of employees not meeting the standard in the entire plant.

## Task 7
15 measurements were made of the time to repair yarn breaks on looms. The sample variance was calculated as $s^2 = 134.2$. Assuming that this time has a normal distribution, determine the 90% confidence interval for the variance $\sigma^2$ and the standard deviation $\sigma$. The sample variance ( s^2 ) is calculated using division by ( n-1 ).

*Hint: Use the chi-square ($\chi^2$) distribution tables*.

## Task 8
Two samples were drawn for a certain feature with a normal distribution:

* Sample 1: $n=25$, mean $\bar{x}=15$, deviation $s=5$.
* Sample 2: $n=100$, mean $\bar{x}=15$, deviation $s=5$.

Calculate the lengths of the 95% confidence intervals for both samples. How does a fourfold increase in sample size affect precision (interval width)? 

## Task 9
A simple sample of size $n=5$ is given: $\{2, 4, 6, 8, 10\}$. Calculate the value of the unbiased estimator of the expected value ($\bar{x}$) and the unbiased estimator of the variance ($s^2$).

Explain why we divide by $n-1$ instead of $n$ for variance.

## Task 10
The percentage starch content was examined in 80 potatoes. The sample mean was $\bar{x}=17.525\%$, and the standard deviation was $s=1.84\%$.

Assuming a confidence level of 0.95, estimate the average starch content in the entire batch.
