# Task 03: Elimination of Time and Interpretation of Acceleration

---

## 1. Problem Restatement
The path of a particle is given in parametric form:
$$x(t) = 2t^2, \qquad y(t) = 3t^3$$

We must:
1. Eliminate the parameter $t$ to find the Cartesian path equation.
2. Determine the velocity $\vec v(t)$, its magnitude $|\vec v(t)|$, the acceleration $\vec a(t)$, and its magnitude $|\vec a(t)|$.
3. Determine if the acceleration is constant.
4. Prepare for a trajectory drawing.

---

## 2. Physical Model and Assumptions
* **Model:** Two-dimensional motion defined by power-law functions of time.
* **Assumptions:** Standard Cartesian coordinates; time $t \ge 0$.

---

## 3. Mathematical Derivation

### Elimination of the Parameter $t$
From the $x(t)$ equation:
$$x = 2t^2 \implies t^2 = \frac{x}{2} \implies t = \left(\frac{x}{2}\right)^{1/2}$$
Substitute this into the $y(t)$ equation:
$$y = 3t^3 = 3\left[\left(\frac{x}{2}\right)^{1/2}\right]^3 = 3\left(\frac{x}{2}\right)^{3/2}$$
So, the path is:
$$\mathbf{y = \frac{3}{2\sqrt{2}}x^{3/2}}$$

### Velocity $\vec v(t)$
$$\vec v(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right) = \mathbf{(4t, 9t^2)}$$
Magnitude:
$$|\vec v(t)| = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4} = \mathbf{t\sqrt{16 + 81t^2}}$$

### Acceleration $\vec a(t)$
$$\vec a(t) = \left( \frac{dv_x}{dt}, \frac{dv_y}{dt} \right) = \mathbf{(4, 18t)}$$
Magnitude:
$$|\vec a(t)| = \sqrt{4^2 + (18t)^2} = \mathbf{\sqrt{16 + 324t^2}}$$

### Is the acceleration constant?
No. While the $x$-component ($a_x = 4$) is constant, the $y$-component ($a_y = 18t$) depends linearly on time. Therefore, the vector $\vec a(t)$ changes in both magnitude and direction as $t$ increases.

---

## 4. Interpretation of Results
The trajectory is a semi-cubical parabola. Unlike projectile motion where acceleration is a constant vector $(0, -g)$, here the "engine" or "force" causing the motion is increasing its push in the $y$-direction over time.

---

## 5. Conceptual Explanation
Eliminating time allows us to see the "shape" of the path in space, regardless of how fast the particle moves along it. The fact that acceleration depends on $t$ tells us that the net force acting on the particle is not constant; specifically, the force in the $y$-direction must be increasing linearly with time ($F_y \propto t$).

> **Note:** Trajectory plot required (Phase 2). The curve starts at the origin and curves upward more sharply than a standard parabola.
