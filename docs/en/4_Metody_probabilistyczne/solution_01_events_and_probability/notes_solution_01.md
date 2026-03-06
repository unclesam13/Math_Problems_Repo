# Random Events and Probability – Theory Notes

These notes summarize the **terminology, formulas, and reasoning methods** used in Solution No.1 Tasks.  
The goal is to build a reference that helps **understand and reproduce solutions without technology**.

---

# 1. Basic Terminology of Probability

## Random Experiment
A **random experiment** is an experiment whose outcome cannot be predicted with certainty.

Example:
- tossing a coin
- measuring water flow
- transmission of a signal through a noisy channel


## Sample Space

The **sample space** is the set of all possible elementary outcomes.

It is denoted:

$$
\Omega
$$

Example:

$$
\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}
$$


## Elementary Event

An **elementary event** is a single outcome of the experiment.

Example:

$$
\omega_3
$$



## Random Event

A **random event** is a subset of the sample space.

Example:

$$
A = \{\omega_1,\omega_3,\omega_5\}
$$



# 2. Operations on Events

## Union of Events

The union of two events means **at least one of them occurs**.

Notation:

$$
A \cup B
$$

Definition:

$$
A \cup B =
\{\omega : \omega \in A \; \text{or} \; \omega \in B\}
$$



## Intersection of Events

The intersection means **both events occur simultaneously**.

Notation:

$$
A \cap B
$$

Definition:

$$
A \cap B =
\{\omega : \omega \in A \; \text{and} \; \omega \in B\}
$$



## Difference of Events

Difference means outcomes belonging to one event but not the other.

$$
A \setminus B
$$

Definition:

$$
A \setminus B =
\{\omega : \omega \in A \text{ and } \omega \notin B\}
$$



## Complement of an Event

The complement means the event **does not occur**.

Notation:

$$
A'
$$

Definition:

$$
A' = \Omega \setminus A
$$

Probability formula:

$$
P(A') = 1 - P(A)
$$



# 3. Probability Rules

## Classical Probability

If all outcomes are equally likely:

$$
P(A) = \frac{|A|}{|\Omega|}
$$

where

- $|A|$ = number of favorable outcomes
- $|\Omega|$ = total number of outcomes



## Union Formula

For any two events:

$$
P(A \cup B) =
P(A) + P(B) - P(A \cap B)
$$



## De Morgan's Laws

$$
(A \cup B)' = A' \cap B'
$$

$$
(A \cap B)' = A' \cup B'
$$



# 4. Reliability of Systems

## Series Systems

In a **series connection**, the system works only if **all components work**.

Event representation:

$$
A = A_1 \cap A_2 \cap ... \cap A_n
$$



## Parallel Systems

In a **parallel connection**, the system works if **at least one component works**.

Event representation:

$$
A = A_1 \cup A_2
$$

Probability formula:

$$
P(A_1 \cup A_2) =
P(A_1) + P(A_2) - P(A_1 \cap A_2)
$$



# 5. Law of Total Probability

Used when an event can occur through **several mutually exclusive cases**.

Formula:

$$
P(A) =
\sum_{i=1}^{n} P(B_i)P(A|B_i)
$$

where

- $B_i$ are mutually exclusive events
- $\bigcup B_i = \Omega$



# 6. Bayes' Theorem

Used to **update probabilities after observing evidence**.

Formula:

$$
P(B_i|A) =
\frac{P(B_i)P(A|B_i)}{\sum_{j=1}^{n}P(B_j)P(A|B_j)}
$$

Interpretation:

- prior probability → $P(B_i)$
- likelihood → $P(A|B_i)$
- posterior probability → $P(B_i|A)$



# 7. Independence of Events

Two events are **independent** if:

$$
P(A \cap B) = P(A)P(B)
$$


# 8. Probability in Communication Channels

If symbols are transmitted **independently**, the probability of receiving a sequence equals the product of probabilities for each symbol.

Example:

Receiving $ACAA$:

$$
P =
P(A_1)P(C_2)P(A_3)P(A_4)
$$


&nbsp;


# Possible  Questions



# Task 1 – Events and Set Operations

### Possible Question

**What is the difference between union and intersection?**

**Answer**

Union represents the event that **at least one event occurs**.

$$
A \cup B
$$

Intersection represents the event that **both events occur simultaneously**.

$$
A \cap B
$$



# Task 2 – Reliability of Circuits

### Possible Question

**Why is a parallel connection represented by a union of events?**

**Answer**

Because the system works if **at least one component functions**.

Thus the event that the system works is

$$
A_2 \cup A_3
$$



# Task 3 – Classical Probability

### Possible Question

**When can we use classical probability?**

**Answer**

When all elementary outcomes are **equally likely**.

Formula:

$$
P(A) = \frac{|A|}{|\Omega|}
$$



# Task 4 – Parallel Reliability

### Possible Question

**Why do we subtract $P(A_1 \cap A_2)$ in the union formula?**

**Answer**

Because when adding

$$
P(A_1) + P(A_2)
$$

the intersection is counted **twice**, so it must be subtracted once.



# Task 5 – Complement Events

### Possible Question

**What is the meaning of the complement of an event?**

**Answer**

The complement represents the event that **A does not occur**.

Formula:

$$
P(A') = 1 - P(A)
$$



# Task 6 – Total Probability and Bayes

### Possible Question

**What is the difference between total probability and Bayes' theorem?**

**Answer**

Total probability calculates the probability of an event:

$$
P(A)
$$

Bayes' theorem calculates the probability of the **cause after observing the result**:

$$
P(B|A)
$$



# Task 7 – Signal Transmission

### Possible Question

**Why do we multiply probabilities when calculating signal transmission?**

**Answer**

Because interference affects symbols **independently**, therefore the joint probability equals the product of individual probabilities.



# Task 8 – Random Arrangement

### Possible Question

**Why do probabilities change after the first pulse is chosen?**

**Answer**

Because the experiment becomes **dependent without replacement**, so the sample space changes.

Example:

$$
P(A_1) = \frac{4}{7}
$$

After choosing A:

$$
P(C_2|A_1) = \frac{1}{6}
$$



# Task 9 – Independent Production

### Possible Question

**Why do we multiply probabilities from different plants?**

**Answer**

Because production in different plants is assumed to be **independent events**.

Thus

$$
P = P_1 P_2 P_3
$$



# Task 10 – Communication with Errors

### Possible Question

**Why do we sum probabilities from different transmitted signals?**

**Answer**

Because the received signal may originate from **different transmitted sequences**.

Therefore we use the **law of total probability**.

$$
P(A) =
\sum P(\text{signal})P(\text{received}|\text{signal})
$$

&nbsp;

# Key Ideas to Remember

1. Events behave like **sets**.
2. Reliability problems use **union and intersection**.
3. Communication problems use **independence of symbols**.
4. Multiple possible causes require the **law of total probability**.
5. Inverse reasoning requires **Bayes' theorem**.