# Task 02: Projectile Motion

---

## 1. Problem Restatement
Analyze a body moving in a uniform gravitational field without air resistance.
Given: Initial velocity $v_0$ and launch angle $\alpha$ relative to the horizontal.

We must:
* Derive equations for horizontal ($x$) and vertical ($y$) motion.
* Determine time of flight, maximum height, and range.
* Find the optimal angle for maximum range.
* Note requirements for a future trajectory animation.

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics (Projectile Motion).
* **Assumptions:** * Gravity is constant ($g \approx 9.81 \text{ m/s}^2$) and acts only in the negative $y$-direction.
    * No air resistance (vacuum conditions).
    * The starting point is the origin $(0,0)$.

---

## 3. Mathematical Derivation

### Decomposition of Initial Velocity
$$v_{0x} = v_0 \cos \alpha, \qquad v_{0y} = v_0 \sin \alpha$$

### Equations of Motion
Since $a_x = 0$ and $a_y = -g$:
1. **Horizontal:** $x(t) = (v_0 \cos \alpha)t$
2. **Vertical:** $y(t) = (v_0 \sin \alpha)t - \frac{1}{2}gt^2$

### Time of Flight ($t_f$)
The body hits the ground when $y(t) = 0$:
$$(v_0 \sin \alpha)t_f - \frac{1}{2}gt_f^2 = 0 \implies t_f \left(v_0 \sin \alpha - \frac{1}{2}gt_f\right) = 0$$
Ignoring $t=0$, we get:
$$t_f = \frac{2v_0 \sin \alpha}{g}$$

### Maximum Height ($H$)
This occurs when the vertical velocity $v_y = 0$, which is at $t = \frac{t_f}{2}$:
$$H = y\left(\frac{v_0 \sin \alpha}{g}\right) = (v_0 \sin \alpha)\left(\frac{v_0 \sin \alpha}{g}\right) - \frac{1}{2}g\left(\frac{v_0 \sin \alpha}{g}\right)^2 = \frac{v_0^2 \sin^2 \alpha}{2g}$$

### Range ($R$)
The range is the horizontal distance at $t = t_f$:
$$R = x(t_f) = (v_0 \cos \alpha) \left(\frac{2v_0 \sin \alpha}{g}\right) = \frac{v_0^2 (2 \sin \alpha \cos \alpha)}{g}$$
Using the trigonometric identity $2 \sin \alpha \cos \alpha = \sin(2\alpha)$:
$$R = \frac{v_0^2 \sin(2\alpha)}{g}$$

### Maximum Range Angle
$R$ is maximized when $\sin(2\alpha)$ is maximum (equal to 1):
$$2\alpha = 90^\circ \implies \alpha = 45^\circ$$

---

## 4. Interpretation of Results
The trajectory is a downward-opening parabola. The symmetry of the motion means the object spends as much time going up as it does coming down. Interestingly, the range is identical for angles $\alpha$ and $(90^\circ - \alpha)$ (e.g., $30^\circ$ and $60^\circ$).

---

## 5. Conceptual Explanation
Projectile motion is the superposition of two independent motions: a constant velocity motion horizontally and a free-fall motion vertically. This independence is key to understanding why the horizontal distance doesn't affect the time it takes to hit the ground—only the vertical component matters.

> **Note:** HTML visualization/animation required (Phase 2). 
> **Interactive Features:** Sliders for $v_0$ and $\alpha$ to observe real-time changes in the parabolic trajectory.
