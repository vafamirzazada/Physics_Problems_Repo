# Problem Set 3 — Task 10: Numerical Model of a Dynamical System

**Given Potential:** $U(x) = \frac{k}{2}x^2 + \lambda x^4$

---

### 1. Determining the Force

The force $F$ is the negative derivative of the potential energy with respect to position:

$$F(x) = -\frac{dU}{dx} = -\frac{d}{dx} \left( \frac{k}{2}x^2 + \lambda x^4 \right)$$

> **Result:** $F(x) = -kx - 4\lambda x^3$

---

### 2. Equation of Motion

Applying Newton's Second Law ($F = m\ddot{x}$):

$$m\ddot{x} = -kx - 4\lambda x^3$$

> **Standard Form:** $\ddot{x} + \frac{k}{m}x + \frac{4\lambda}{m}x^3 = 0$

*(This is known as the **Duffing Equation** without damping. It is non-linear because of the $x^3$ term.)*

---

### 3. Effect of Initial Energy on Motion

Total Energy $E = \frac{1}{2}m\dot{x}^2 + U(x)$.

* **Low Energy ($E \approx 0$):** The $\lambda x^4$ term is negligible. The system behaves like a Simple Harmonic Oscillator with a constant period.
* **High Energy ($E \gg 0$):** The $x^4$ term dominates. The "restoring force" becomes much stronger at large displacements. 
* **Key Difference:** In a linear spring, the period is independent of amplitude. In this quartic potential, **the period decreases as amplitude increases** (the clock ticks faster the further you pull the weight).

---

### 4. Phase Portrait Interpretation

In the phase portrait ($\dot{x}$ vs $x$):
* The trajectories are closed loops, indicating periodic motion.
* Unlike the perfect ellipses of a linear spring, these loops become "boxier" or more "diamond-shaped" as energy increases, reflecting the non-linear stiffness.
