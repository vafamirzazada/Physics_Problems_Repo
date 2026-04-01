# Problem Set 3 — Task 02: Inclined Plane with Friction

**Parameters:** Mass: $m$  
Angle of Inclination: $\alpha$  
Kinetic Friction Coefficient: $\mu$  
Descent Height: $h$

---

### 1. Forces Acting on the Body

We decompose the forces into a coordinate system where the $x$-axis is parallel to the slope:

1. **Gravity ($\vec{F}_g$):** $mg$, acting vertically downward.
   * Component down the slope: $F_{gx} = mg \sin \alpha$
   * Component perpendicular to slope: $F_{gy} = mg \cos \alpha$
2. **Normal Force ($\vec{N}$):** Acts perpendicular to the surface.
   * $N = mg \cos \alpha$
3. **Friction Force ($\vec{F}_f$):** Acts opposite to the motion (up the slope).
   * $F_f = \mu N = \mu mg \cos \alpha$

---

### 2. Derivation of Acceleration ($a$)

Using Newton's Second Law ($\sum F = ma$) along the $x$-axis:

$$mg \sin \alpha - F_f = ma$$

$$mg \sin \alpha - \mu mg \cos \alpha = ma$$

Dividing the entire equation by $m$:

> **Result:** $a = g(\sin \alpha - \mu \cos \alpha)$

---

### 3. Time of Descent ($t$)

The length of the slope ($s$) can be calculated from the height $h$:
$$s = \frac{h}{\sin \alpha}$$

Using the kinematic equation for an object starting from rest ($s = \frac{1}{2}at^2$):

$$\frac{h}{\sin \alpha} = \frac{1}{2} [g(\sin \alpha - \mu \cos \alpha)] t^2$$

Solving for $t$:

> **Result:** $t = \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}$

---

### 4. Final Velocity ($v$)

Using the velocity-time relationship $v = at$:

$$v = g(\sin \alpha - \mu \cos \alpha) \cdot \sqrt{\frac{2h}{g \sin \alpha (\sin \alpha - \mu \cos \alpha)}}$$

Alternatively, using $v^2 = 2as$:

$$v^2 = 2 \cdot g(\sin \alpha - \mu \cos \alpha) \cdot \frac{h}{\sin \alpha}$$

> **Result:** $v = \sqrt{2gh \left(1 - \mu \cot \alpha\right)}$

---

### 5. Energy Balance Consistency

To check consistency, we use the Work-Energy Theorem:
**Initial Potential Energy = Final Kinetic Energy + Work Done by Friction**

$$E_p = K_f + W_{friction}$$

1. **Potential Energy:** $mgh$
2. **Kinetic Energy:** $\frac{1}{2}mv^2 = \frac{1}{2}m \left( 2gh (1 - \mu \frac{\cos \alpha}{\sin \alpha}) \right) = mgh - \mu mgh \cot \alpha$
3. **Work by Friction:** $F_f \cdot s = (\mu mg \cos \alpha) \cdot (\frac{h}{\sin \alpha}) = \mu mgh \cot \alpha$

**Verification:**
$$mgh = (mgh - \mu mgh \cot \alpha) + (\mu mgh \cot \alpha)$$
$$mgh = mgh$$

> **Conclusion:** The results are consistent with the energy balance.
