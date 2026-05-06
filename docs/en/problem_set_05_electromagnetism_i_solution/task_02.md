# Problem 2: Coulomb's Force and Electrostatic Energy

This task examines the fundamental interaction between two static point charges. We calculate the force vector, determine the magnitude of attraction, and analyze the energy required to change the configuration of the system.

---

### 1. Physical Parameters and Setup

The system consists of two point charges:
* **Charge 1 ($q_1$):** $3 \, \mu\text{C} = 3 \times 10^{-6} \, \text{C}$ at $\vec{r}_1 = (0, 0)$
* **Charge 2 ($q_2$):** $-5 \, \mu\text{C} = -5 \times 10^{-6} \, \text{C}$ at $\vec{r}_2 = (0.4, 0.3) \, \text{m}$

**Distance Vector ($\vec{r}$):**
$$\vec{r} = \vec{r}_2 - \vec{r}_1 = (0.4, 0.3) \, \text{m}$$

**Scalar Distance ($r$):**
$$r = \sqrt{0.4^2 + 0.3^2} = \sqrt{0.16 + 0.09} = 0.5 \, \text{m}$$

---

### 2. Force Vector Acting on $q_2$

According to **Coulomb's Law**, the force vector $\vec{F}$ is given by:
$$\vec{F} = k \frac{q_1 q_2}{r^2} \hat{r} = k \frac{q_1 q_2}{r^3} \vec{r}$$

Using $k \approx 8.99 \times 10^9 \, \text{N}\cdot\text{m}^2/\text{C}^2$:
$$\vec{F} = (8.99 \times 10^9) \frac{(3 \times 10^{-6})(-5 \times 10^{-6})}{0.5^3} (0.4, 0.3)$$
$$\vec{F} = \frac{-0.13485}{0.125} (0.4, 0.3) = -1.0788 (0.4, 0.3)$$
$$\vec{F} \approx (-0.432, -0.324) \, \text{N}$$

*The negative sign indicates an **attractive force**, pulling $q_2$ toward the origin.*

---

### 3. Force Magnitude

The magnitude of the force ($F$) is calculated as:
$$F = |\vec{F}| = \sqrt{(-0.432)^2 + (-0.324)^2} = 0.54 \, \text{N}$$

---

### 4. Potential Energy of the System ($U$)

The electrostatic potential energy of the pair is defined as:
$$U = k \frac{q_1 q_2}{r}$$
$$U = (8.99 \times 10^9) \frac{(3 \times 10^{-6})(-5 \times 10^{-6})}{0.5}$$
$$U = \frac{-0.13485}{0.5} = -0.2697 \, \text{J}$$

---

### 5. Work Required to Separate Charges ($W$)

To separate the charges from an initial distance $r_i = 0.5 \, \text{m}$ to a final distance $r_f = 2 \, \text{m}$, we calculate the change in potential energy:
$$W = \Delta U = U_f - U_i$$

**Final Potential Energy ($U_f$):**
$$U_f = k \frac{q_1 q_2}{2.0} = \frac{-0.13485}{2.0} = -0.067425 \, \text{J}$$

**Work ($W$):**
$$W = -0.067425 - (-0.2697) = 0.202275 \, \text{J}$$

*Since $W > 0$, external work must be performed to overcome the attractive force and pull the charges apart.*
