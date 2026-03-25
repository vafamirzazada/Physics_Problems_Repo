# Task 07: 2D Motion with a Given Acceleration

---

## 1. Problem Restatement
We are given a constant 2D acceleration vector and the starting conditions (initial velocity and position).

**Given:**
* Acceleration: $\vec a = (2, -3)$
* Initial velocity: $\vec v(0) = (1, 0)$
* Initial position: $\vec r(0) = (0, 0)$

**We need to:**
1. Determine the velocity function $\vec v(t)$ over time.
2. Determine the position function $\vec r(t)$ over time.
3. Note the requirements for drawing the trajectory and vectors (HTML animation).

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics with constant acceleration. 
* **Assumptions:** * The object is a point mass.
    * The acceleration does not change with time.
    * The motion starts at time $t = 0$ at the origin.

---

## 3. Mathematical Derivation

Since acceleration is the derivative of velocity, we find velocity by **integrating** the acceleration. Since velocity is the derivative of position, we find position by **integrating** the velocity.

We will do this separately for the $x$ and $y$ directions.

### Step 1: Determine Velocity $\vec v(t)$

**For the X-direction:**
Integrate the $x$-acceleration ($a_x = 2$):

$$v_x(t) = \int 2 \, dt$$

$$v_x(t) = 2t + C_x$$

Use the initial condition $v_x(0) = 1$ to find $C_x$:

$$1 = 2(0) + C_x \implies C_x = 1$$

$$v_x(t) = 2t + 1$$

**For the Y-direction:**
Integrate the $y$-acceleration ($a_y = -3$):

$$v_y(t) = \int -3 \, dt$$

$$v_y(t) = -3t + C_y$$

Use the initial condition $v_y(0) = 0$ to find $C_y$:

$$0 = -3(0) + C_y \implies C_y = 0$$

$$v_y(t) = -3t$$

**Final Velocity Vector:**
Combine the $x$ and $y$ components:

$$\vec v(t) = (2t + 1, \, -3t)$$

---

### Step 2: Determine Position $\vec r(t)$

**For the X-direction:**
Integrate the $x$-velocity ($v_x(t) = 2t + 1$):

$$x(t) = \int (2t + 1) \, dt$$

$$x(t) = t^2 + t + C_{rx}$$

Use the initial position $x(0) = 0$ to find $C_{rx}$:

$$0 = 0^2 + 0 + C_{rx} \implies C_{rx} = 0$$

$$x(t) = t^2 + t$$

**For the Y-direction:**
Integrate the $y$-velocity ($v_y(t) = -3t$):

$$y(t) = \int -3t \, dt$$

$$y(t) = -\frac{3}{2}t^2 + C_{ry}$$

Use the initial position $y(0) = 0$ to find $C_{ry}$:

$$0 = -\frac{3}{2}(0)^2 + C_{ry} \implies C_{ry} = 0$$

$$y(t) = -1.5t^2$$

**Final Position Vector:**
Combine the $x$ and $y$ components:

$$\vec r(t) = (t^2 + t, \, -1.5t^2)$$

---

## 4. Interpretation of Results
The $x$-component of the position increases very quickly because it has both an initial velocity and a positive acceleration. The $y$-component drops downwards (negative) increasingly fast due to the negative acceleration. The resulting path will look like a sideways, downward-curving parabola.

---

## 5. Conceptual Explanation
This problem demonstrates the core principle of classical mechanics: if you know where an object starts, how fast it is moving initially, and the forces acting on it (which give it constant acceleration), you can perfectly predict its entire future path by simply integrating step-by-step. 

> **Note:** HTML animation required (Phase 2).
> **Requirements:** Draw the parabolic trajectory curve. Add visual arrows for $\vec v(t)$ (always tangent to the curve) and $\vec a(t)$ (always pointing in the constant $(2, -3)$ direction) that update as the point moves along the path.
