# Problem Set 3 - Problem 1: Newton's Second Law

## Problem Statement
A body of mass $m = 2\text{ kg}$ is acted upon by a constant force $\vec{F} = [6, 2]\text{ N}$. 
The body starts from point $\vec{r}(0) = (0, 0)\text{ m}$ with an initial velocity $\vec{v}(0) = (1, -1)\text{ m/s}$.

---

## 1. Determine $\vec{a}(t)$
Using Newton's Second Law:
$$\vec{F} = m \cdot \vec{a} \implies \vec{a} = \frac{\vec{F}}{m}$$
$$\vec{a} = \frac{[6, 2]}{2} = [3, 1] \text{ m/s}^2$$
Since the force and mass are constant, the acceleration is constant:
**$\vec{a}(t) = [3, 1] \text{ m/s}^2$**

---

## 2. Determine $\vec{v}(t)$
We integrate acceleration with respect to time:
$$\vec{v}(t) = \int \vec{a} \, dt = [3t, t] + \vec{C}$$
Using initial condition $\vec{v}(0) = [1, -1]$:
$$[0, 0] + \vec{C} = [1, -1] \implies \vec{C} = [1, -1]$$
**$\vec{v}(t) = [3t + 1, t - 1] \text{ m/s}$**

---

## 3. Determine $\vec{r}(t)$
We integrate velocity with respect to time:
$$\vec{r}(t) = \int \vec{v}(t) \, dt = \left[ \frac{3}{2}t^2 + t, \frac{1}{2}t^2 - t \right] + \vec{D}$$
Using initial condition $\vec{r}(0) = [0, 0]$:
$$[0, 0] + \vec{D} = [0, 0] \implies \vec{D} = [0, 0]$$
**$\vec{r}(t) = [1.5t^2 + t, 0.5t^2 - t] \text{ m}$**

---

## 4. Work Done at $t = 3\text{ s}$
First, find the position at $t = 3$:
$$\vec{r}(3) = [1.5(3^2) + 3, 0.5(3^2) - 3] = [13.5 + 3, 4.5 - 3] = [16.5, 1.5] \text{ m}$$
Work done by a constant force is the dot product:
$$W = \vec{F} \cdot \Delta\vec{r} = [6, 2] \cdot [16.5, 1.5]$$
$$W = (6 \cdot 16.5) + (2 \cdot 1.5) = 99 + 3 = 102 \text{ J}$$
**Work Done $W = 102 \text{ J}$**

---

## 5. Consistency with Work-Energy Theorem
The theorem states $W = \Delta K = K_f - K_i$.

**Initial Kinetic Energy ($t=0$):**
$$v(0)^2 = 1^2 + (-1)^2 = 2$$
$$K_i = \frac{1}{2}mv(0)^2 = \frac{1}{2}(2)(2) = 2 \text{ J}$$

**Final Kinetic Energy ($t=3$):**
$$\vec{v}(3) = [3(3) + 1, 3 - 1] = [10, 2]$$
$$v(3)^2 = 10^2 + 2^2 = 104$$
$$K_f = \frac{1}{2}mv(3)^2 = \frac{1}{2}(2)(104) = 104 \text{ J}$$

**Change in Kinetic Energy:**
$$\Delta K = 104 - 2 = 102 \text{ J}$$
Since $W = 102 \text{ J}$ and $\Delta K = 102 \text{ J}$, the results are consistent.
