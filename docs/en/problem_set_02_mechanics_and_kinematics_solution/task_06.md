# Task 06: Cycloid – Trajectory of a Point on a Rolling Circle

---

## 1. Problem Restatement
A circle of radius $R$ rolls without slipping along the $x$-axis. A point on its rim traces a cycloid given by:
$$x(t) = R(\omega t - \sin(\omega t)), \qquad y(t) = R(1 - \cos(\omega t))$$

We must:
1. Determine the velocity $\vec v(t)$ and acceleration $\vec a(t)$ vectors.
2. Calculate the speed $|\vec v(t)|$ and find when the point "stops" relative to the ground.
3. Determine the maximum values of $|\vec v(t)|$ and $|\vec a(t)|$.
4. Note the requirements for an HTML animation.
5. Compare the cycloid with circular motion in a reference frame attached to the circle.

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics of rigid body motion (rolling without slipping). 
* **Assumptions:** The wheel moves along a flat, horizontal surface ($y=0$). The angular velocity $\omega$ of the rolling circle is constant. The initial position of the tracking point at $t=0$ is at the origin $(0,0)$.

---

## 3. Mathematical Derivation

### 1. Velocity and Acceleration Vectors
Differentiating the position equations with respect to time $t$:
$$v_x(t) = \frac{dx}{dt} = R(\omega - \omega\cos(\omega t)) = R\omega(1 - \cos(\omega t))$$
$$v_y(t) = \frac{dy}{dt} = R\omega\sin(\omega t)$$

So, the velocity vector is:
$$\vec v(t) = (R\omega(1 - \cos(\omega t)), R\omega\sin(\omega t))$$

Differentiating the velocity components:
$$a_x(t) = \frac{dv_x}{dt} = R\omega^2\sin(\omega t)$$
$$a_y(t) = \frac{dv_y}{dt} = R\omega^2\cos(\omega t)$$

So, the acceleration vector is:
$$\vec a(t) = (R\omega^2\sin(\omega t), R\omega^2\cos(\omega t))$$

### 2. Magnitude of Velocity and "Stops"
$$|\vec v(t)| = \sqrt{v_x^2 + v_y^2} = \sqrt{R^2\omega^2(1 - \cos(\omega t))^2 + R^2\omega^2\sin^2(\omega t)}$$
$$|\vec v(t)| = R\omega\sqrt{1 - 2\cos(\omega t) + \cos^2(\omega t) + \sin^2(\omega t)}$$

Since $\cos^2(\omega t) + \sin^2(\omega t) = 1$:
$$|\vec v(t)| = R\omega\sqrt{2 - 2\cos(\omega t)} = R\omega\sqrt{2(1 - \cos(\omega t))}$$

Using the half-angle trigonometric identity $1 - \cos(\omega t) = 2\sin^2\left(\frac{\omega t}{2}\right)$:
$$|\vec v(t)| = R\omega\sqrt{4\sin^2\left(\frac{\omega t}{2}\right)} = 2R\omega\left\vert \sin\left(\frac{\omega t}{2}\right) \right\vert$$

**When does it stop?**
The point stops when $|\vec v(t)| = 0$, which occurs when $\sin\left(\frac{\omega t}{2}\right) = 0$.
$$\frac{\omega t}{2} = n\pi \implies t = \frac{2n\pi}{\omega} \quad \text{for } n = 0, 1, 2, \dots$$
At these exact moments, $y(t) = 0$. The point is momentarily stationary as it touches the ground.

### 3. Maximum Values

**Maximum Speed:** The maximum speed occurs when the sine term is at its peak, meaning $\left\vert \sin\left(\frac{\omega t}{2}\right) \right\vert = 1$.

$$|\vec v|_{max} = 2R\omega$$

This happens at the very top of the circle's path ($y = 2R$).

**Maximum Acceleration:**

$$|\vec a(t)| = \sqrt{(R\omega^2\sin(\omega t))^2 + (R\omega^2\cos(\omega t))^2}$$
$$|\vec a(t)| = \sqrt{R^2\omega^4(\sin^2(\omega t) + \cos^2(\omega t))} = R\omega^2$$

The magnitude of acceleration is strictly **constant**! Thus, its maximum value is simply $R\omega^2$.

---

## 4. Interpretation of Results
The most striking result is that a point on a rolling wheel does not move at a constant speed relative to the ground. When it touches the ground, its instantaneous velocity is exactly zero (this is what "rolling without slipping" means). When it is at the very top of the wheel, it moves at $2R\omega$, which is twice the speed of the center of the wheel!



---

## 5. Conceptual Explanation and Frame of Reference
If we change our reference frame to move with the center of the wheel (which moves horizontally at constant velocity $\vec V_c = (R\omega, 0)$), the horizontal motion of the center is subtracted. 

In this moving frame, the point simply undergoes uniform circular motion:
$$\vec r'(t) = (-R\sin(\omega t), -R\cos(\omega t))$$

The cycloid is therefore mathematically and physically the superposition (vector sum) of uniform linear translation and uniform circular motion. 

> **Note:** HTML animation required (Phase 2).
> **Requirements:** A visual showing the rolling circle, the point drawing the cycloid curve, and the dynamic vectors $\vec v$ and $\vec a$ scaling and rotating as the point moves.  The magnitude of acceleration is strictly **constant**! Thus, its maximum value is simply $R\omega^2$.

---

## 4. Interpretation of Results
The most striking result is that a point on a rolling wheel does not move at a constant speed. When it touches the ground, its instantaneous velocity is exactly zero (this is what "rolling without slipping" means). When it is at the very top of the wheel, it moves at $2R\omega$, which is twice the speed of the center of the car/wheel!

---

## 5. Conceptual Explanation and Frame of Reference
If we change our reference frame to move with the center of the wheel (which moves horizontally at constant velocity $\vec V_c = (R\omega, 0)$), the horizontal motion of the center is subtracted. 
In this moving frame, the point simply undergoes uniform circular motion:
$$\vec r'(t) = (-R\sin(\omega t), -R\cos(\omega t))$$
The cycloid is therefore mathematically and physically just the superposition (vector sum) of uniform linear translation and uniform circular motion. 

> **Note:** HTML animation required (Phase 2).
> **Requirements:** A visual showing the rolling circle, the point drawing the cycloid curve, and the dynamic vectors $\vec v$ and $\vec a$ scaling and rotating as the point moves.  This happens at the very top of the circle's path ($y = 2R$).
* **Maximum Acceleration:**
  $$|\vec a(t)| = \sqrt{(R\omega^2\sin(\omega t))^2 + (R\omega^2\cos(\omega t))^2} = \sqrt{R^2\omega^4(\sin^2(\omega t) + \cos^2(\omega t))} = \mathbf{R\omega^2}$$
  The magnitude of acceleration is strictly **constant**! Thus, its maximum value is simply $R\omega^2$.

---

## 4. Interpretation of Results
The most striking result is that a point on a rolling wheel does not move at a constant speed. When it touches the ground, its instantaneous velocity is exactly zero (this is what "rolling without slipping" means). When it is at the very top of the wheel, it moves at $2R\omega$, which is twice the speed of the center of the car/wheel!

---

## 5. Conceptual Explanation and Frame of Reference
If we change our reference frame to move with the center of the wheel (which moves horizontally at constant velocity $\vec V_c = (R\omega, 0)$), the horizontal motion of the center is subtracted. 
In this moving frame, the point simply undergoes uniform circular motion:
$$\vec r'(t) = (-R\sin(\omega t), -R\cos(\omega t))$$
The cycloid is therefore mathematically and physically just the superposition (vector sum) of uniform linear translation and uniform circular motion. 

> **Note:** HTML animation required (Phase 2).
> **Requirements:** A visual showing the rolling circle, the point drawing the cycloid curve, and the dynamic vectors $\vec v$ and $\vec a$ scaling and rotating as the point moves.
### 3. Maximum Values
* **Maximum Speed:** $|\vec v|_{max}$ occurs when $\left|\sin\left(\frac{\omega t}{2}\right)\right| = 1$.
  $$|\vec v|_{max} = \mathbf{2R\omega}$$
  This happens at the very top of the circle's path ($y = 2R$).
* **Maximum Acceleration:**
  $$|\vec a(t)| = \sqrt{(R\omega^2\sin(\omega t))^2 + (R\omega^2\cos(\omega t))^2} = \sqrt{R^2\omega^4(\sin^2(\omega t) + \cos^2(\omega t))} = \mathbf{R\omega^2}$$
  The magnitude of acceleration is strictly **constant**! Thus, its maximum value is simply $R\omega^2$.

---

## 4. Interpretation of Results
The most striking result is that a point on a rolling wheel does not move at a constant speed. When it touches the ground, its instantaneous velocity
