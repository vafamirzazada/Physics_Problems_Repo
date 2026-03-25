# Task 01: Uniform and Uniformly Accelerated Motion

---

## 1. Problem Restatement
Given the equation of motion:
$$x(t) = x_0 + v_0t + \frac{1}{2}at^2$$

We need to:
1. Determine the velocity $v(t)$ and acceleration $a(t)$.

2. For the parameters $x_0 = 0, v_0 = 5 \text{ m/s}, a = -2 \text{ m/s}^2$:
    * Calculate the stopping time.
    * Determine the maximum velocity.
    * Calculate the maximum displacement.

3. Prepare for a future visualization of $x(t), v(t), a(t)$.

---

## 2. Physical Model and Assumptions
* **Model:** One-dimensional kinematics with constant acceleration (Rectilinear motion).
* **Assumptions:** The object is a point mass. Time $t$ starts at $0$.
* **Sign Convention:** Positive direction is to the right. Since $a$ is negative, the object is decelerating.

---

## 3. Mathematical Derivation

### Functional Forms
The velocity is the time derivative of position:
$$v(t) = \frac{dx}{dt} = \frac{d}{dt}\left(x_0 + v_0t + \frac{1}{2}at^2\right) = v_0 + at$$

The acceleration is the time derivative of velocity:
$$a(t) = \frac{dv}{dt} = \frac{d}{dt}(v_0 + at) = a$$

### Numerical Calculations
Given: $x_0 = 0$, $v_0 = 5$, $a = -2$.

**1. Stopping Time ($t_s$):**
The object stops when $v(t) = 0$:
$$0 = 5 - 2t_s \implies 2t_s = 5 \implies t_s = 2.5 \text{ s}$$

**2. Maximum Displacement ($x_{max}$):**
This occurs at the moment the object stops ($t = 2.5$):
$$x(2.5) = 0 + 5(2.5) + \frac{1}{2}(-2)(2.5)^2$$
$$x(2.5) = 12.5 - 6.25 = 6.25 \text{ m}$$

**3. Maximum Velocity:**
Since $a = -2$ (negative), the velocity $v(t) = 5 - 2t$ decreases immediately for $t > 0$. Therefore, the maximum velocity is at the start:
$$v_{max} = v(0) = 5 \text{ m/s}$$

---

## 4. Interpretation of Results
The particle starts with a velocity of $5 \text{ m/s}$ but is being "pulled back" by a constant acceleration of $-2 \text{ m/s}^2$. This creates a parabolic position-time graph. At $2.5 \text{ seconds}$, the particle reaches its furthest point ($6.25 \text{ m}$) and stops momentarily before reversing direction.



---

## 5. Conceptual Explanation
In physics, constant acceleration means the velocity changes by the same amount every second. Here, the velocity drops by $2 \text{ m/s}$ every second. Because the acceleration is opposite to the initial motion, the kinetic energy is converted into "distance" until the object stops.

> **Note:** HTML visualization required (Phase 2). The application should allow adjusting $v_0$ and $a$ to see how the "peak" of the displacement curve shifts.
