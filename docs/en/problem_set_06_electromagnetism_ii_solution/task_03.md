# Problem 3: Magnetic Moment and Torque on a Conducting Loop

This task investigates the interaction between a current-carrying loop and an external uniform magnetic field $\vec{B}$. We define the magnetic properties of the loop and analyze the mechanical consequences, specifically the torque and potential energy that drive rotational motion.

---

### 1. Definition of the Magnetic Moment $\vec{\mu}$

For a conducting loop with $N$ turns, a surface area $S$, and a current $I$ flowing through it, the **magnetic dipole moment** $\vec{\mu}$ is a vector that represents the strength and orientation of the loop's magnetic field.

It is defined as:
$$\vec{\mu} = N I \vec{S}$$

* **Magnitude:** $|\mu| = NIS$
* **Direction:** Perpendicular to the plane of the loop, determined by the **Right-Hand Rule** (curl your fingers in the direction of the current; your thumb points in the direction of $\vec{\mu}$).

---

### 2. Determination of the Torque $\vec{M}$

When the loop is placed in a uniform magnetic field $\vec{B}$, the magnetic forces acting on the sides of the loop create a **torque** (rotational force). This torque is mathematically expressed as the cross product of the magnetic moment and the magnetic field:

$$\vec{M} = \vec{\mu} \times \vec{B}$$

The magnitude of the torque is:
$$M = \mu B \sin(\theta)$$

Where $\theta$ is the angle between the magnetic moment vector $\vec{\mu}$ (normal to the loop) and the magnetic field vector $\vec{B}$.

---

### 3. Maximum Torque Condition

The torque magnitude follows a sine relationship: $M \propto \sin(\theta)$.

* **Maximum Torque ($M_{max} = \mu B$):** Occurs when $\sin(\theta) = 1$, which means **$\theta = 90^\circ$ (or $\pi/2$ radians)**.
* **Physical Interpretation:** Torque is highest when the plane of the loop is **parallel** to the magnetic field lines. In this position, the magnetic moment is perpendicular to the field.

---

### 4. Determination of Potential Energy $U$

The work required to rotate the magnetic dipole against the magnetic field is stored as electrostatic potential energy. It is defined as the negative dot product of the magnetic moment and the field:

$$U = -\vec{\mu} \cdot \vec{B}$$

$$U = -\mu B \cos(\theta)$$

---

### 5. Stable and Unstable Positions

The stability of the loop is determined by the "Energy Landscape." Nature always seeks the state of lowest potential energy.

* **Stable Equilibrium:** Occurs at **$\theta = 0^\circ$**.
    * $U = -\mu B$ (Minimum energy).
    * $\vec{\mu}$ and $\vec{B}$ are perfectly aligned (pointing in the same direction). If nudged, the loop will return to this alignment.
* **Unstable Equilibrium:** Occurs at **$\theta = 180^\circ$**.
    * $U = +\mu B$ (Maximum energy).
    * $\vec{\mu}$ and $\vec{B}$ are anti-aligned (opposite directions). In this position, the net torque is zero, but any tiny displacement will cause the loop to flip violently toward the stable $0^\circ$ position.
