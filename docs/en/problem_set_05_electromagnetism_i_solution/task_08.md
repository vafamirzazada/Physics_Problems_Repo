# Problem 8: Energy of a Three-Charge System

This task focuses on the electrostatic potential energy of a discrete system of point charges. We explore how geometric configuration and charge signs dictate the total energy and stability of the system.

---

### 1. Total Energy of the System

The total electrostatic potential energy ($U$) of a system of point charges is the work required to assemble the configuration by bringing each charge from infinity to its final position. For a three-charge system ($q_1, q_2, q_3$), this energy is the sum of the potential energies of all unique pairs:

$$U = U_{12} + U_{13} + U_{23}$$

Applying Coulomb's Law, the formula becomes:

$$U = \frac{1}{4\pi\varepsilon_0} \left( \frac{q_1 q_2}{r_{12}} + \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)$$

* **$r_{ij}$:** The distance between charge $i$ and charge $j$.
* **$\varepsilon_0$:** The vacuum permittivity.

---

### 2. Energy for an Equilateral Triangle Configuration

In an equilateral triangle configuration, all charges are separated by the same distance $a$ ($r_{12} = r_{13} = r_{23} = a$). If we assume all charges are identical ($q_1 = q_2 = q_3 = q$), the formula simplifies to:

$$U = \frac{1}{4\pi\varepsilon_0} \left( \frac{q^2}{a} + \frac{q^2}{a} + \frac{q^2}{a} \right)$$

$$U = \frac{3q^2}{4\pi\varepsilon_0 a}$$

This configuration represents a high-energy state if all charges have the same sign, as they all experience mutual repulsion.

---

### 3. Investigation of Charge Sign Reversal

Changing the sign of one charge (e.g., $q_3 \to -q$) fundamentally alters the nature of the interactions:

* **Original (all positive):** All three terms in the sum are positive (repulsive). Total energy $U > 0$.
* **Modified (two positive, one negative):** The terms involving the negative charge become negative (attractive).

$$U_{new} = \frac{1}{4\pi\varepsilon_0} \left( \frac{q_1 q_2}{r_{12}} - \frac{q_1 q_3}{r_{13}} - \frac{q_2 q_3}{r_{23}} \right)$$

Depending on the distances, the total energy can become negative, indicating that the system is now bound by attractive forces.

---

### 4. Numerical Search for Minimum Energy Configuration

To find the minimum energy configuration numerically, we implement an optimization algorithm (such as a gradient descent or a simple grid search) that varies the coordinates $(x_i, y_i)$ of the charges.

* **Objective Function:** Minimize $U(\mathbf{r}_1, \mathbf{r}_2, \mathbf{r}_3)$.
* **Constraints:** We often fix one charge at the origin $(0,0)$ and another along the x-axis to remove rotational and translational degrees of freedom.
* **Observation:** For three identical charges, the minimum energy configuration is simply increasing the distance $r_{ij}$ to infinity. However, if charges are constrained within a boundary, they will seek the most symmetric distribution possible to minimize repulsion.

---

### 5. Interpretation of System Stability

The stability of the system is determined by the "Energy Landscape":

* **Repulsive Systems (Same Signs):** These systems are inherently unstable. Without external constraints, the charges will accelerate away from each other to reach a state of zero energy at infinite separation.
* **Mixed Systems (Opposite Signs):** These can form stable or meta-stable "bound states." A local minimum in the potential energy function indicates a stable equilibrium point where any small displacement results in a restoring force.
* **Stability Criterion:** A configuration is stable if it sits at a minimum of the total potential energy ($dU = 0$ and $d^2U > 0$).
