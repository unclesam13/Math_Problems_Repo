# Solution 1 — Events and Probability

## Task 5 - Buffon's Needle Experiment

### Setup — Sample Space

From Task 5, a needle of length $L \leq d$ is thrown onto a plane with parallel lines spaced $d$ apart.

Each throw is described by two parameters:

- $x \in \left[0, \tfrac{d}{2}\right]$ — distance from needle's **center** to the nearest line
- $\theta \in \left[0, \tfrac{\pi}{2}\right]$ — **angle** between needle and the lines

The sample space is the rectangle:

$$\Omega = \left[0, \frac{d}{2}\right] \times \left[0, \frac{\pi}{2}\right]$$

with area:

$$|\Omega| = \frac{d}{2} \cdot \frac{\pi}{2} = \frac{\pi d}{4}$$

Both $x$ and $\theta$ are **independent** and **uniformly distributed**, so probabilities are computed as:

$$P(A) = \frac{\text{area of region } A}{\text{area of } \Omega} = \frac{\text{area of } A}{\pi d / 4}$$

---

## When Does the Needle Cross a Line?

The needle crosses a line if and only if the perpendicular projection of the half-needle onto the direction normal to the lines reaches a line. The needle crosses when:

$$x \leq \frac{L}{2}\sin\theta$$

This is the fundamental geometric condition for all events below.

---

## Event $A$ — Needle Intersects a Line

The favorable region is:

$$A = \left\{(x, \theta) \in \Omega : x \leq \frac{L}{2}\sin\theta\right\}$$

Computing the area by integration:

$$\text{area}(A) = \int_0^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{L}{2}\Big[-\cos\theta\Big]_0^{\pi/2} = \frac{L}{2}(0-(-1)) = \frac{L}{2}$$

Therefore:

$$\boxed{P(A) = \frac{L/2}{\pi d/4} = \frac{2L}{\pi d}}$$

> **Historical note:** This is the famous **Buffon's formula**. It was used historically to estimate $\pi$ experimentally — by throwing needles and observing:
> $$\pi \approx \frac{2L \cdot N}{d \cdot n_{\text{cross}}}$$
> where $N$ is total throws and $n_{\text{cross}}$ is the number of crossings.

---

## Event $B$ — Needle Does Not Intersect Any Line

This is simply the complement of $A$:

$$B = A^c = \left\{(x,\theta) \in \Omega : x > \frac{L}{2}\sin\theta\right\}$$

$$\boxed{P(B) = 1 - P(A) = 1 - \frac{2L}{\pi d}}$$

For example, with $L = d$ (needle length equals line spacing):

$$P(B) = 1 - \frac{2}{\pi} \approx 36.34\%$$

---

## Event $C$ — Angle Smaller Than $\tfrac{\pi}{6}$

The angle condition is independent of position, so we only need the fraction of $\theta$ values in $\left[0, \tfrac{\pi}{6}\right]$:

$$C = \left\{(x,\theta) \in \Omega : \theta < \frac{\pi}{6}\right\}$$

$$\text{area}(C) = \frac{d}{2} \cdot \frac{\pi}{6}$$

$$
\boxed{P(C) = \frac{d/2 \cdot \pi/6}{\pi d/4} = \frac{\pi d/12}{\pi d/4} = \frac{1}{3} \approx 33.33\%}
$$

This makes sense — $\theta$ is uniform on $\left[0, \tfrac{\pi}{2}\right]$, so $P\!\left(\theta < \tfrac{\pi}{6}\right) = \tfrac{\pi/6}{\pi/2} = \tfrac{1}{3}$.

---

## Event $D$ — Center Closer Than $\tfrac{d}{4}$ to Nearest Line

The position condition is independent of angle:

$$D = \left\{(x,\theta) \in \Omega : x < \frac{d}{4}\right\}$$

$$\text{area}(D) = \frac{d}{4} \cdot \frac{\pi}{2}$$

$$\boxed{P(D) = \frac{d/4 \cdot \pi/2}{\pi d/4} = \frac{\pi d/8}{\pi d/4} = \frac{1}{2}}$$

Again intuitive — $x$ is uniform on $\left[0, \tfrac{d}{2}\right]$, so the probability of being in the lower half $\left[0, \tfrac{d}{4}\right]$ is exactly $\tfrac{1}{2}$.

---

## Event $E$ — Needle Crosses a Line AND Angle Greater Than $\tfrac{\pi}{4}$

This is an intersection of two conditions:

$$E = \left\{(x,\theta) \in \Omega : x \leq \frac{L}{2}\sin\theta \text{ and } \theta > \frac{\pi}{4}\right\}$$

Computing the area:

$$\text{area}(E) = \int_{\pi/4}^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{L}{2}\Big[-\cos\theta\Big]_{\pi/4}^{\pi/2}$$

$$= \frac{L}{2}\left(-\cos\frac{\pi}{2} + \cos\frac{\pi}{4}\right) = \frac{L}{2}\left(0 + \frac{\sqrt{2}}{2}\right) = \frac{L\sqrt{2}}{4}$$

$$\boxed{P(E) = \frac{L\sqrt{2}/4}{\pi d/4} = \frac{L\sqrt{2}}{\pi d}}$$

Note that $P(E) = P(A) \cdot P(\theta > \tfrac{\pi}{4} \mid \text{crosses})$, but since crossing and angle are **not independent**, we must integrate directly as above.

---

## Additional Event

**Event $F$** — needle crosses a line AND the center is within $\tfrac{d}{4}$ of the nearest line:

$$F = \left\{(x,\theta) \in \Omega : x \leq \frac{L}{2}\sin\theta \text{ and } x < \frac{d}{4}\right\}$$

Since $L \leq d$, we have $\tfrac{L}{2}\sin\theta \leq \tfrac{L}{2} \leq \tfrac{d}{2}$, so the crossing condition $x \leq \tfrac{L}{2}\sin\theta$ already implies $x \leq \tfrac{d}{4}$ whenever $\sin\theta \leq \tfrac{d}{2L}$.

We split into two cases:

**Case 1:** $\tfrac{L}{2}\sin\theta \leq \tfrac{d}{4}$, i.e. $\sin\theta \leq \tfrac{d}{2L}$ — the crossing region lies entirely within $x < \tfrac{d}{4}$, so both conditions reduce to just the crossing condition.

**Case 2:** $\tfrac{L}{2}\sin\theta > \tfrac{d}{4}$ — the crossing region extends beyond $\tfrac{d}{4}$, so the binding constraint is $x < \tfrac{d}{4}$.

For the special case $L = d$:

$$\text{area}(F) = \int_0^{\pi/6} \frac{L}{2}\sin\theta\,d\theta + \int_{\pi/6}^{\pi/2} \frac{d}{4}\,d\theta$$

$$= \frac{L}{2}\Big[-\cos\theta\Big]_0^{\pi/6} + \frac{d}{4}\cdot\frac{\pi}{3}$$

$$= \frac{d}{2}\left(1 - \frac{\sqrt{3}}{2}\right) + \frac{\pi d}{12} = \frac{d(2-\sqrt{3})}{4} + \frac{\pi d}{12}$$

$$P(F) = \frac{\text{area}(F)}{\pi d/4} = \frac{2-\sqrt{3}}{\pi} + \frac{1}{3} \approx \frac{0.268}{\pi} + 0.333 \approx 0.419$$

---

## Summary Table

| Event | Description | Probability |
|---|---|---|
| $A$ | Needle crosses a line | $\dfrac{2L}{\pi d}$ |
| $B$ | Needle does not cross | $1 - \dfrac{2L}{\pi d}$ |
| $C$ | Angle $< \tfrac{\pi}{6}$ | $\dfrac{1}{3}$ |
| $D$ | Center within $\tfrac{d}{4}$ of line | $\dfrac{1}{2}$ |
| $E$ | Crosses AND angle $> \tfrac{\pi}{4}$ | $\dfrac{L\sqrt{2}}{\pi d}$ |
| $F$ | Crosses AND center within $\tfrac{d}{4}$ (case $L=d$) | $\dfrac{2-\sqrt{3}}{\pi} + \dfrac{1}{3}$ |

---

## Key Techniques Used

- **Geometric probability**: $P(A) = \dfrac{\text{area}(A)}{\text{area}(\Omega)}$ since $(x,\theta)$ is uniformly distributed over $\Omega$
- **Integration**: the crossing boundary $x = \tfrac{L}{2}\sin\theta$ is a curve, so areas require integration
- **Independence of $x$ and $\theta$**: when an event depends only on $x$ or only on $\theta$, the probability reduces to a simple ratio of interval lengths (Events $C$ and $D$)
- **Complement rule**: Event $B$ is trivially obtained from $A$
- **Intersection of dependent events**: Event $E$ cannot be factored as $P(\text{cross}) \cdot P(\theta > \pi/4)$ — the crossing depends on $\theta$, so direct integration is required