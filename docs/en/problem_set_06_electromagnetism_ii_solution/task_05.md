# Problem 5: Motional EMF in a Moving Conducting Rod

This task examines the phenomenon of electromagnetic induction in a straight conductor moving through a uniform magnetic field. We derive the induced Electromotive Force (EMF), analyze the potential difference across the rod, and investigate the energy transformations involved.

---

### 1. Determination of Induced EMF ($\mathcal{E}$)

When a conductor moves through a magnetic field, the free charges within it experience a Lorentz force ($F = qvB$), which pushes them toward the ends of the rod. This separation of charge creates an induced EMF.

**Formula for Motional EMF:**
$$\mathcal{E} = B \cdot L \cdot v$$

**Given Data:**
* $B = 0.6 \, \text{T}$
* $L = 0.25 \, \text{m}$
* $v = 4 \, \text{m/s}$

**Calculation:**
$$\mathcal{E} = 0.6 \cdot 0.25 \cdot 4 = 0.6 \, \text{V}$$

---

### 2. Potential Difference Between the Ends

In a steady state, the separation of charges creates an internal electric field that eventually balances the magnetic force. The potential difference ($\Delta V$) between the ends of the rod is exactly equal to the induced EMF:
$$\Delta V = \mathcal{E} = 0.6 \, \text{V}$$

One end of the rod becomes positively charged, while the other becomes negatively charged (determined by the Right-Hand Rule).

---

### 3. Non-Perpendicular Motion

If the velocity $\vec{v}$ is not perpendicular to the magnetic field $\vec{B}$, only the component of velocity perpendicular to the field lines contributes to the induction.

The general formula becomes:
$$\mathcal{E} = B L v \sin(\phi)$$

where $\phi$ is the angle between $\vec{v}$ and $\vec{B}$.
* **If $\phi = 0^\circ$ (Parallel):** No EMF is induced because the rod does not "cut" any magnetic field lines.
* **If $\phi = 90^\circ$ (Perpendicular):** EMF is maximized.

---

### 4. Dependence of $\mathcal{E}$ on Length ($L$)

The induced EMF is **linearly proportional** to the length of the rod ($\mathcal{E} \propto L$).
* **Physical Interpretation:** A longer rod "collects" more magnetic flux as it moves and provides a longer path for charge separation. Doubling the length of the rod would double the induced voltage.

---

### 5. Source of Energy

A common misconception is that the energy comes from the magnetic field. However, **the magnetic field does no work.**

The energy of the electric field in the rod comes from the **mechanical work** performed by the external agent moving the rod. 
* As charges separate, they create a current (if the circuit is closed).
* This current in a magnetic field creates a counter-force (Lenz's Law).
* The agent must push against this force, and that mechanical energy is converted into electrical potential energy.

**Conclusion:** This is a pure transformation of mechanical energy into electrical energy.
