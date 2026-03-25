# Task 02: Projectile Motion

---

## 1. Problem Restatement
Analyze a body moving in a uniform gravitational field without air resistance.
Given: Initial velocity $v_0$ and launch angle $\alpha$ relative to the horizontal.

We must:
* Derive equations for horizontal ($x$) and vertical ($y$) motion.
* Determine the total time of flight.
* Determine the maximum height reached.
* Determine the total horizontal range.
* Find the optimal angle for maximum range.
* Note requirements for a future trajectory animation.

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics (Projectile Motion).
* **Assumptions:** * Gravity is constant ($g \approx 9.81 \text{ m/s}^2$) and pulls straight down (negative $y$-direction).
    * There is no air resistance (vacuum conditions).
    * The starting point is the origin $(0,0)$.

---

## 3. Mathematical Derivation

### Step 1: Decomposition of Initial Velocity
The initial velocity vector must be split into horizontal ($x$) and vertical ($y$) pieces using trigonometry:

$$v_{0x} = v_0 \cos \alpha$$

$$v_{0y} = v_0 \sin \alpha$$

### Step 2: Equations of Motion
Since there is no air resistance, horizontal acceleration is zero ($a_x = 0$). Vertical acceleration is just gravity ($a_y = -g$).

**Horizontal position:**
$$x(t) = v_{0x} t$$
$$x(t) = (v_0 \cos \alpha) t$$

**Vertical position:**
$$y(t) = v_{0y} t + \frac{1}{2} a_y t^2$$
$$y(t) = (v_0 \sin \alpha) t - \frac{1}{2} g t^2$$

### Step 3: Time of Flight ($t_f$)
The object hits the ground when its vertical position is zero again ($y = 0$). 

Set the vertical equation to zero:
$$(v_0 \sin \alpha) t - \frac{1}{2} g t^2 = 0$$

Factor out $t$:
$$t \left( v_0 \sin \alpha - \frac{1}{2} g t \right) = 0$$

This gives two solutions. The first is $t = 0$ (the launch). We want the second solution (the landing):
$$v_0 \sin \alpha - \frac{1}{2} g t_f = 0$$

Move the gravity term to the other side:
$$\frac{1}{2} g t_f = v_0 \sin \alpha$$

Multiply by 2 and divide by $g$:
**$$t_f = \frac{2 v_0 \sin \alpha}{g}$$**

### Step 4: Maximum Height ($H$)
The object reaches its highest point exactly halfway through its flight. So, the time to reach the top is half of $t_f$:
$$t_{top} = \frac{v_0 \sin \alpha}{g}$$

Plug this time into the vertical position equation $y(t)$:
$$H = (v_0 \sin \alpha) \left( \frac{v_0 \sin \alpha}{g} \right) - \frac{1}{2} g \left( \frac{v_0 \sin \alpha}{g} \right)^2$$

Multiply the terms out:
$$H = \frac{v_0^2 \sin^2 \alpha}{g} - \frac{1}{2} g \left( \frac{v_0^2 \sin^2 \alpha}{g^2} \right)$$

Cancel one $g$ in the second term:
$$H = \frac{v_0^2 \sin^2 \alpha}{g} - \frac{v_0^2 \sin^2 \alpha}{2g}$$

Subtract half from a whole:
**$$H = \frac{v_0^2 \sin^2 \alpha}{2g}$$**

### Step 5: Range ($R$)
The range is the horizontal distance traveled by the time the object hits the ground ($t = t_f$).

Plug $t_f$ into the horizontal position equation $x(t)$:
$$R = (v_0 \cos \alpha) \left( \frac{2 v_0 \sin \alpha}{g} \right)$$

Rearrange the variables to group the trig functions:
$$R = \frac{v_0^2 (2 \sin \alpha \cos \alpha)}{g}$$

Use the trigonometric identity $\sin(2\alpha) = 2 \sin \alpha \cos \alpha$:
**$$R = \frac{v_0^2 \sin(2\alpha)}{g}$$**

### Step 6: Maximum Range Angle
To get the biggest possible range, the sine function in our range formula must be as large as possible. The maximum value of sine is 1.

$$\sin(2\alpha) = 1$$

The angle that gives a sine of 1 is $90^\circ$:
$$2\alpha = 90^\circ$$

Divide by 2:
**$$\alpha = 45^\circ$$**

---

## 4. Interpretation of Results
The math proves that the horizontal and vertical motions don't affect each other. The time the object spends in the air is determined *entirely* by its vertical speed and gravity. However, how far it travels (the range) depends on finding the perfect balance: a high angle keeps it in the air longer, but a low angle gives it more forward speed. The math shows that exactly $45^\circ$ is the perfect compromise in a vacuum.

---

## 5. Conceptual Explanation
Imagine separating the motion into two shadows: one moving along the ground, and one moving straight up a wall. The shadow on the ground moves at a perfectly steady, constant speed. The shadow on the wall acts exactly like a ball thrown straight up—it slows down, stops at the peak, and falls back down. Projectile motion is just these two simple shadows happening at the same time.

> **Note:** HTML visualization required (Phase 2). 
> **Interactive Features:** Sliders for initial velocity $v_0$ and angle $\alpha$ to observe real-time changes in the parabolic trajectory, highlighting the $45^\circ$ maximum range.
