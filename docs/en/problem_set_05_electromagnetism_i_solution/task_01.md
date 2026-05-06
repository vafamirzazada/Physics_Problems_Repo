# Problem 1: Electrostatic Potential and Energy

This task investigates the fundamental relationship between a point charge, the potential it creates in space, and the work required to manipulate a test charge within that field. We also derive the electric field intensity using calculus and verify the results against Coulomb’s Law.

---

### 1. Calculation of Electric Potential ($V$)

The electric potential at a distance $r$ from a point charge $q$ is defined as the potential energy per unit charge. Using the vacuum permittivity $k \approx 8.99 \times 10^9 \, \text{N}\cdot\text{m}^2/\text{C}^2$:

$$V(r) = \frac{k q}{r}$$

**Given:** $q = 4 \, \mu\text{C} = 4 \times 10^{-6} \, \text{C}$ and $r = 0.3 \, \text{m}$

$$V(0.3) = \frac{8.99 \times 10^9 \cdot 4 \times 10^{-6}}{0.3} \approx 119,866.67 \, \text{V}$$

---

### 2. Potential Difference ($\Delta V$)

The potential difference between two points represents the change in potential energy per unit charge as one moves between those points.

**Points:** $r_1 = 0.3 \, \text{m}$ and $r_2 = 0.6 \, \text{m}$

$$\Delta V = V(r_2) - V(r_1) = k q \left( \frac{1}{r_2} - \frac{1}{r_1} \right)$$

$$V(0.6) = \frac{8.99 \times 10^9 \cdot 4 \times 10^{-6}}{0.6} \approx 59,933.33 \, \text{V}$$

$$\Delta V = 59,933.33 - 119,866.67 = -59,933.34 \, \text{V}$$

*Interpretation:* The negative result indicates that the potential decreases as we move away from a positive source charge.

---

### 3. Work Done ($W$) on a Test Charge

The work required to move a test charge $q_0$ between two points in an electrostatic field is equal to the product of the charge and the potential difference:

$$W = q_0 \cdot \Delta V$$

**Given:** $q_0 = 2 \, \mu\text{C} = 2 \times 10^{-6} \, \text{C}$

$$W = 2 \times 10^{-6} \cdot (-59,933.34) \approx -0.1199 \, \text{J}$$

*Analogy:* Moving the charge away from a like-sign charge is like a ball rolling down a hill; the field does the work, which is why the value is negative (from the perspective of an external agent).

---

### 4. Electric Field Intensity ($E$) from Potential

The electric field is the negative gradient (derivative) of the potential. In a radial system:

$$E(r) = -\frac{dV}{dr}$$

Differentiating $V(r) = \frac{k q}{r}$ with respect to $r$:

$$E(r) = -\frac{d}{dr} \left( k q r^{-1} \right) = -(-1) k q r^{-2} = \frac{k q}{r^2}$$

At $r = 0.3 \, \text{m}$:
$$E(0.3) = \frac{8.99 \times 10^9 \cdot 4 \times 10^{-6}}{(0.3)^2} \approx 399,555.56 \, \text{N/C}$$

---

### 5. Comparison with Coulomb's Law

Coulomb’s Law defines the force between two charges as $F = \frac{k q q_0}{r^2}$. Since $E$ is defined as force per unit charge ($E = F / q_0$), we have:

$$E_{Coulomb} = \frac{1}{q_0} \left( \frac{k q q_0}{r^2} \right) = \frac{k q}{r^2}$$

**Conclusion:** The derivative of the potential function yields the exact same formula as Coulomb's Law. This verification proves the mathematical consistency between the scalar field (Potential) and the vector field (Intensity).
