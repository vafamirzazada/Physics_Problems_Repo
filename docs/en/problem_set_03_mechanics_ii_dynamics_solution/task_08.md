# Problem Set 3 — Task 08: Harmonic Oscillator (Formal Dynamics)

**Equation of Motion:** $m\ddot{x} + kx = 0$  
*(Where $\ddot{x}$ represents the second derivative of position with respect to time, $d^2x/dt^2$.)*

---

### 1. Solving the Equation

We rewrite the equation as:
$$\ddot{x} + \frac{k}{m}x = 0$$

Let $\omega^2 = \frac{k}{m}$. The equation becomes $\ddot{x} + \omega^2 x = 0$. This is a linear homogeneous second-order differential equation. The general solution is:

> **Result:** $x(t) = A \cos(\omega t + \phi)$

*(Where $A$ is the amplitude and $\phi$ is the initial phase.)*

---

### 2. Natural Frequency

The parameter $\omega$ represents the **angular frequency**:

> **$\omega = \sqrt{\frac{k}{m}}$** (rad/s)

The **natural frequency** $f$ (number of oscillations per second) is:
> **$f = \frac{\omega}{2\pi} = \frac{1}{2\pi}\sqrt{\frac{k}{m}}$** (Hz)

---

### 3. Energy as a Function of Time

To find the total energy $E(t)$, we sum the Kinetic Energy ($K$) and Potential Energy ($U$):

1. **Velocity:** $v(t) = \dot{x}(t) = -A\omega \sin(\omega t + \phi)$
2. **Kinetic Energy:** $K(t) = \frac{1}{2}mv^2 = \frac{1}{2}m A^2 \omega^2 \sin^2(\omega t + \phi)$
3. **Potential Energy:** $U(t) = \frac{1}{2}kx^2 = \frac{1}{2}k A^2 \cos^2(\omega t + \phi)$

Using $k = m\omega^2$:

> **$E(t) = \frac{1}{2}m A^2 \omega^2 \left[ \sin^2(\omega t + \phi) + \cos^2(\omega t + \phi) \right]$**

---

### 4. Conservation of Energy

Using the trigonometric identity $\sin^2\theta + \cos^2\theta = 1$:

> **$E = \frac{1}{2}m A^2 \omega^2 = \frac{1}{2}k A^2$**

**Conclusion:** The total energy is constant (independent of time). Energy oscillates between purely kinetic (at the equilibrium point $x=0$) and purely potential (at the turning points $x = \pm A$), but the sum remains conserved.

---

### 5. Phase Space Interpretation

In phase space, we plot **Momentum ($p = m\dot{x}$)** on the Y-axis and **Position ($x$)** on the X-axis.

For a harmonic oscillator, the relationship between $p$ and $x$ is:
$$\frac{p^2}{m^2 A^2 \omega^2} + \frac{x^2}{A^2} = 1$$

> **Interpretation:** The trajectory in phase space is an **Ellipse**. 
> * A larger ellipse represents a higher energy state.
> * The motion travels clockwise around the ellipse as time progresses.
