# Problem 6: Magnetic Braking - Rod on Inclined Rails

This task investigates the complex interplay between gravitational potential energy and electromagnetic induction. We analyze a conducting rod sliding down inclined rails in a uniform magnetic field, leading to the phenomenon of magnetic damping and terminal velocity.

---

### 1. Motional EMF $\mathcal{E}(v)$ and Current $I(v)$

As the rod slides with velocity $v$, it cuts the magnetic field lines, inducing an EMF.
$$\mathcal{E} = B L v \cos(\alpha)$$
*Note: Since the field is perpendicular to the plane of the rails, $\mathcal{E} = BLv$.*

The induced current $I$ flows through the closed circuit of resistance $R$:
$$I = \frac{\mathcal{E}}{R} = \frac{BLv}{R}$$

---

### 2. Magnetic Braking Force

According to **Lenz's Law**, the induced current creates its own magnetic field that opposes the change in flux. The rod experiences a Lorentz force $\vec{F}_B = I(\vec{L} \times \vec{B})$.
The magnitude of this braking force is:
$$F_B = BIL = B \left( \frac{BLv}{R} \right) L = \frac{B^2 L^2 v}{R}$$

This force points **up the incline**, directly opposing the motion.

---

### 3. Equation of Motion

Applying Newton's Second Law along the incline:
$$\sum F = ma \implies mg \sin(\alpha) - F_B = m \frac{dv}{dt}$$

Substituting the expression for $F_B$:
$$m \frac{dv}{dt} + \left( \frac{B^2 L^2}{R} \right) v = mg \sin(\alpha)$$

**Interpretation:** This is a differential equation with "damping proportional to $v$." It is mathematically identical to an object falling through a viscous fluid (air resistance).

---

### 4. Terminal Velocity $v_\infty$

Terminal velocity is reached when the acceleration becomes zero ($dv/dt = 0$). At this point, the gravitational pull equals the magnetic braking force:
$$\frac{B^2 L^2 v_\infty}{R} = mg \sin(\alpha)$$

Solving for $v_\infty$:
$$v_\infty = \frac{mg R \sin(\alpha)}{B^2 L^2}$$

**Numerical Calculation ($m=0.20, L=0.30, B=0.80, R=0.50, \alpha=25^\circ$):**
$$v_\infty = \frac{0.20 \cdot 9.81 \cdot 0.50 \cdot \sin(25^\circ)}{0.80^2 \cdot 0.30^2} \approx \frac{0.4146}{0.0576} \approx 7.20 \, \text{m/s}$$

---

### 5. Power Balance and Steady State

In the steady state, the mechanical power $P_{mech}$ provided by gravity must equal the electrical power $P_{elec}$ dissipated as heat (Joule heating).

* **Mechanical Power:** $P_{mech} = F_g \cdot v = (mg \sin \alpha) \cdot v$
* **Electrical Power:** $P_{elec} = I^2 R$

By substituting $mg \sin \alpha = \frac{B^2 L^2 v}{R}$ and $I = \frac{BLv}{R}$ into the equation:
$$(mg \sin \alpha) \cdot v = \left( \frac{B^2 L^2 v}{R} \right) v = \frac{B^2 L^2 v^2}{R} = I^2 R$$

**Conclusion:** $mg \sin \alpha \cdot v = I^2 R$ 
This proves that 100% of the gravitational potential energy lost per second is being converted into heat within the circuit's resistance. The magnetic field acts as the "transmission" that enables this energy conversion.
