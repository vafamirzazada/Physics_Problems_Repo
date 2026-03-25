# Task 04: Circular Motion

---

## 1. Problem Restatement
A body moves in a circle of radius $R$ with constant angular velocity $\omega$. 

We must:
1. Determine the position $\vec r(t)$, velocity $\vec v(t)$, and acceleration $\vec a(t)$ vectors.
2. Calculate the magnitudes $|\vec r(t)|$, $|\vec v(t)|$, and $|\vec a(t)|$.
3. Show that the acceleration is centripetal (pointing toward the center).
4. Prepare for a vector visualization.

---

## 2. Physical Model and Assumptions
* **Model:** Uniform Circular Motion in the $xy$-plane.
* **Assumptions:** The center of the circle is at the origin $(0,0)$. The angular velocity $\omega$ is constant.

---

## 3. Mathematical Derivation

### Position Vector $\vec r(t)$
In polar coordinates mapped to Cartesian:
$$\vec r(t) = (R \cos(\omega t), R \sin(\omega t))$$

### Velocity Vector $\vec v(t)$
Differentiating $\vec r(t)$ with respect to time $t$:
$$\vec v(t) = \frac{d\vec r}{dt} = (-R\omega \sin(\omega t), R\omega \cos(\omega t))$$

### Acceleration Vector $\vec a(t)$
Differentiating $\vec v(t)$ with respect to time $t$:
$$\vec a(t) = \frac{dv}{dt} = (-R\omega^2 \cos(\omega t), -R\omega^2 \sin(\omega t))$$

### Magnitudes
* **Position:** $|\vec r| = \sqrt{R^2(\cos^2(\omega t) + \sin^2(\omega t))} = \mathbf{R}$
* **Velocity:** $|\vec v| = \sqrt{R^2\omega^2(\sin^2(\omega t) + \cos^2(\omega t))} = \mathbf{R\omega}$
* **Acceleration:** $|\vec a| = \sqrt{R^2\omega^4(\cos^2(\omega t) + \sin^2(\omega t))} = \mathbf{R\omega^2}$

### Proof of Centripetal Acceleration
Notice that the expression for $\vec a(t)$ can be factored:
$$\vec a(t) = -\omega^2 (R \cos(\omega t), R \sin(\omega t)) = -\omega^2 \vec r(t)$$
Because $\vec a(t)$ is a negative multiple of the position vector $\vec r(t)$, it points in the **exact opposite direction** of the radius vector—meaning it points directly toward the center of the circle. This is the definition of **centripetal acceleration**.

---

## 4. Interpretation of Results
Even though the speed $|\vec v| = R\omega$ is constant, the velocity vector is constantly changing its **direction**. This change in direction requires an acceleration. Since this acceleration always points toward the center, it changes the direction of motion without changing the speed.

---

## 5. Conceptual Explanation
In circular motion, the velocity is always tangent to the circle, while the acceleration is always perpendicular to the velocity (radial). If the acceleration had a component parallel to the velocity, the object would speed up or slow down. Since it is perfectly radial, it only "turns" the object.

> **Note:** HTML visualization required (Phase 2).
> **Interactive Features:** Show vectors $\vec r$ (blue), $\vec v$ (green), and $\vec a$ (red) rotating in real-time.
