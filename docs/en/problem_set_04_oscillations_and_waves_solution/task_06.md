# Problem 6: The Damped Harmonic Oscillator

In real-world physical systems, oscillations do not continue indefinitely because energy is dissipated by resistive forces such as friction or air resistance. We model this behavior using the **Damped Harmonic Oscillator**.

---

### 1. The Equation of Motion
The system is governed by a second-order linear ordinary differential equation based on Newton's Second Law:

$$m\frac{d^{2}x}{dt^{2}} + b\frac{dx}{dt} + kx = 0$$

**Where each term represents a specific physical force:**

* **$m\frac{d^{2}x}{dt^{2}}$ (Inertia):** The force required to accelerate the mass $m$.
* **$b\frac{dx}{dt}$ (Damping Force):** A resistive force that is directly proportional to the velocity ($v = \frac{dx}{dt}$), where $b$ is the damping coefficient.
* **$kx$ (Restoring Force):** The linear force of the spring pulling the mass back toward the equilibrium position $x=0$.

---

### 2. General Solutions and Classification of Cases
To solve the equation, we assume a solution of the form $x(t) = e^{rt}$. Substituting this into the differential equation yields the characteristic equation:

$$mr^2 + br + k = 0$$

The roots are determined by the quadratic formula: $r = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}$. The behavior of the system is classified based on the discriminant $\Delta = b^2 - 4mk$:

#### **Case I: Underdamped ($b^2 < 4mk$)**
The discriminant is negative, resulting in complex roots. The solution is an oscillation with an exponentially decaying amplitude:

$$x(t) = A e^{-\gamma t} \cos(\omega_d t + \varphi)$$

Where $\gamma = \frac{b}{2m}$ is the decay constant and $\omega_d = \sqrt{\frac{k}{m} - \frac{b^2}{4m^2}}$ is the damped angular frequency.

#### **Case II: Critically Damped ($b^2 = 4mk$)**
The discriminant is zero, leading to a repeated real root. This represents the threshold where the system returns to equilibrium as fast as possible without oscillating:

$$x(t) = (A + Bt) e^{-\gamma t}$$

#### **Case III: Overdamped ($b^2 > 4mk$)**
The discriminant is positive, resulting in two distinct real roots. The damping is so strong that the system crawls back to equilibrium without ever crossing it:

$$x(t) = A e^{r_1 t} + B e^{r_2 t}$$

---

### 3. Numerical Strategy: Runge-Kutta (RK4)
While analytical solutions are exact, we solve the equation numerically to allow for interactive investigation of the parameter $b$. We convert the second-order ODE into a system of two first-order ODEs:

$$\frac{dx}{dt} = v$$

$$\frac{dv}{dt} = \frac{-bv - kx}{m}$$

We apply the **4th Order Runge-Kutta (RK4) method**, which calculates four "slopes" ($k_1$ through $k_4$) at different points within the time step $\Delta t$ and takes a weighted average to update the state. This provides superior accuracy and numerical stability compared to simpler methods like Euler.

---

### 4. Interpretation of Results

* **Effect of Parameter $b$:** Increasing the damping coefficient $b$ reduces the number of oscillations until the system reaches the critically damped threshold.
* **Graph of $x(t)$:** In the underdamped case, the graph shows a sinusoidal wave trapped inside an exponentially decaying "envelope."
* **Phase Portrait:** By plotting Velocity ($v$) against Position ($x$), we visualize the energy loss. In a perfect oscillator, this would be a closed loop; however, in a damped system, the trajectory is an inward spiral ending at the origin $(0,0)$, representing total energy dissipation.
