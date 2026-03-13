# Solution 10 — Events and Probability

## Task 10 - Events and Probabilities in Buffon's Needle Experiment

### Setup — Sample Space and Probability Model

From Task 5, with needle length $L \leq d$ (distance between lines):

$$\Omega = \left[0, \frac{d}{2}\right] \times \left[0, \frac{\pi}{2}\right]$$

- $x \in \left[0, \tfrac{d}{2}\right]$ — distance from needle's center to nearest line
- $\theta \in \left[0, \tfrac{\pi}{2}\right]$ — angle between needle and the lines

Both variables are **independent** and **uniformly distributed**. Area of $\Omega$:

$$|\Omega| = \frac{d}{2} \cdot \frac{\pi}{2} = \frac{\pi d}{4}$$

Probabilities are computed as:

$$P(A) = \frac{\text{area of region } A}{\pi d / 4}$$

**Crossing condition:** The needle crosses a line if and only if:

$$x \leq \frac{L}{2}\sin\theta$$

This is the boundary curve separating crossing from non-crossing outcomes in $\Omega$.

---

## Event $A$ — Needle Intersects a Line

The favorable region:

$$A = \left\{(x,\theta) : 0 \leq x \leq \frac{L}{2}\sin\theta,\ \theta \in \left[0,\frac{\pi}{2}\right]\right\}$$

Its area is computed by integrating the crossing boundary over all angles:

$$\text{area}(A) = \int_0^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{L}{2} \Big[-\cos\theta\Big]_0^{\pi/2} = \frac{L}{2}(1 - 0) = \frac{L}{2}$$

$$\boxed{P(A) = \frac{L/2}{\pi d/4} = \frac{2L}{\pi d}}$$

For $L = d$: $P(A) = \tfrac{2}{\pi} \approx 63.66\%$

> **The $\pi$ estimation method (Buffon, 1777):** Rearranging gives $\pi = \tfrac{2L \cdot N}{d \cdot n_{\text{cross}}}$ where $N$ is total throws and $n_{\text{cross}}$ is crossings. Throwing thousands of needles physically (or via Monte Carlo simulation) estimates $\pi$.

---

## Event $B$ — Needle Does Not Intersect Any Line

The complement of $A$:

$$P(B) = 1 - P(A) = 1 - \frac{2L}{\pi d}$$

| $L/d$ ratio | $P(A)$ (crosses) | $P(B)$ (no cross) |
|---|---|---|
| $0.25$ | $\approx 15.92\%$ | $\approx 84.08\%$ |
| $0.50$ | $\approx 31.83\%$ | $\approx 68.17\%$ |
| $0.75$ | $\approx 47.75\%$ | $\approx 52.25\%$ |
| $1.00$ | $\approx 63.66\%$ | $\approx 36.34\%$ |

As the needle gets longer relative to the spacing, crossings become more likely — as expected.

---

## Event $C$ — Angle Smaller Than $\tfrac{\pi}{6}$

The condition $\theta < \tfrac{\pi}{6}$ depends only on $\theta$, which is uniform on $\left[0, \tfrac{\pi}{2}\right]$:

$$C = \left\{(x,\theta) : \theta \in \left[0, \frac{\pi}{6}\right]\right\}$$

$$\text{area}(C) = \frac{d}{2} \cdot \frac{\pi}{6}$$

$$\boxed{P(C) = \frac{d/2 \cdot \pi/6}{\pi d/4} = \frac{\pi d/12}{\pi d/4} = \frac{1}{3}}$$

Since $\theta$ is uniform on $\left[0, \tfrac{\pi}{2}\right]$, the fraction of angles below $\tfrac{\pi}{6}$ is simply $\tfrac{\pi/6}{\pi/2} = \tfrac{1}{3}$. No integration needed.

---

## Event $D$ — Center Closer Than $\tfrac{d}{4}$ to Nearest Line

The condition $x < \tfrac{d}{4}$ depends only on $x$, which is uniform on $\left[0, \tfrac{d}{2}\right]$:

$$D = \left\{(x,\theta) : x \in \left[0, \frac{d}{4}\right]\right\}$$

$$\text{area}(D) = \frac{d}{4} \cdot \frac{\pi}{2}$$

$$\boxed{P(D) = \frac{d/4 \cdot \pi/2}{\pi d/4} = \frac{1}{2}}$$

The center falls in the closer half of $\left[0, \tfrac{d}{2}\right]$ with probability exactly $\tfrac{1}{2}$ — by uniformity of $x$.

---

## Event $E$ — Needle Crosses a Line AND Angle Greater Than $\tfrac{\pi}{4}$

The crossing condition depends on $\theta$, so we cannot separate $x$ and $\theta$ here. We must integrate directly:

$$E = \left\{(x,\theta) : x \leq \frac{L}{2}\sin\theta,\ \theta \in \left(\frac{\pi}{4}, \frac{\pi}{2}\right]\right\}$$

$$\text{area}(E) = \int_{\pi/4}^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{L}{2}\Big[-\cos\theta\Big]_{\pi/4}^{\pi/2}$$

$$= \frac{L}{2}\left(-\cos\frac{\pi}{2} + \cos\frac{\pi}{4}\right) = \frac{L}{2}\left(0 + \frac{\sqrt{2}}{2}\right) = \frac{L\sqrt{2}}{4}$$

$$\boxed{P(E) = \frac{L\sqrt{2}/4}{\pi d/4} = \frac{L\sqrt{2}}{\pi d} = \frac{\sqrt{2}}{2} \cdot \frac{2L}{\pi d} = \frac{\sqrt{2}}{2} \cdot P(A)}$$

So $P(E) \approx 0.707 \cdot P(A)$ — about 70.7% of all crossings happen when $\theta > \tfrac{\pi}{4}$.

**Why not just multiply $P(A) \cdot P(\theta > \tfrac{\pi}{4})$?**

That would give $\tfrac{2L}{\pi d} \cdot \tfrac{1}{2} = \tfrac{L}{\pi d}$, which is **wrong**. The crossing event and the angle event are **not independent** — the probability of crossing given $\theta$ is $P(x \leq \tfrac{L}{2}\sin\theta) = \tfrac{L\sin\theta}{d}$, which depends directly on $\theta$.

---

## Additional Event

**Event $F$** — needle crosses a line given that the angle is exactly in $\left[0, \tfrac{\pi}{6}\right]$:

This is a **conditional probability** $P(A \mid C)$.

First compute $P(A \cap C)$ — needle crosses AND $\theta < \tfrac{\pi}{6}$:

$$\text{area}(A \cap C) = \int_0^{\pi/6} \frac{L}{2}\sin\theta \, d\theta = \frac{L}{2}\Big[-\cos\theta\Big]_0^{\pi/6} = \frac{L}{2}\left(1 - \frac{\sqrt{3}}{2}\right) = \frac{L(2-\sqrt{3})}{4}$$

$$P(A \cap C) = \frac{L(2-\sqrt{3})/4}{\pi d/4} = \frac{L(2-\sqrt{3})}{\pi d}$$

Now apply the definition of conditional probability:

$$\boxed{P(A \mid C) = \frac{P(A \cap C)}{P(C)} = \frac{L(2-\sqrt{3})/(\pi d)}{1/3} = \frac{3L(2-\sqrt{3})}{\pi d}}$$

For $L = d$: $P(A \mid C) = \tfrac{3(2-\sqrt{3})}{\pi} \approx \tfrac{3 \times 0.268}{\pi} \approx 25.60\%$

Compare with unconditional $P(A) = \tfrac{2}{\pi} \approx 63.66\%$ — when the angle is small (needle nearly parallel to the lines), crossing is much less likely, which makes intuitive sense.

---

## Summary Table

| Event | Description | Probability | For $L=d$ |
|---|---|---|---|
| $A$ | Needle crosses a line | $\dfrac{2L}{\pi d}$ | $\approx 63.66\%$ |
| $B$ | No crossing | $1 - \dfrac{2L}{\pi d}$ | $\approx 36.34\%$ |
| $C$ | Angle $< \tfrac{\pi}{6}$ | $\dfrac{1}{3}$ | $33.33\%$ |
| $D$ | Center within $\tfrac{d}{4}$ of line | $\dfrac{1}{2}$ | $50.00\%$ |
| $E$ | Crosses AND $\theta > \tfrac{\pi}{4}$ | $\dfrac{L\sqrt{2}}{\pi d}$ | $\approx 45.02\%$ |
| $F$ | Crosses given $\theta < \tfrac{\pi}{6}$ | $\dfrac{3L(2-\sqrt{3})}{\pi d}$ | $\approx 25.60\%$ |

---

## Key Techniques Used

- **Geometric probability**: $P(A) = \tfrac{\text{area}(A)}{\text{area}(\Omega)}$ for uniform distributions over continuous regions
- **Integration**: the crossing boundary $x = \tfrac{L}{2}\sin\theta$ is curved, requiring $\int_a^b \tfrac{L}{2}\sin\theta\,d\theta$
- **Independence of $x$ and $\theta$**: when an event constrains only one variable, the probability is a simple ratio (Events $C$ and $D$)
- **Complement rule**: Event $B$ trivially from $A$
- **Avoiding false independence**: Event $E$ cannot be factored — crossing probability depends on $\theta$, requiring direct integration
- **Conditional probability**: $P(A \mid C) = \tfrac{P(A \cap C)}{P(C)}$ — used in Event $F$ with geometric interpretation