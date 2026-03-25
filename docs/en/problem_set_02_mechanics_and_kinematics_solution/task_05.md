# Task 05: Elliptical Motion (Purely Kinematic)

---

## 1. Problem Restatement
The path of a particle is given by the parametric equations:
$$x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t)$$

We need to:
1. Calculate the velocity $\vec v(t)$ and acceleration $\vec a(t)$ vectors.
2. Determine if the magnitude of the velocity (speed) is constant.
3. Identify where on the trajectory the velocity is maximum.
4. Prepare for drawing the trajectory and the graphs of $|\vec v(t)|$ and $|\vec a(t)|$.

---

## 2. Physical Model and Assumptions
* **Model:** 2D kinematics. The path is an ellipse centered at the origin with semi-axes $a$ and $b$.
* **Assumptions:** $\omega$ (angular frequency) is constant. Let's assume $a > b > 0$ for the sake of specific interpretation (the ellipse is wider along the x-axis).

---

## 3. Mathematical Derivation

### Velocity Vector $\vec v(t)$
Differentiating the position components with respect to time:
$$\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right) = \mathbf{(-a\omega\sin(\omega t), \, b\omega\cos(\omega t))}$$

### Acceleration Vector $\vec a(t)$
Differentiating the velocity components:
$$\vec a(t) = \left( \frac{dv_x}{dt}, \frac{dv_y}{dt} \right) = \mathbf{(-a\omega^2\cos(\omega t), \, -b\omega^2\sin(\omega t))}$$
*Notice that $\vec a(t) = -\omega^2 \vec r(t)$, meaning the acceleration always points directly toward the center of the ellipse.*

### Magnitude of Velocity $|\vec v(t)|$
$$|\vec v(t)| = \sqrt{(-a\omega\sin(\omega t))^2 + (b\omega\cos(\omega t))^2} = \mathbf{\omega \sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)}}$$

**Is it constant?**
**No.** Unless $a = b$ (which would make it a circle), the terms $\sin^2(\omega t)$ and $\cos^2(\omega t)$ oscillate between $0$ and $1$ as time passes. Therefore, the speed constantly changes.

### Where is the velocity maximum?
To maximize $|\vec v(t)|$, we must maximize the expression inside the square root: $a^2\sin^2(\omega t) + b^2\cos^2(\omega t)$.
Assuming $a > b$ (the x-axis is the major axis):
* The maximum value occurs when $\sin^2(\omega t) = 1$ and $\cos^2(\omega t) = 0$.
* This happens when $\omega t = \frac{\pi}{2}, \frac{3\pi}{2}, \dots$
* At these times, the position is $x = 0$ and $y = \pm b$.
**Conclusion:** The velocity is strictly maximum at the ends of the **minor axis** (the points closest to the center). Conversely, it is minimum at the ends of the major axis.

---

## 4. Interpretation of Results
In this specific parametrization, the "angle" $\omega t$ changes at a constant rate. Because the ellipse is "flattened," sweeping out the same angle takes the particle across a longer physical distance near the minor axis than near the major axis. Thus, the particle must speed up when it is closer to the origin and slow down when it is further away.

---

## 5. Conceptual Explanation
It is highly important to distinguish this purely kinematic mathematical motion from gravitational orbital motion (Kepler's laws). In gravitational orbits, angular momentum is conserved, meaning the actual angular velocity $\omega$ is *not* constant. Here, we forced $\omega$ to be constant, which creates a specific "engine-driven" motion where acceleration always points exactly to the geometric center, behaving like a 2D harmonic oscillator (e.g., a mass on two perpendicular springs).

> **Note:** HTML visualization required (Phase 2).
> **Requirements:** > 1. Draw the elliptical trajectory.
> 2. Plot $|\vec v(t)|$ and $|\vec a(t)|$ vs. time on a side-by-side graph to show that they are out of phase (when speed is max, acceleration magnitude is min).
