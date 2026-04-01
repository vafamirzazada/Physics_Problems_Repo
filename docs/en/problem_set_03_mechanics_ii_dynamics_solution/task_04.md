# Problem Set 3 — Task 04: Conservation of Energy

**Scenario:** A body falls from an initial height $h$ without air resistance.

---

### 1. Total Energy $E(h)$

The total mechanical energy is the sum of Kinetic Energy ($T$) and Potential Energy ($U$). At the initial launch point (height $h$, starting from rest):

* **Kinetic Energy:** $T(h) = \frac{1}{2}m(0)^2 = 0$
* **Potential Energy:** $U(h) = mgh$

> **Total Energy:** $E = T + U = mgh$

*(Since there is no air resistance, this value $mgh$ remains constant throughout the entire fall.)*

---

### 2. Velocity as a Function of Height $v(y)$

Let $y$ be the current height of the body ($0 \leq y \leq h$). At any point during the fall:

$$mgh = \frac{1}{2}mv(y)^2 + mgy$$

We solve for $v(y)$:

$$mg(h - y) = \frac{1}{2}mv^2$$

$$v^2 = 2g(h - y)$$

> **Result:** $v(y) = \sqrt{2g(h - y)}$

---

### 3. Comparison with Newton's Second Law

Using Newton's Second Law for a falling body:
$F = ma \implies -mg = m \frac{dv}{dt} \implies a = -g$

Using the kinematic equation $v_f^2 = v_i^2 + 2a\Delta y$:
* $v_i = 0$
* $a = -g$
* $\Delta y = (y - h)$

$$v^2 = 0 + 2(-g)(y - h) = 2g(h - y)$$

> **Conclusion:** The energy conservation approach and Newton's Second Law yield the exact same result. However, the energy method is often faster as it avoids time-dependent integration.

---

### 4. Height for 75% Kinetic Energy

We want to find the height $y$ where $T = 0.75 E$.

Since $E = T + U$, if $T = 0.75E$, then $U$ must be $0.25E$:

$$mgy = 0.25 (mgh)$$

Dividing both sides by $mg$:

> **Result:** $y = 0.25h$ (or $1/4$ of the original height)

*(Physically, this makes sense: as the object falls, it loses potential energy and gains kinetic energy. When it has fallen 75% of the way down, it has converted 75% of its potential energy into kinetic energy.)*
