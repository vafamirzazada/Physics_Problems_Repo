# Problem 6: The Damped Harmonic Oscillator

In real-world physics, oscillators don't bounce forever. They lose energy to their surroundings. We model this using the **Damped Harmonic Oscillator** equation.

### 1. The Equation of Motion
The system is governed by a second-order linear ordinary differential equation:
$$m\frac{d^{2}x}{dt^{2}} + b\frac{dx}{dt} + kx = 0$$

* **$m\frac{d^{2}x}{dt^{2}}$ (Inertia):** The mass resisting acceleration.
* **$b\frac{dx}{dt}$ (Damping Force):** The friction or "drag" proportional to velocity.
* **$kx$ (Restoring Force):** The spring pulling the mass back to equilibrium.

### 2. Classification of Damping Cases
The behavior of the system depends on the **damping ratio**. We define the characteristic equation and look at the discriminant $\Delta = b^2 - 4mk$.

* **Underdamped ($b^2 < 4mk$):** The system oscillates, but the amplitude decays exponentially over time. This is like a bell ringing that slowly fades.
* **Critically Damped ($b^2 = 4mk$):** The system returns to equilibrium as quickly as possible without any oscillation. This is the ideal setting for car shock absorbers or high-end door closers.
* **Overdamped ($b^2 > 4mk$):** The damping is so strong (like moving through thick honey) that the system slowly crawls back to equilibrium without ever crossing it.

### 3. Numerical Strategy: Runge-Kutta (RK4)
To solve this numerically, we break the second-order ODE into a system of two first-order ODEs:
1. $\frac{dx}{dt} = v$
2. $\frac{dv}{dt} = \frac{-bv - kx}{m}$

We then apply the **RK4 method**, which provides much higher precision than the basic Euler method by taking four "weighted samples" of the slope for every time step.

### 4. Visualizing the Phase Portrait
By plotting **Velocity ($v$) vs. Position ($x$)**, we can see the "energy spiral." In a damped system, the trajectory spirals inward toward the origin $(0,0)$, representing the loss of total mechanical energy.
