# Problem Set 3 — Task 01: Newton's Second Law & Energy

**Body Mass ($m$):** $2 \text{ kg}$  
**Constant Force ($\vec{F}$):** $[6, 2] \text{ N}$

---

### 1. Acceleration $\vec{a}(t)$

According to Newton's Second Law, the acceleration is derived directly from the force:

$$\vec{a} = \frac{\vec{F}}{m}$$

$$\vec{a} = \frac{[6, 2]}{2}$$

> **Result:** $\vec{a}(t) = [3, 1] \text{ m/s}^2$

*(Note: Since the force is constant, the acceleration remains constant throughout the motion.)*

---

### 2. Velocity $\vec{v}(t)$

To find the velocity, we integrate the acceleration vector over time:

$$\vec{v}(t) = \int \vec{a} \, dt = [3t, t] + \vec{C}$$

We apply the initial condition $\vec{v}(0) = [1, -1]$ to solve for the constant $\vec{C}$:

$$[0, 0] + \vec{C} = [1, -1] \implies \vec{C} = [1, -1]$$

> **Result:** $\vec{v}(t) = [3t + 1, t - 1] \text{ m/s}$

---

### 3. Trajectory $\vec{r}(t)$

To find the position, we integrate the velocity vector:

$$\vec{r}(t) = \int \vec{v}(t) \, dt = \left[ 1.5t^2 + t, 0.5t^2 - t \right] + \vec{D}$$

Using the initial condition $\vec{r}(0) = [0, 0]$:

$$[0, 0] + \vec{D} = [0, 0] \implies \vec{D} = [0, 0]$$

> **Result:** $\vec{r}(t) = [1.5t^2 + t, 0.5t^2 - t] \text{ m}$

---

### 4. Work Done ($W$) at $t = 3 \text{ s}$

First, we calculate the displacement at $3$ seconds:

$$\vec{r}(3) = [1.5(3^2) + 3, 0.5(3^2) - 3] = [16.5, 1.5] \text{ m}$$

For a constant force, Work is the dot product of Force and Displacement:

$$W = \vec{F} \cdot \Delta\vec{r} = [6, 2] \cdot [16.5, 1.5]$$

$$W = (6 \times 16.5) + (2 \times 1.5) = 99 + 3$$

> **Result:** $W = 102 \text{ J}$

---

### 5. Work-Energy Theorem Verification

The theorem states that the work done equals the change in Kinetic Energy: $W = \Delta K$.

**Initial State ($t=0$):**
$$v(0)^2 = 1^2 + (-1)^2 = 2$$
$$K_i = \frac{1}{2} m v(0)^2 = \frac{1}{2}(2)(2) = 2 \text{ J}$$

**Final State ($t=3$):**
$$\vec{v}(3) = [3(3) + 1, 3 - 1] = [10, 2]$$
$$v(3)^2 = 10^2 + 2^2 = 104$$
$$K_f = \frac{1}{2} m v(3)^2 = \frac{1}{2}(2)(104) = 104 \text{ J}$$

**Conclusion:**
$$\Delta K = 104 - 2 = 102 \text{ J}$$

Since **$W = \Delta K = 102 \text{ J}$**, the calculation is consistent with the Work-Energy Theorem.
