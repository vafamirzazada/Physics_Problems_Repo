# Problem 2: Velocity Selection in Crossed Fields

This task analyzes the behavior of a charged particle moving through a region where electric ($\vec{E}$) and magnetic ($\vec{B}$) fields are perpendicular to each other (crossed fields). We derive the specific velocity required for a particle to maintain a straight-line trajectory.

---

### 1. Condition for Rectilinear Motion

For a particle with charge $q$ moving with velocity $\vec{v}$ through crossed fields, the total Lorentz force is:
$$\vec{F} = q\vec{E} + q(\vec{v} \times \vec{B})$$

For **rectilinear (straight-line) motion**, the net force must be zero ($\vec{F} = 0$). This occurs when the electric force and the magnetic force are equal in magnitude but opposite in direction:
$$|q\vec{E}| = |q\vec{v} \times \vec{B}|$$

Given $\vec{E} = (0, E, 0)$ and $\vec{B} = (0, 0, B)$, and assuming motion along the x-axis $\vec{v} = (v, 0, 0)$:
* **Electric Force:** $\vec{F}_E = (0, qE, 0)$
* **Magnetic Force:** $\vec{F}_B = q(v \hat{i} \times B \hat{k}) = (0, -qvB, 0)$

Setting the sum to zero:
$$qE - qvB = 0 \implies v_d = \frac{E}{B}$$

This specific velocity, $v_d$, is known as the **drift velocity** or selection velocity.

---

### 2. Numerical Calculation

**Given:**
* $E = 400 \, \text{V/m}$
* $B = 0.8 \, \text{T}$

**Calculation:**
$$v_d = \frac{400}{0.8} = 500 \, \text{m/s}$$

---

### 3. Kinetic Energy in Steady Motion

**No, the kinetic energy does not change.**
In steady rectilinear motion, the net force is zero, meaning there is no acceleration ($\vec{a} = 0$). Since the velocity vector remains constant in both magnitude and direction, the kinetic energy ($E_k = \frac{1}{2}mv^2$) remains constant. Furthermore, we previously established that magnetic forces never do work, and in this specific case, the electric force is perfectly cancelled out.

---

### 4. Operating Principle of the Velocity Selector

The velocity selector acts as a "filter" for charged particles based on their speed, independent of their mass or charge magnitude.

* **Particles with $v = E/B$:** The forces balance perfectly. They travel in a straight line and pass through the exit slit.
* **Particles with $v > E/B$:** The magnetic force ($qvB$) dominates. They are deflected (in this setup, downward) and hit the wall.
* **Particles with $v < E/B$:** The electric force ($qE$) dominates. They are deflected upward and hit the wall.

**Interpretation:** This device allows scientists to "tune" an experimental beam to a precise speed by simply adjusting the ratio of the electric and magnetic field strengths.
