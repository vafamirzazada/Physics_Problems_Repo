# Problem Set 3 — Task 09: Potential and Conservative Field

**Given Potential Energy:** $U(x, y) = \frac{k}{2}(x^2 + y^2)$

---

### 1. Force as the Gradient of Potential

The force vector $\vec{F}$ is defined as the negative gradient of the potential energy:
$$\vec{F} = -\nabla U = - \left[ \frac{\partial U}{\partial x}, \frac{\partial U}{\partial y} \right]$$

* $\frac{\partial U}{\partial x} = \frac{k}{2}(2x) = kx$
* $\frac{\partial U}{\partial y} = \frac{k}{2}(2y) = ky$

> **Result:** $\vec{F} = [-kx, -ky]$

---

### 2. Equations of Motion

Using Newton's Second Law ($\vec{F} = m\vec{a}$):
$$m\ddot{x} = -kx \implies \ddot{x} + \frac{k}{m}x = 0$$
$$m\ddot{y} = -ky \implies \ddot{y} + \frac{k}{m}y = 0$$

Let $\omega = \sqrt{k/m}$. The general solutions are independent harmonic oscillations:
* **$x(t) = A_x \cos(\omega t + \phi_x)$**
* **$y(t) = A_y \cos(\omega t + \phi_y)$**

---

### 3. Type of Motion

The motion is a **2D Harmonic Oscillation**. 
* If the phase shift $\Delta \phi = 0$, the trajectory is a **straight line**.
* If the phase shift $\Delta \phi = \pi/2$ and $A_x = A_y$, the trajectory is a **circle**.
* In the general case, the trajectory is an **ellipse** centered at the origin.

---

### 4. Total Energy

The total energy $E$ is the sum of Kinetic and Potential energy:
$$E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2)$$

Substituting the solutions:
> **Result:** $E = \frac{1}{2}k(A_x^2 + A_y^2)$

---

### 5. Geometric Interpretation (Lissajous Curves)

The trajectory is a special case of a Lissajous curve where the frequencies in $x$ and $y$ are identical ($1:1$ ratio). Because the frequencies are the same, the path always closes into a stable ellipse.
