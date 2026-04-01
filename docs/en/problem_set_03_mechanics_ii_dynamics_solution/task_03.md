# Problem Set 3 — Task 03: Work of a Variable Force

**Given:** A one-dimensional restoring force $F(x) = -kx$.

---

### 1. Equation of Motion and Solution

Applying Newton's Second Law ($F = ma$):

$$-kx = m \frac{d^2x}{dt^2}$$

Rearranging into the standard form for a second-order differential equation:

$$\frac{d^2x}{dt^2} + \frac{k}{m}x = 0$$

Let $\omega^2 = \frac{k}{m}$. The general solution for this harmonic oscillator is:

> **Result:** $x(t) = A \cos(\omega t + \phi)$

*(Where $A$ is amplitude and $\phi$ is the phase constant.)*

---

### 2. Work Done from $0$ to $x_0$

Since the force is variable (it depends on $x$), we must use integration to calculate Work ($W$):

$$W = \int_{0}^{x_0} F(x) \, dx$$

$$W = \int_{0}^{x_0} (-kx) \, dx$$

Integrating:

$$W = \left[ -\frac{1}{2}kx^2 \right]_{0}^{x_0}$$

> **Result:** $W = -\frac{1}{2}kx_0^2$

---

### 3. Interpretation as Potential Energy ($U$)

Work done by a conservative force is equal to the negative change in potential energy ($W = -\Delta U$).

If we define $U(0) = 0$, then:

$$\Delta U = -W$$

> **Result:** $U(x) = \frac{1}{2}kx^2$

*(This shows that the work done **by** the restoring force is negative because it opposes the displacement, resulting in energy being stored in the system.)*

---

### 4. Verification of $F = -\frac{dU}{dx}$

To verify the relationship, we take the negative derivative of our potential energy result:

$$-\frac{d}{dx} \left( \frac{1}{2}kx^2 \right) = -\frac{1}{2}k (2x)$$

> **Result:** $F = -kx$

*(The relationship is verified. The force is the negative gradient of the potential energy.)*

---

### 5. Graphical Interpretation

* **$F(x) = -kx$**: A straight line passing through the origin with a negative slope ($-k$). It is in the 2nd and 4th quadrants.
* **$U(x) = \frac{1}{2}kx^2$**: A parabola opening upwards, centered at the origin ($x=0$).
