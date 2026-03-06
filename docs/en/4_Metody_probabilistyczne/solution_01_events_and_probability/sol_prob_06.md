# Solution 1 – Task 6

## Given

Production ratio:

$$
3:2
$$

Thus:

$$
P(M_1) = \frac{3}{5}
$$

$$
P(M_2) = \frac{2}{5}
$$

First-quality probabilities:

$$
P(F|M_1) = 0.65
$$

$$
P(F|M_2) = 0.85
$$



## 1. Probability a random product is first-quality

Using the **law of total probability**:

$$
P(F) =
P(M_1)P(F|M_1) +
P(M_2)P(F|M_2)
$$

Substitute values:

$$
P(F) =
\frac{3}{5}\cdot0.65 +
\frac{2}{5}\cdot0.85
$$

$$
P(F) = 0.39 + 0.34 = 0.73
$$



## 2. Probability it came from machine 1

Using **Bayes' theorem**:

$$
P(M_1|F) =
\frac{P(M_1)P(F|M_1)}{P(F)}
$$

Substitute values:

$$
P(M_1|F) =
\frac{\frac{3}{5}\cdot0.65}{0.73}
$$

$$
P(M_1|F) \approx 0.534
$$