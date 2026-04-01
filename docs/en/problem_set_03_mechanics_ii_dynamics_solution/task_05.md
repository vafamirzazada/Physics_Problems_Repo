# Problem Set 3 — Task 05: One-Dimensional Elastic Collision

**Scenario:** Two bodies with masses $m_1$ and $m_2$ collide head-on in a perfectly elastic manner.

---

### 1. Conservation Principles

In an **elastic collision**, both total momentum and total kinetic energy are conserved.

**Conservation of Momentum:**
$$m_1 v_{1i} + m_2 v_{2i} = m_1 v_{1f} + m_2 v_{2f}$$

**Conservation of Kinetic Energy:**
$$\frac{1}{2}m_1 v_{1i}^2 + \frac{1}{2}m_2 v_{2i}^2 = \frac{1}{2}m_1 v_{1f}^2 + \frac{1}{2}m_2 v_{2f}^2$$

---

### 2. Velocities After Collision

By solving the system of equations above (often using the "Relative Velocity" shortcut: $v_{1i} - v_{2i} = -(v_{1f} - v_{2f})$), we derive the final velocities:

> **Final Velocity of $m_1$:** > $$v_{1f} = \frac{m_1 - m_2}{m_1 + m_2}v_{1i} + \frac{2m_2}{m_1 + m_2}v_{2i}$$

> **Final Velocity of $m_2$:** > $$v_{2f} = \frac{2m_1}{m_1 + m_2}v_{1i} + \frac{m_2 - m_1}{m_1 + m_2}v_{2i}$$

---

### 3. Case 1: Equal Masses ($m_1 = m_2$)

If the masses are equal, we substitute $m_1 = m_2$ into the equations:

* $v_{1f} = \frac{0}{2m}v_{1i} + \frac{2m}{2m}v_{2i} = v_{2i}$
* $v_{2f} = \frac{2m}{2m}v_{1i} + \frac{0}{2m}v_{2i} = v_{1i}$

> **Physical Interpretation:** The bodies simply **swap velocities**. This is what happens in a game of billiards when one ball hits another of the same weight directly.

---

### 4. Case 2: The "Wall" Limit ($m_2 \gg m_1$)

If the second mass is much larger than the first (like a ball hitting a wall), we assume $m_2 \approx \infty$. If the wall is at rest ($v_{2i} = 0$):

* $v_{1f} \approx \frac{-m_2}{m_2}v_{1i} = -v_{1i}$
* $v_{2f} \approx \frac{2m_1}{m_2}v_{1i} \approx 0$

> **Physical Interpretation:** The small mass **bounces back** with the same speed in the opposite direction, while the massive body remains virtually stationary.

---

### 5. Summary Table

| Scenario | Mass Relation | Outcome |
| :--- | :--- | :--- |
| **Billiards** | $m_1 = m_2$ | Velocities are perfectly swapped. |
| **Wall** | $m_2 \gg m_1$ | $m_1$ reflects; $m_2$ doesn't move. |
| **Bowling** | $m_1 \gg m_2$ | $m_1$ keeps moving; $m_2$ is rocketed forward at $2v_{1i}$. |
