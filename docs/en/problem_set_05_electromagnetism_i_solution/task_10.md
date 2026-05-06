# Problem 10: Electric Field Flux and Verification of Gauss's Law

In this task, we transition from circuit dynamics to the fundamental principles of electromagnetism. We investigate the concept of electric flux and perform a numerical verification of Gauss's Law by calculating the flux of a point charge through a surrounding spherical surface.

---

### 1. Definition of Electric Field Flux

Electric flux ($\Phi_E$) is a measure of the "flow" of the electric field through a given surface. Mathematically, for a surface $S$, it is defined as the surface integral of the electric field $\mathbf{E}$ over that surface:

$$\Phi_E = \iint_S \mathbf{E} \cdot d\mathbf{A}$$

* **$\mathbf{E}$:** The electric field vector.
* **$d\mathbf{A}$:** The vector area element, pointing normal (perpendicular) to the surface.
* **Physical Analogy:** Much like water flowing through a pipe, the flux represents the total number of electric field lines passing through the "door" of our chosen surface.

---

### 2. Theoretical Case: Sphere Around a Point Charge

According to **Coulomb's Law**, the electric field $\mathbf{E}$ created by a point charge $q$ at a distance $r$ is:

$$\mathbf{E} = \frac{1}{4\pi\varepsilon_0} \frac{q}{r^2} \mathbf{\hat{r}}$$

When we place this charge at the center of a sphere of radius $R$, the electric field is always parallel to the area vector $d\mathbf{A}$ (since both point radially outward). Thus, the dot product $\mathbf{E} \cdot d\mathbf{A}$ simplifies to $E \cdot dA$.

By **Gauss's Law**, the total flux through any closed surface is simply:

$$\Phi_{total} = \frac{q_{enclosed}}{\varepsilon_0}$$

---

### 3. Numerical Strategy: Discrete Approximation

To verify this numerically, we cannot perform an infinite integral. Instead, we divide the sphere's surface into $N$ discrete patches. The total flux is approximated by the sum:

$$\Phi_E \approx \sum_{i=1}^{N} \mathbf{E}_i \cdot \Delta\mathbf{A}_i$$

We use spherical coordinates $(\theta, \phi)$ to generate grid points on the sphere:
* $\theta \in [0, \pi]$ (latitude)
* $\phi \in [0, 2\pi]$ (longitude)

The area element for each patch is calculated as:
$$\Delta A = R^2 \sin(\theta) \Delta\theta \Delta\phi$$

---

### 4. Implementation and Convergence Analysis

A critical part of this task is investigating the **dependence on the number of grid points ($N$)**. 

* **Numerical Error:** With a low number of points, the "curved" sphere is represented by flat tiles, leading to an approximation error.
* **Convergence:** As $N$ increases, the discrete sum approaches the analytical value of $q/\varepsilon_0$. 
* **Observation:** This numerical verification proves that our algorithmic approach to field theory is robust and matches the high-level calculus derived by Gauss.

---

### 5. Comparison: Analytical vs. Numerical Result

| Feature | Analytical (Gauss's Law) | Numerical (Discrete Sum) |
| :--- | :--- | :--- |
| **Formula** | $\Phi = q/\varepsilon_0$ | $\Phi = \sum E \Delta A$ |
| **Complexity** | Instant calculation | Computationally heavy as $N \to \infty$ |
| **Accuracy** | Exact | Approximates exactness with density |
| **Flexibility** | Limited to symmetric shapes | Can calculate flux for any arbitrary geometry |
