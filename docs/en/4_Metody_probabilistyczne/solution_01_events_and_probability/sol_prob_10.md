# Solution 1 - Task 10

## Given

Signals:

$$
P(AAAA)=0.4
$$

$$
P(BBBB)=0.3
$$

$$
P(CCCC)=0.3
$$

Correct transmission:

$$
P(A\to A)=0.8
$$

$$
P(B\to B)=0.8
$$

$$
P(C\to C)=0.8
$$

Error probability:

$$
0.1
$$

Letters are transmitted independently.



## 1. Probability of receiving AAAA

Possible transmissions:

From AAAA:

$$
0.4 \cdot 0.8^4
$$

From BBBB:

$$
0.3 \cdot 0.1^4
$$

From CCCC:

$$
0.3 \cdot 0.1^4
$$

Thus:

$$
P(AAAA) =
0.4\cdot0.4096 +
0.3\cdot0.0001 +
0.3\cdot0.0001
$$

$$
P(AAAA) \approx 0.1639
$$



## 2. Probability of receiving the signal $ACAA$


### Step 1: Probability of receiving $ACAA$ if $AAAA$ was transmitted

We analyze each position separately.

Desired received signal:

$$
A \; C \; A \; A
$$

If $AAAA$ was transmitted:

| Position | Transmitted | Received | Probability |
|--------|--------|--------|--------|
|1|A|A|0.8|
|2|A|C|0.1|
|3|A|A|0.8|
|4|A|A|0.8|

Thus

$$
P(ACAA \mid AAAA)
=
0.8 \cdot 0.1 \cdot 0.8 \cdot 0.8
$$

$$
P(ACAA \mid AAAA) = 0.0512
$$

Now multiply by the probability that $AAAA$ was transmitted:

$$
0.4 \cdot 0.0512 = 0.02048
$$

---

### Step 2: Probability of receiving $ACAA$ if $BBBB$ was transmitted

Again analyze position by position.

| Position | Transmitted | Received | Probability |
|--------|--------|--------|--------|
|1|B|A|0.1|
|2|B|C|0.1|
|3|B|A|0.1|
|4|B|A|0.1|

Thus

$$
P(ACAA \mid BBBB)
=
0.1 \cdot 0.1 \cdot 0.1 \cdot 0.1
$$

$$
P(ACAA \mid BBBB) = 0.0001
$$

Multiply by transmission probability:

$$
0.3 \cdot 0.0001 = 0.00003
$$

---

### Step 3: Probability of receiving $ACAA$ if $CCCC$ was transmitted

| Position | Transmitted | Received | Probability |
|--------|--------|--------|--------|
|1|C|A|0.1|
|2|C|C|0.8|
|3|C|A|0.1|
|4|C|A|0.1|

Thus

$$
P(ACAA \mid CCCC)
=
0.1 \cdot 0.8 \cdot 0.1 \cdot 0.1
$$

$$
P(ACAA \mid CCCC) = 0.0008
$$

Multiply by transmission probability:

$$
0.3 \cdot 0.0008 = 0.00024
$$

---

### Step 4: Total probability of receiving $ACAA$

Using the **law of total probability**:

$$
P(ACAA)
=
P(AAAA)P(ACAA|AAAA)
+
P(BBBB)P(ACAA|BBBB)
+
P(CCCC)P(ACAA|CCCC)
$$

Substituting the values:

$$
P(ACAA)
=
0.02048
+
0.00003
+
0.00024
$$

$$
P(ACAA) = 0.02075
$$

---

## Final Result

$$
P(ACAA) \approx 0.02075
$$

---

## Interpretation

The largest contribution comes from the case when **AAAA was transmitted**, because:

- the signal $AAAA$ has the highest prior probability,
- only **one error** is required to obtain $ACAA$.

Signals $BBBB$ and $CCCC$ contribute very little because they require **multiple simultaneous errors**.