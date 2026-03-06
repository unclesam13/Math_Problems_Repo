# Solution 1 – Task 7

## Given

Signals:

$$
P(111)=0.65
$$

$$
P(000)=0.35
$$

Error probability:

$$
P(1\to0)=0.2
$$

$$
P(0\to1)=0.2
$$

Correct transmission:

$$
P(1\to1)=0.8
$$

$$
P(0\to0)=0.8
$$

Symbols are independent.

---

## 1. Probability of receiving 111

Two possible transmissions:

From 111:

$$
0.65 \cdot 0.8^3
$$

From 000:

$$
0.35 \cdot 0.2^3
$$

Thus:

$$
P(111) =
0.65\cdot0.512 +
0.35\cdot0.008
$$

$$
P(111) = 0.3356
$$

---

## 2. Probability of receiving 000

From 000:

$$
0.35\cdot0.8^3
$$

From 111:

$$
0.65\cdot0.2^3
$$

$$
P(000) =
0.35\cdot0.512 +
0.65\cdot0.008
$$

$$
P(000) = 0.1844
$$

---

## 3. Probability of receiving 010

From 111:

$$
0.65\cdot(0.2\cdot0.8\cdot0.2)
$$

From 000:

$$
0.35\cdot(0.8\cdot0.2\cdot0.8)
$$

$$
P(010) = 0.0208 + 0.0448 = 0.0656
$$