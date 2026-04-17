# Problem 3 — Weather (7 days × 3 states)

# 1. Conceptual Foundations

## 1.1 Description of the Experiment

We consider a **random experiment** describing the weather during a week.

Each day can take one of three possible states:

$$
S = \text{sunny}, \quad C = \text{cloudy}, \quad R = \text{rainy}
$$

There are 7 days:

$$
\{Mon, Tue, Wed, Thu, Fri, Sat, Sun\}
$$

<iframe src="https://unclesam13.github.io/Math_Problems_Repo/anim/4_Metody_probalistyczne/weather_task4.html" width="100%" height="520" frameborder="0" style="border-radius:4px;"></iframe>

## 1.2 Sample Space

An **elementary outcome** is a full assignment of weather states to all days:

$$
\omega = (w_{Mon}, w_{Tue}, w_{Wed}, w_{Thu}, w_{Fri}, w_{Sat}, w_{Sun})
$$

where:

$$
w_d \in \{S, C, R\}
$$

Thus the sample space is:

$$
\Omega = \{S, C, R\}^7
$$



## 1.3 Meaning of the Table Representation

The table is **not a list of outcomes**.

Instead, it is a **graphical representation of an event**, i.e., a subset of $\Omega$.

- Columns represent **days**
- Rows represent **weather states**
- Marking a cell ($X$) means that this state is **allowed or selected** for that day

Thus, the table defines a **set of all sequences consistent with the marked constraints**.

<br></br>

# 2. Part A — Constructing Events



## 2.1 Event: Monday is sunny

### Formal description

$$
A = \{\omega \in \Omega : w_{Mon} = S\}
$$

### Interpretation

Only Monday is fixed; all other days are arbitrary.

### Graphical representation


|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   | X   |     |     |     |     |     |     |
| C   |     |     |     |     |     |     |     |
| R   |     |     |     |     |     |     |     |



## 2.2 Event: Weekend (Saturday and Sunday) is rainy

### Formal description

$$
A = \{\omega \in \Omega : w_{Sat} = R \;\text{and}\; w_{Sun} = R\}
$$

### Interpretation

Both days must be rainy simultaneously (logical AND).

### Graphical representation

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   |     |     |     |     |     |     |     |
| C   |     |     |     |     |     |     |     |
| R   |     |     |     |     |     | X   | X   |



## 2.3 Event: It rains on Wednesday or Friday

### Formal description

$$
A = \{\omega \in \Omega : w_{Wed} = R \;\lor\; w_{Fri} = R\}
$$

### Interpretation

This is a **logical OR**:
- at least one of the days is rainy
- possibly both

### Graphical representation

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   |     |     |     |     |     |     |     |
| C   |     |     |     |     |     |     |     |
| R   |     |     | X   |     | X   |     |     |


## 2.4 Event: There is no rainy day during the week

### Formal description

$$
A = \{\omega \in \Omega : \forall d,\; w_d \neq R\}
$$

Equivalently:

$$
w_d \in \{S, C\} \quad \text{for all } d
$$

### Interpretation

Rain is completely excluded.

### Graphical representation

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   | X   | X   | X   | X   | X   | X   | X   |
| C   | X   | X   | X   | X   | X   | X   | X   |
| R   |     |     |     |     |     |     |     |


## 2.5 Event: Thursday is not sunny

### Formal description

$$
A = \{\omega \in \Omega : w_{Thu} \neq S\}
$$

### Interpretation

Allowed states: $C$ or $R$

### Graphical representation

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   |     |     |     |     |     |     |     |
| C   |     |     |     | X   |     |     |     |
| R   |     |     |     | X   |     |     |     |

<br></br>


# 3. Part B — Interpreting Events

## 3.1 Case 1

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   |     |     |     |     |     | X   | X   |
| C   |     |     |     |     |     |     |     |
| R   |     |     |     |     |     |     |     |



### Step 1 — Observation

- Only row $S$ is marked
- Only for Saturday and Sunday

---

### Step 2 — Formal description

$$
A = \{\omega \in \Omega : w_{Sat} = S \;\text{and}\; w_{Sun} = S\}
$$

---

### Step 3 — Interpretation

> The weekend is sunny.

All other days are unrestricted.



## 3.2 Case 2

|     | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|-----|-----|-----|-----|-----|-----|-----|-----|
| S   | X   | X   | X   | X   | X   | X   | X   |
| C   | X   | X   | X   | X   | X   | X   | X   |
| R   |     |     |     |     |     |     |     |



---

### Step 1 — Observation

- $S$ and $C$ allowed for all days
- $R$ excluded everywhere

---

### Step 2 — Formal description

$$
A = \{\omega \in \Omega : \forall d,\; w_d \in \{S, C\}\}
$$

---

### Step 3 — Interpretation

> There are no rainy days during the week.

<br></br>

# 4. Conceptual Discussion

This problem highlights a key transition in probability theory:



## 4.1 Events as Sets

An event is not merely a verbal description, but a **subset of the sample space**:

$$
A \subseteq \Omega
$$


## 4.2 Logical Statements vs Set Structure

Statements such as:

- “Monday is sunny”
- “It rains on Wednesday or Friday”

correspond to:

- restrictions on coordinates
- logical operations (AND, OR, NOT)


## 4.3 Graphical Representation

The table allows us to:

- visualize allowed configurations
- see structure instead of listing outcomes
- understand constraints geometrically


## 4.4 From Intuition to Formalism

We move through three levels:

1. Verbal description  
2. Graphical structure  
3. Formal mathematical definition  

This transition is essential for understanding probability as a **mathematical theory**, not just a computational tool.

<br></br>

# 5. Final Insight

The main idea of this problem is:

> An event can be described equivalently as:
> - a condition,
> - a graphical constraint,
> - a subset of the sample space.

Understanding these connections is fundamental for further study of probability.

