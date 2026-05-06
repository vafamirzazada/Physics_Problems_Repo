# Problem 3: Electric Field of a Two-Charge System

This task analyzes the electric field distribution produced by two point charges of unequal magnitude ($+q$ and $+2q$) placed on the x-axis. We explore the field geometry, locate equilibrium points, and examine the system's behavior in the far-field limit.

---

### 1. General Field Vector Derivation $\vec{E}(x, y)$

The total electric field at any point $P(x, y)$ is the vector sum of the fields from charge $Q_1 = +q$ at $(-a, 0)$ and $Q_2 = +2q$ at $(a, 0)$:

$$\vec{E}_{total} = \vec{E}_1 + \vec{E}_2$$

For a general point $(x, y)$:
$$\vec{E}(x, y) = k q \left[ \frac{(x+a)\hat{i} + y\hat{j}}{((x+a)^2 + y^2)^{3/2}} + \frac{2(x-a)\hat{i} + 2y\hat{j}}{((x-a)^2 + y^2)^{3/2}} \right]$$

**Specific Cases:**
* **On the y-axis $\vec{E}(0, y)$:** Due to symmetry, the y-components add and the x-components partially cancel.
$$\vec{E}(0, y) = k q \left[ \frac{-a\hat{i} + y\hat{j}}{(a^2 + y^2)^{3/2}} + \frac{2a\hat{i} + 2y\hat{j}}{(a^2 + y^2)^{3/2}} \right] = \frac{k q}{(a^2 + y^2)^{3/2}} (a\hat{i} + 3y\hat{j})$$

* **On the x-axis $\vec{E}(x, 0)$:**
$$\vec{E}(x, 0) = k q \left[ \frac{\text{sgn}(x+a)}{(x+a)^2} + \frac{2\text{sgn}(x-a)}{(x-a)^2} \right] \hat{i}$$

---

### 2. Condition for Zero Field ($\vec{E} = 0$)

To find the equilibrium point, we solve for $\vec{E} = 0$. Since the charges are of the same sign, the equilibrium point must lie on the x-axis between the charges (where $-a < x < a$).

Setting the x-components equal:
$$\frac{k q}{(x+a)^2} = \frac{k (2q)}{(a-x)^2} \implies (a-x)^2 = 2(x+a)^2$$
Taking the square root:
$$a - x = \sqrt{2}(x + a) \implies x(\sqrt{2} + 1) = a(1 - \sqrt{2})$$
$$x = a \frac{1 - \sqrt{2}}{1 + \sqrt{2}} = a(3 - 2\sqrt{2}) \approx -0.1716a$$

---

### 3. Numerical Calculation
**Given:** $a = 0.2$ m, $y = 0.3$ m, $q = 2 \mu$C.
Using the $\vec{E}(0, y)$ formula derived in Part 1:
* $r = \sqrt{0.2^2 + 0.3^2} = \sqrt{0.13} \approx 0.3606$ m
* $E_x = \frac{k q a}{r^3} = \frac{(9 \times 10^9)(2 \times 10^{-6})(0.2)}{0.0468} \approx 76.9$ kN/C
* $E_y = \frac{3 k q y}{r^3} = \frac{3(9 \times 10^9)(2 \times 10^{-6})(0.3)}{0.0468} \approx 346.1$ kN/C

---

### 4. Far-Field Limit Investigation ($y \gg a$)

When the observation point is very far from the charges, the separation $a$ becomes negligible. The system should behave like a single point charge of magnitude $Q_{total} = 3q$.

Mathematically, as $y \to \infty$:
$$\vec{E}(0, y) \approx \frac{kq}{y^3} (a\hat{i} + 3y\hat{j}) \approx \frac{3kq}{y^2} \hat{j}$$
This confirms the **Monopole Approximation**: the field strength follows the inverse-square law $\frac{k(3q)}{y^2}$.

---

### 5. Does a Zero Field exist on the y-axis?

**No.**
Looking at the derived vector $\vec{E}(0, y) = \frac{k q}{r^3} (a\hat{i} + 3y\hat{j})$:
* The x-component is constant ($a$) relative to the sign of the charges.
* The y-component only vanishes at $y=0$ (on the x-axis).
* At the origin $(0,0)$, the field is $\vec{E}(0,0) = \frac{kq}{a^2} \hat{i}$, which is non-zero.
Therefore, no point on the y-axis can have a total field of zero.
