# TASK LIST NO. 11: Introduction to Statistical Decision Theory

## Task 1
We consider a batch of goods (e.g., processors) in which we examine defectiveness. We test the hypothesis $H_0: p = 0.02$ (good batch) against $H_1: p = 0.10$ (defective batch). A test was constructed that rejects the batch if the number of defective items in a sample of size $n=50$ exceeds $k=3$.

Calculate:

1. The probability of a Type I error $\alpha$ (rejecting a good batch – producer's risk).
2. The probability of a Type II error $\beta$ (accepting a bad batch – consumer's risk).

## Task 2
For the test from Task 1, determine the power of the test ($1-\beta$) for several alternative values of parameter $p$. Prepare a graph of the test power curve (power function). What does this graph tell us about the "sensitivity" of the decision algorithm to deviations from the norm?

## Task 3
For a mean test $H_0: \mu = 100$ with known $\sigma=5$ and $n=25$:

1. Determine the formula for the operating characteristic (OC) function: $L(\mu) = P(\text{acceptance of } H_0 | \mu)$.
2. How will changing the sample size to $n=100$ affect the steepness of this curve (discriminatory ability)?
Consider a one-sided test at significance level ( \alpha = 0.05 ).

## Task 4

We want to construct a **one-sided test for the population mean** assuming a normal distribution with **known standard deviation** $\sigma = 5$.

We test the hypotheses:

$$
H_0: \mu = \mu_0
\quad \text{against} \quad
H_1: \mu = \mu_0 + 2.
$$

The safety requirements are:

- The probability of a Type I error (rejecting the norm when it is true) must be  $\alpha = 0.01$.
- The probability of a Type II error (accepting the norm when the true mean is shifted by 2 units) must not exceed  $\beta = 0.05$.

Assuming the test is based on the statistic

$$
Z = \frac{\bar{X} - \mu_0}{\sigma/\sqrt{n}},
$$

determine the **minimum sample size $n$** that satisfies the above conditions.


## Task 5
The defectiveness of the production of certain products has been 10% ($p_0=0.1$) so far. A new technology is expected to reduce defectiveness to 5% ($p_1=0.05$). Instead of taking a fixed sample, we take items one by one.

Construct a sequential probability ratio test (Wald test), setting risks $\alpha=0.05$ and $\beta=0.10$.

1. Determine the decision lines (acceptance region, rejection region, and continuation region).
2. Present the procedure in the form of an algorithm (pseudocode).

## Task 6
For the test from Task 5, suppose the following were drawn sequentially:
Good, Good, Bad, Good, Good, Good, Good...

Mark these points on the sequential test chart. In which step (if any) will the algorithm make the decision "The new technology is better"?

## Task 7
One of the advantages of sequential methods is that they require less data on average than classical tests. For the test from Task 5, calculate the expected number of steps (samples) needed to make a decision (ASN), assuming that hypothesis $H_0$ is true.

$$
E(n) \approx \frac{\alpha\ln A + (1-\alpha) \ln B}{E(z)}
$$

where $A, B$ are decision thresholds.
Here ( z ) denotes the log-likelihood ratio for a single observation.

## Task 8
An automated machine produces parts with a nominal diameter $\mu_0$. We suspect that the machine has become decalibrated and the mean has increased to $\mu_1$. The deviation $\sigma$ is known.

Construct a sequential test verifying $H_0: \mu = \mu_0$ against $H_1: \mu = \mu_1$. Write the "stop" condition for this algorithm.
Assume error probabilities ( \alpha = 0.05 ) and ( \beta = 0.10 ).

## Task 9
We have two possible decisions $d_1$ (system deployment) and $d_2$ (no deployment) and two states of nature $\theta_1$ (system works correctly) and $\theta_2$ (system has errors). The loss (cost) matrix is as follows:

* If $d_1$ and $\theta_1$: Cost = 0
* If $d_1$ and $\theta_2$: Cost = 1000 (failure at client's site)
* If $d_2$ and $\theta_1$: Cost = 100 (lost profit)
* If $d_2$ and $\theta_2$: Cost = 0

What decision should be made using the **Minimax** criterion (minimizing the maximum loss)?

## Task 10
For the situation from Task 9, assume that we know from previous tests that the probability of errors occurring is $P(\theta_2) = 0.05$. Calculate the expected loss (Bayes risk) for both decisions. Which decision is optimal in the Bayesian sense?
