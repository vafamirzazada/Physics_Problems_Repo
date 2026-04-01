# Problem Set 3 — Task 06: Motion with Linear Drag

**Given Force:** $F = -kv$ (Drag force proportional to velocity)  
**Initial Conditions:** $v(0) = v_0$, $x(0) = 0$

---

### 1. Equation of Motion and Solution

Using Newton's Second Law ($F = ma$):

$$-kv = m \frac{dv}{dt}$$

We rearrange this into a separable differential equation:

$$\frac{dv}{v} = -\frac{k}{m} dt$$

Integrating both sides:

$$\ln(v) = -\frac{k}{m}t + C$$

Applying the initial condition $v(0) = v_0$:

$$\ln(v_0) = 0 + C \implies C = \ln(v_0)$$

$$\ln\left(\frac{v}{v_0}\right) = -\frac{k}{m}t$$

Taking the exponential of both sides:

> **Result (Velocity):** $v(t) = v_0 e^{-\frac{k}{m}t}$

---

### 2. Investigation of the Limit $\lim_{t \to \infty} v(t)$

We look at the behavior of the velocity as time approaches infinity:

$$\lim_{t \to \infty} \left( v_0 e^{-\frac{k}{m}t} \right) = v_0 \cdot 0$$

> **Result:** $\lim_{t \to \infty} v(t) = 0$

**Physical Interpretation:** The drag force constantly saps the kinetic energy of the body. Because the force is always present as long as $v > 0$, the body will eventually come to a complete stop, though mathematically it only reaches zero at infinity.

---

### 3. Comparison with Motion Without Drag

| Property | Motion Without Drag ($k=0$) | Motion With Linear Drag ($k>0$) |
| :--- | :--- | :--- |
| **Acceleration** | $0$ (Constant velocity) | Negative and decreasing ($a \propto -v$) |
| **Velocity Path** | Constant ($v = v_0$) | Exponential Decay ($v \propto e^{-t}$) |
| **Stopping Distance** | Infinite | Finite ($x_{max} = \frac{mv_0}{k}$) |
| **Final State** | Continues forever | Eventually stops |

---

### 4. Displacement Calculation (Extra Context)

To find how far it travels, we integrate the velocity:

$$x(t) = \int_{0}^{t} v_0 e^{-\frac{k}{m}\tau} d\tau = \frac{mv_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)$$

As $t \to \infty$, the body reaches a total distance of **$D = \frac{mv_0}{k}$**.
