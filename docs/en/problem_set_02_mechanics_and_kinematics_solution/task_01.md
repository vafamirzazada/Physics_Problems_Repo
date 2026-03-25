# Task 01: Uniform and Uniformly Accelerated Motion

## 1. Problem Restatement
Given the equation of motion:
$$x(t) = x_0 + v_0t + \frac{1}{2}at^2$$
We need to determine $v(t)$ and $a(t)$, and for the specific parameters ($x_0 = 0$, $v_0 = 5$ m/s, $a = -2$ m/s²), calculate:
* The stopping time.
* The maximum displacement.
* Analysis of velocity relative to the sign of acceleration.

## 2. Physical Model and Assumptions
* **Model:** One-dimensional kinematics with constant acceleration.
* **Assumptions:** The object is a point mass; time $t \ge 0$.
* **Parameters:** Initial velocity is positive (moving right), but acceleration is negative (braking).

## 3. Mathematical Derivation

**Velocity and Acceleration Functions:**
* Velocity is the first derivative of position:
$$v(t) = \frac{dx}{dt} = \frac{d}{dt}\left(x_0 + v_0t + \frac{1}{2}at^2\right) = \mathbf{v_0 + at}$$
* Acceleration is the first derivative of velocity:
$$a(t) = \frac{dv}{dt} = \frac{d}{dt}(v_0 + at) = \mathbf{a}$$

**Calculation with Given Values ($v_0 = 5, a = -2$):**

1.  **Stopping Time ($t_s$):**
    The object stops when $v(t) = 0$.
    $$0 = 5 + (-2)t_s \implies 2t_s = 5 \implies \mathbf{t_s = 2.5 \text{ s}}$$

2.  **Maximum Displacement ($x_{max}$):**
    The maximum displacement occurs at the stopping time ($t = 2.5$).
    $$x(2.5) = 0 + 5(2.5) + \frac{1}{2}(-2)(2.5)^2$$
    $$x(2.5) = 12.5 - 6.25 = \mathbf{6.25 \text{ m}}$$

3.  **Maximum Velocity Analysis:**
    Since acceleration is constant and negative ($a = -2$), the velocity $v(t) = 5 - 2t$ is **strictly decreasing**. Therefore, the maximum velocity occurs at the earliest possible time, $t=0$, which is **$5$ m/s**.

## 4. Interpretation of Results
The object starts moving with an initial speed but immediately begins to slow down (decelerate) due to the negative acceleration. It travels 6.25 meters before coming to a momentary halt at 2.5 seconds. If the motion continues after $t=2.5$, the object will begin moving in the negative direction (reversing).


## 5. Conceptual Explanation
In this scenario, the acceleration vector points opposite to the velocity vector. This is why the "speed" (magnitude of velocity) decreases. The quadratic nature of the position equation creates a parabolic path in a position-time graph, where the "peak" of the parabola represents the furthest point reached before the object turns back.

> **Note:** HTML visualization required (Phase 2) for interactive $x(t), v(t), a(t)$ graphs.
