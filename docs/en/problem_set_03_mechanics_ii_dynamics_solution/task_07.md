# Problem Set 3 — Task 07: Vertical Throw with Linear Drag

**Equation of Motion:** $m \frac{dv}{dt} = -mg - kv$  
**Initial Conditions:** $v(0) = v_0$, $x(0) = 0$

---

### 1. Solving the Equation of Motion

This is a separable first-order differential equation. We rearrange to isolate $v$:

$$\frac{dv}{mg + kv} = -\frac{1}{m} dt$$

Integrating both sides:

$$\frac{1}{k} \ln(mg + kv) = -\frac{t}{m} + C$$

Applying $v(0) = v_0$ to find $C$: $C = \frac{1}{k} \ln(mg + kv_0)$.

$$\ln\left( \frac{mg + kv}{mg + kv_0} \right) = -\frac{k}{m}t$$

Solving for $v(t)$:

> **Result (Velocity):** $v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}$

---

### 2. Determine the Maximum Height ($H_{max}$)

At the maximum height, the velocity is zero ($v = 0$). First, we find the time $t_{up}$ it takes to reach the peak:

$$0 = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t_{up}} - \frac{mg}{k}$$

$$t_{up} = \frac{m}{k} \ln\left( 1 + \frac{kv_0}{mg} \right)$$

Integrating $v(t)$ from $0$ to $t_{up}$ gives the height:

> **Result:** $H_{max} = \frac{mv_0}{k} - \frac{m^2g}{k^2} \ln\left( 1 + \frac{kv_0}{mg} \right)$

---

### 3. Comparison with the Case Without Drag ($k=0$)

| Feature | Without Drag | With Linear Drag |
| :--- | :--- | :--- |
| **Max Height** | $H = \frac{v_0^2}{2g}$ | $H < \frac{v_0^2}{2g}$ (Significant reduction) |
| **Time to Peak** | $t = \frac{v_0}{g}$ | $t < \frac{v_0}{g}$ (Stops sooner) |
| **Velocity Curve** | Linear ($v = v_0 - gt$) | Exponential decay toward terminal velocity |

---

### 4. Comparison: Analytical vs. Numerical

* **Analytical:** Provides an exact solution but becomes extremely difficult if drag is non-linear (e.g., $v^2$).
* **Numerical:** Uses time-stepping (Euler or Runge-Kutta). It easily handles complex forces but introduces "truncation error" if the time step $\Delta t$ is too large.
* **Observation:** In the presence of drag, numerical methods are preferred for engineering because they can account for changing air density or varying drag coefficients.
