# Problem 9: Electric Dipole in a Uniform External Field

This task examines the behavior of an electric dipole placed within a uniform external electric field $\mathbf{E_0}$. We derive its dynamics, energy states, and demonstrate how it acts as a harmonic oscillator under specific conditions.

---

### 1. Derivation of Torque acting on the Dipole

An electric dipole consists of two equal and opposite charges, $+q$ and $-q$, separated by a distance $d$. The dipole moment is defined as $\mathbf{p} = q\mathbf{d}$. 

When placed in a uniform field $\mathbf{E_0}$, the force on the positive charge is $\mathbf{F_+} = q\mathbf{E_0}$ and on the negative charge is $\mathbf{F_-} = -q\mathbf{E_0}$. While the net force is zero, these forces create a **torque** ($\boldsymbol{\tau}$) that attempts to align the dipole with the field:

$$\boldsymbol{\tau} = \mathbf{r_+} \times \mathbf{F_+} + \mathbf{r_-} \times \mathbf{F_-}$$

$$\boldsymbol{\tau} = \mathbf{p} \times \mathbf{E_0}$$

The magnitude of this torque is:
$$\tau = p E_0 \sin(\theta)$$

Where $\theta$ is the angle between the dipole moment $\mathbf{p}$ and the electric field $\mathbf{E_0}$.

---

### 2. Potential Energy of the Dipole

The work done by the external field to rotate the dipole is stored as electrostatic potential energy ($U$). We calculate this by integrating the torque over the angle of rotation:

$$U = \int \tau \, d\theta = \int p E_0 \sin(\theta) \, d\theta$$

$$U = -p E_0 \cos(\theta)$$

In vector notation, this is expressed as the dot product:
$$U = -\mathbf{p} \cdot \mathbf{E_0}$$

* **Stable Equilibrium:** $U = -pE_0$ (when $\theta = 0^\circ$, aligned with the field).
* **Unstable Equilibrium:** $U = +pE_0$ (when $\theta = 180^\circ$, anti-aligned).

---

### 3. Equation of Angular Motion

According to Newton's Second Law for rotation, the torque is equal to the product of the moment of inertia ($I$) and the angular acceleration ($\alpha$):

$$\tau = I \alpha = I \frac{d^2\theta}{dt^2}$$

The restoring torque acts to decrease the angle $\theta$, so we introduce a negative sign:
$$I \frac{d^2\theta}{dt^2} = -p E_0 \sin(\theta)$$

This is a non-linear second-order differential equation.

---

### 4. Linearization for Small Displacements

For very small angles ($\theta \approx 0$), we can use the **Small Angle Approximation**:
$$\sin(\theta) \approx \theta$$

Substituting this into our equation of motion gives us the linearized form:
$$I \frac{d^2\theta}{dt^2} + (p E_0) \theta = 0$$

$$\frac{d^2\theta}{dt^2} + \left( \frac{p E_0}{I} \right) \theta = 0$$

---

### 5. Interpretation as a Harmonic Oscillator

The linearized equation above is mathematically identical to the equation for a **Simple Harmonic Oscillator** ($\ddot{x} + \omega^2 x = 0$). 

By comparing the terms, we can identify the natural angular frequency ($\omega_0$) of the dipole's vibration:

$$\omega_0 = \sqrt{\frac{p E_0}{I}}$$

**Physical Conclusion:**
If a dipole is slightly nudged from its alignment with an external field, it will not simply return to its original position. Instead, it will oscillate back and forth around the field lines. This demonstrates that the alignment of a dipole is not just a static state, but a dynamic equilibrium governed by oscillatory physics.
