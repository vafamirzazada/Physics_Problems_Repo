# Problem 1: The Lorentz Force and Trajectory Analysis

This task explores the interaction between a moving point charge and a uniform magnetic field. We analyze the resulting force vector, investigate the energy properties of magnetic interactions, and derive the geometric parameters of the particle's trajectory.

---

### 1. Determination of the Lorentz Force Vector $\vec{F}$

The magnetic component of the Lorentz force is defined by the cross product of the velocity vector $\vec{v}$ and the magnetic field vector $\vec{B}$:

$$\vec{F} = q (\vec{v} \times \vec{B})$$

**Given Data:**
* $q = 1 \, \text{mC} = 10^{-3} \, \text{C}$
* $\vec{v} = (2, 3, 0) \, \text{m/s}$
* $\vec{B} = (0, 0, 1) \, \text{T}$

**Calculation:**
$$\vec{v} \times \vec{B} = \begin{vmatrix} \mathbf{\hat{i}} & \mathbf{\hat{j}} & \mathbf{\hat{k}} \\ 2 & 3 & 0 \\ 0 & 0 & 1 \end{vmatrix} = \mathbf{\hat{i}}(3 \cdot 1 - 0) - \mathbf{\hat{j}}(2 \cdot 1 - 0) + \mathbf{\hat{k}}(0) = (3, -2, 0)$$

$$\vec{F} = 10^{-3} \cdot (3, -2, 0) = (0.003, -0.002, 0) \, \text{N}$$

---

### 2. Equation of Motion and Trajectory

According to Newton’s Second Law, $\vec{F} = m\vec{a}$. For a constant magnetic field perpendicular to the velocity, the particle undergoes **Uniform Circular Motion** in the $xy$-plane.

Assuming initial position $(0, 0, 0)$ at $t=0$, the parametric equations of motion are:
* $x(t) = R \sin(\omega t)$
* $y(t) = R \cos(\omega t)$
where $\omega = \frac{qB}{m}$ is the cyclotron frequency.

---

### 3. Magnitude of the Force $|\vec{F}|$

The magnitude can be calculated from the vector components:
$$|\vec{F}| = \sqrt{0.003^2 + (-0.002)^2} = \sqrt{9 \times 10^{-6} + 4 \times 10^{-6}} = \sqrt{13 \times 10^{-6}}$$
$$|\vec{F}| \approx 3.61 \times 10^{-3} \, \text{N} = 3.61 \, \text{mN}$$

Alternatively, using $|\vec{F}| = qvB\sin(\theta)$ where $v = \sqrt{2^2 + 3^2} = \sqrt{13}$:
$$|\vec{F}| = 10^{-3} \cdot \sqrt{13} \cdot 1 \cdot \sin(90^\circ) \approx 3.61 \, \text{mN}$$

---

### 4. Does the Magnetic Force do work?

**No.** The magnetic force is always perpendicular to the velocity vector ($\vec{F} \perp \vec{v}$). 
The power $P$ delivered by the force is:
$$P = \vec{F} \cdot \vec{v} = q(\vec{v} \times \vec{B}) \cdot \vec{v}$$
Since the dot product of a vector and its own cross product is always zero, **the magnetic force changes only the direction of motion, never the speed or kinetic energy.**

---

### 5. Radius of the Trajectory ($m = 0.01 \, \text{kg}$)

The centripetal force is provided by the Lorentz force:
$$\frac{mv^2}{r} = qvB \implies r = \frac{mv}{qB}$$

**Calculation:**
$$r = \frac{0.01 \cdot \sqrt{13}}{10^{-3} \cdot 1} = 10 \cdot \sqrt{13} \approx 36.06 \, \text{m}$$

---

### 6. Impact of Doubling the Magnetic Field ($B$)

From the derived formula $r = \frac{mv}{qB}$, we see that the radius $r$ is **inversely proportional** to the magnetic field strength $B$ ($r \propto 1/B$).

**Conclusion:** If the value of $B$ is doubled, the radius of the trajectory will be **halved** ($r_{new} = \frac{1}{2}r_{old}$). The particle will turn more sharply due to the increased force.
