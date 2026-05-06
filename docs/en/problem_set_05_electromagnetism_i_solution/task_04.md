# Problem 4: Motion of a Particle in a Uniform Electric Field

This task analyzes the kinematics and dynamics of a charged particle moving through a constant, uniform electric field. We derive the analytical trajectory and verify the solution through the principle of energy conservation.

---

### 1. Initial Conditions and Physical Parameters

The system is defined by the following constants:
* **Mass ($m$):** $0.02 \, \text{kg}$
* **Charge ($q$):** $1 \, \text{mC} = 10^{-3} \, \text{C}$
* **Electric Field ($\vec{E}$):** $(30, 100) \, \text{N/C}$
* **Initial Velocity ($\vec{v}_0$):** $(20, 0) \, \text{m/s}$
* **Initial Position ($\vec{r}_0$):** $(0, 0)$

---

### 2. Equations of Motion

According to Newton's Second Law ($\vec{F} = m\vec{a}$) and the electrostatic force law ($\vec{F} = q\vec{E}$), the acceleration is constant:
$$\vec{a} = \frac{q\vec{E}}{m} = \left( \frac{10^{-3} \cdot 30}{0.02}, \frac{10^{-3} \cdot 100}{0.02} \right) = (1.5, 5.0) \, \text{m/s}^2$$

**Analytical Solutions for Velocity:**
* $v_x(t) = v_{0x} + a_x t = 20 + 1.5t$
* $v_y(t) = v_{0y} + a_y t = 0 + 5.0t$

**Analytical Solutions for Position (Trajectory):**
* $x(t) = x_0 + v_{0x}t + \frac{1}{2}a_x t^2 = 20t + 0.75t^2$
* $y(t) = y_0 + v_{0y}t + \frac{1}{2}a_y t^2 = 2.5t^2$

---

### 3. Time to Reach Vertical Velocity ($v_y = 50 \, \text{m/s}$)

Using the vertical velocity equation:
$$v_y(t) = a_y t \implies 50 = 5.0t$$
$$t = 10 \, \text{seconds}$$

---

### 4. Kinetic Energy Calculation ($t = 0.05 \, \text{s}$)

First, we find the velocities at $t = 0.05 \, \text{s}$:
* $v_x(0.05) = 20 + 1.5(0.05) = 20.075 \, \text{m/s}$
* $v_y(0.05) = 5.0(0.05) = 0.25 \, \text{m/s}$

The magnitude of velocity squared ($v^2$):
$$v^2 = 20.075^2 + 0.25^2 \approx 403.005 + 0.0625 = 403.0675 \, \text{m}^2/\text{s}^2$$

**Kinetic Energy ($E_k$):**
$$E_k = \frac{1}{2}mv^2 = 0.5 \cdot 0.02 \cdot 403.0675 = 4.030675 \, \text{J}$$

---

### 5. Energy Balance Verification

The work done by the electric field ($W$) must equal the change in kinetic energy ($\Delta E_k$).
$$W = q\vec{E} \cdot \vec{d} = q(E_x \Delta x + E_y \Delta y)$$

At $t=0.05 \, \text{s}$:
* $\Delta x = 20(0.05) + 0.75(0.05)^2 = 1.0 + 0.001875 = 1.001875 \, \text{m}$
* $\Delta y = 2.5(0.05)^2 = 0.00625 \, \text{m}$

$$W = 10^{-3} \cdot (30 \cdot 1.001875 + 100 \cdot 0.00625) = 10^{-3} \cdot (30.05625 + 0.625) = 0.03068125 \, \text{J}$$

**Initial Kinetic Energy:** $E_{k0} = \frac{1}{2}(0.02)(20^2) = 4.0 \, \text{J}$
**Final Kinetic Energy:** $4.030675 \, \text{J}$
**Change in Energy:** $\Delta E_k \approx 0.030675 \, \text{J}$

The Work-Energy theorem ($W \approx \Delta E_k$) is satisfied, confirming numerical consistency.
