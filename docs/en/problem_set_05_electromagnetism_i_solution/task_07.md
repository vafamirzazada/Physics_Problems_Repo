# Problem 7: Motion in a Central Electric Field

This task explores the dynamics of a charged particle moving within a central electric field. This system is a fundamental model for understanding orbital mechanics and subatomic interactions, specifically demonstrating the parallels between electrostatic and gravitational forces.

---

### 1. The Equation of Motion

A particle with mass $m$ and charge $q$ is placed in a central field $\mathbf{E}(r) = k \frac{Q}{r^2} \mathbf{\hat{r}}$. According to Newton's Second Law and the Lorentz force law, the equation of motion is:

$$m \frac{d^2\mathbf{r}}{dt^2} = q \mathbf{E}(r)$$

Substituting the field expression:
$$m \frac{d^2\mathbf{r}}{dt^2} = \frac{k q Q}{r^2} \mathbf{\hat{r}}$$

* **Attractive Force:** If $q$ and $Q$ have opposite signs, the force is directed toward the center.
* **Repulsive Force:** If $q$ and $Q$ have the same sign, the force is directed away from the center.

---

### 2. Radial Motion

In the specific case of **radial motion**, the particle moves along a straight line passing through the center (angular momentum $L = 0$). The vector equation simplifies to a scalar second-order ODE for the radial distance $r$:

$$m \frac{d^2r}{dt^2} = \frac{k q Q}{r^2}$$

This describes a particle either falling directly toward the source or being "shot" directly away from it.

---

### 3. Numerical Strategy: Runge-Kutta (RK4)

Since the force is non-linear (proportional to $1/r^2$), we solve the system numerically. We convert the second-order ODE into two first-order ODEs:

1. $\frac{dr}{dt} = v$
2. $\frac{dv}{dt} = \frac{k q Q}{m r^2}$

We implement the **4th Order Runge-Kutta (RK4)** method. This is essential for central field problems because it maintains high precision during "close encounters" where the distance $r$ is small and the acceleration changes rapidly.

---

### 4. Energy States: Positive vs. Negative Energy

The total mechanical energy $E$ of the system is the sum of kinetic and potential energy:
$$E = \frac{1}{2}mv^2 - \frac{k q Q}{r}$$

* **Negative Energy ($E < 0$):** The particle is "bound." It cannot escape the field and will move in a closed elliptical orbit (under attractive forces).
* **Positive Energy ($E > 0$):** The particle is "unbound." It has enough speed to escape to infinity, resulting in a hyperbolic trajectory.
* **Zero Energy ($E = 0$):** The boundary case representing a parabolic escape trajectory.

---

### 5. Gravitational Analogy

The motion of a charge in a $1/r^2$ electric field is mathematically isomorphic to **Keplerian planetary motion**. 

| Feature | Electrostatic (Coulomb) | Gravitational (Newton) |
| :--- | :--- | :--- |
| **Force Law** | $F = k \frac{qQ}{r^2}$ | $F = G \frac{mM}{r^2}$ |
| **Potential** | $V \propto 1/r$ | $V \propto 1/r$ |
| **Trajectories** | Conic sections (Circle, Ellipse, Hyperbola) | Conic sections (Circle, Ellipse, Hyperbola) |

The primary difference is that gravity is strictly attractive, whereas the central electric field can be repulsive, leading to "scattering" trajectories where the particle is deflected rather than captured.
