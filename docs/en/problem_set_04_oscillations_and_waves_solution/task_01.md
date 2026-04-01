# Problem Set 3 — Task 10: Numerical Model of a Dynamical System

**The "Angry Spring" Potential:** $U(x) = \frac{k}{2}x^2 + \lambda x^4$

---

### 1. Determining the Force

The force $F(x)$ is the negative derivative of the potential energy. This is the "restoring force" that pulls the particle back to the center.

$$F(x) = -\frac{dU}{dx} = -kx - 4\lambda x^3$$

> **Theory:** Unlike a normal spring ($F = -kx$), this force grows cubically. The further you stretch it, the "angrier" it gets.

---

### 2. Equation of Motion

Using Newton's Second Law ($F = m \cdot a$), where $a$ is the second derivative of position:

$$m \frac{d^2x}{dt^2} + kx + 4\lambda x^3 = 0$$

This is a **Non-linear Differential Equation** (Duffing Equation). Because of the $x^3$ term, we cannot solve this with a simple "Sine" or "Cosine" formula. We must use a numerical simulation.

---

### 3. The Effect of Initial Energy

The total energy of the system determines how much the "Angry" part ($\lambda x^4$) affects the motion.

* **Low Energy:** The $x^2$ term dominates. The system looks like a normal, soft spring.
* **High Energy:** The $x^4$ term dominates. The walls of the potential "bowl" become extremely steep.
* **Key Insight:** In a normal spring, the period (time for one bounce) is always the same. Here, **the period decreases as amplitude increases** (it bounces faster the harder you push it).

---

### 4. Phase Portrait & Geometry

We visualize the motion in "Phase Space" by plotting Velocity vs. Position.

* **Linear Spring:** The path is a perfect **Ellipse** (smooth trading of energy).
* **Anharmonic Spring:** The path deforms into a **"Diamond" shape**.

> **Interpretation:** The boxy diamond shape proves that the particle spends most of its time at high speed and snaps back instantly at the edges due to the massive $x^3$ force.

---

### 5. Numerical Verification (HTML Simulation)

I developed an interactive simulation using the **Euler-Cromer method** to verify these results. The simulation allows us to live-adjust the "Stiffness" ($\lambda$) and observe the transition from a circular phase portrait to a non-linear diamond.
