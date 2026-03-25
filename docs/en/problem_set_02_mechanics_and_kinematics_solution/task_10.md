# Task 10: Analysis of Motion from Numerical Data

---

## 1. Problem Restatement
We are given a theoretical position function and instructed to analyze it using numerical approximation (simulating data collected by a sensor).

**Given:**
* Position function: $x(t) = t + \frac{1}{20}t^2$
* Time interval: $t \in [0, 10]$
* Time step: $\Delta t = 0.1$

**We need to:**
1. Approximate velocity using the finite difference method.
2. Approximate acceleration using the finite difference method.
3. Compare these numerical approximations with the exact analytical solutions.
4. Investigate how the size of the time step ($\Delta t$) affects the accuracy.

---

## 2. Physical Model and Assumptions
* **Model:** 1D Kinematics analyzed via discrete numerical methods.
* **Assumptions:** Data is sampled at regular, discrete intervals ($\Delta t$). The function is smooth enough that finite differences closely approximate continuous derivatives.

---

## 3. Mathematical Derivation

To compare effectively, let's first find the "true" answers using calculus, and then see how the computer's approximation stacks up.

### Step 1: The Analytical Solution (The "True" Values)
Using standard derivatives:

**Exact Velocity:**
$$v(t) = \frac{dx}{dt} = \frac{d}{dt}\left(t + 0.05t^2\right)$$
**$$v_{exact}(t) = 1 + 0.1t$$**

**Exact Acceleration:**
$$a(t) = \frac{dv}{dt} = \frac{d}{dt}(1 + 0.1t)$$
**$$a_{exact}(t) = 0.1$$**

---

### Step 2: Numerical Velocity (Finite Difference)
A computer doesn't know calculus; it only knows how to calculate the slope between two data points. We use the **forward difference method**:

$$v_{num}(t) = \frac{x(t + \Delta t) - x(t)}{\Delta t}$$

Let's plug our position formula into this:
$$x(t + \Delta t) = (t + \Delta t) + 0.05(t + \Delta t)^2$$
$$x(t + \Delta t) = t + \Delta t + 0.05(t^2 + 2t\Delta t + \Delta t^2)$$

Now, subtract $x(t)$ and divide by $\Delta t$:
$$v_{num}(t) = \frac{\Delta t + 0.1t\Delta t + 0.05\Delta t^2}{\Delta t}$$

Divide every term by $\Delta t$:
**$$v_{num}(t) = 1 + 0.1t + 0.05\Delta t$$**

---

### Step 3: Numerical Acceleration
We apply the finite difference method again, this time to the numerical velocity we just found:

$$a_{num}(t) = \frac{v_{num}(t + \Delta t) - v_{num}(t)}{\Delta t}$$

Plug in our $v_{num}$ formula:
$$a_{num}(t) = \frac{(1 + 0.1(t + \Delta t) + 0.05\Delta t) - (1 + 0.1t + 0.05\Delta t)}{\Delta t}$$

Most terms cancel out, leaving:
$$a_{num}(t) = \frac{0.1\Delta t}{\Delta t}$$

**$$a_{num}(t) = 0.1$$**

---

### Step 4: Comparison and the Effect of Time Step

**Comparing Velocity:**
* $v_{exact} = 1 + 0.1t$
* $v_{num} = 1 + 0.1t + 0.05\Delta t$

The numerical velocity has an extra term: $+0.05\Delta t$. This is the **error**. 
If our time step is $\Delta t = 0.1$, the error is $0.05(0.1) = 0.005$. The numerical velocity is slightly overestimating the true velocity.

**Comparing Acceleration:**
* $a_{exact} = 0.1$
* $a_{num} = 0.1$

Interestingly, the numerical acceleration is exactly correct! This happens because the original position function is a perfect parabola (quadratic), and second-order finite differences are exact for quadratics.

**Effect of Time Step ($\Delta t$):**
If we make the time step smaller (e.g., $\Delta t = 0.01$), the error term ($0.05\Delta t$) becomes much smaller ($0.0005$). As $\Delta t \to 0$, the numerical solution perfectly matches the analytical solution. This is the very definition of a limit in calculus!

---

## 4. Interpretation of Results
The finite difference method works by drawing a straight line between two nearby points (a secant line) and pretending it is the tangent line. Because a parabola curves upward, the secant line looking "forward" in time will always be slightly steeper than the true tangent line. This is why our numerical velocity is slightly too high.

---

## 5. Conceptual Explanation
This problem bridges the gap between theoretical physics and computational physics. Real-world sensors (like GPS or a car's speedometer) don't have continuous formulas; they only give position data at discrete "ticks" of a clock. Understanding that dividing by $\Delta t$ introduces a predictable error is crucial for writing accurate physics simulations or programming real-world robots.

> **Note:** HTML/JS programming required (Phase 2).
> **Requirements:** Write a script that calculates an array of $x$, $v_{num}$, and $a_{num}$ using a `for` loop, plots them against the analytical curves, and includes a slider to change $\Delta t$ to visually demonstrate the error shrinking.
