# TASK LIST NO. 5: Limit Theorems and Approximations

## Task 1
**Poisson Theorem – rare events**
The defect rate of a certain electronic component is $p=0.002$. A batch of goods contains $n=1000$ such components. Calculate the probability that in this batch:
1. there will not be a single defective item,
2. there will be at most 3 defective items.

*Hint: Since $n$ is large ($n \ge 100$), $p$ is small ($p \le 0.1$), and $np \le 10$, the Poisson approximation with parameter $\lambda = np$ should be used.*

## Task 2
**De Moivre-Laplace Theorem (Integral) – coin tossing**
We toss a symmetric (fair) coin $n=100$ times. Calculate the probability that the number of obtained heads will fall within the interval $\langle 45, 55 \rangle$.

*Goal: Application of the normal approximation to the binomial distribution for a large number of trials.*

## Task 3
**Sample size selection (Inverse CLT)**
The probability of a boy being born is $p=0.515$. How many times must the experiment (birth) be repeated to assert with a probability of at least $0.95$ that the frequency of boys in the sample differs from the probability $p$ by less than $0.01$?

*Hint: Use the inequality $P(|\frac{k}{n} - p| < \varepsilon) \ge 1 - \alpha$ using the normal cumulative distribution function.*

## Task 4
**Central Limit Theorem – sum of rounding errors**
We add together $n=100$ numbers, each of which has been rounded to the nearest integer. The rounding errors are independent random variables uniformly distributed on the interval $(-0.5; 0.5)$. Calculate the probability that the error of the sum of these numbers (in absolute value) does not exceed $3$.

*Comment: This is a classic example of summing variables with a non-normal distribution (here: uniform), which result in a normal distribution.*

## Task 5
**Central Limit Theorem – elevator load**
A freight elevator can carry a load of up to $2000$ kg. $25$ people enter the elevator. The weight of a random passenger is a random variable with an expected value of $75$ kg and a standard deviation of $10$ kg. Calculate the probability that the total weight of the passengers does not exceed the elevator's permissible load.

## Task 6
**Operating time approximation – exponential distribution**
A laptop battery has an operating time that is a random variable with an exponential distribution with a mean of $4$ hours. A user plans a long fieldwork session and takes $36$ charged batteries with them (replacing them immediately after depletion). What is the probability that the total operating time on this set of batteries will exceed $150$ hours?

## Task 7
**Local De Moivre-Laplace Theorem**
Event $A$ occurs in a single experiment with a probability $p=0.6$. We repeat the experiment $n=600$ times. Calculate the probability that event $A$ occurs exactly $370$ times.

*Hint: For large $n$, the point probability $P(X=k)$ is approximated by the value of the normal distribution density function.*

## Task 8
**Comparison of approximations**
The probability of success in a single trial is $p=0.1$. We perform $n=30$ trials. Calculate the probability of obtaining exactly 2 successes using:
1. the exact Bernoulli formula,
2. the Poisson approximation,
3. the local De Moivre-Laplace theorem.
Compare the results.

## Task 9
**Chebyshev's Inequality**
A random variable $X$ has an expected value $E(X)=10$ and a variance $D^2(X)=4$. Without knowing the exact distribution of this variable, estimate (provide a lower bound for) the probability that the variable $X$ takes a value from the interval $(4, 16)$.

## Task 10
**Statistical application – sample mean**
A random sample of size $n=100$ was taken from a population in which feature $X$ has a distribution (not necessarily normal) with a mean $\mu=100$ and a variance $\sigma^2=25$. Calculate the probability that the arithmetic mean of this sample $\bar{X}$ will be less than $99$.