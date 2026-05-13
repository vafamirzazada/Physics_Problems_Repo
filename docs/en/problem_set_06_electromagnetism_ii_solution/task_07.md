# Problem 7: Magnetic Flux and Induction in a Moving Rectangular Loop

This task investigates the dynamics of a conducting loop as it enters a region of uniform magnetic field $\vec{B}$. We analyze the transition phases of induction, the resulting braking force, and verify the conservation of energy through a power balance.

---

### 1. Magnetic Flux $\Phi(t)$ in the Entering Phase

As the loop enters the field with velocity $v$, the "active" area $S(t)$ within the field increases linearly. Let $x(t) = vt$ be the distance the loop has traveled into the field.

$$\Phi(t) = B \cdot S(t) = B \cdot (a \cdot vt)$$

* **$a$:** The dimension of the loop perpendicular to the motion.
* **$vt$:** The length of the loop currently submerged in the magnetic field.

---

### 2. Induced EMF ($\mathcal{E}$) and Current ($I$)

According to **Faraday's Law**, the induced EMF is the negative rate of change of flux:
$$\mathcal{E} = -\frac{d\Phi}{dt} = -B \cdot a \cdot v$$

The magnitude of the induced current $I$ (flowing through resistance $R$) is:
$$I = \frac{|\mathcal{E}|}{R} = \frac{Bav}{R}$$

---

### 3. Determination of the Braking Force $F(v)$

As current flows through the leading edge of the loop (length $a$) inside the field, it experiences a magnetic Lorentz force. According to **Lenz's Law**, this force must oppose the motion:
$$F = I \cdot a \cdot B$$

Substituting the expression for $I$:
$$F(v) = \left( \frac{Bav}{R} \right) \cdot a \cdot B = \frac{B^2 a^2 v}{R}$$

This is a **braking force** that acts to slow the loop down. To maintain a constant velocity $v$, an equal and opposite external mechanical force must be applied.

---

### 4. Power Balance: Mechanical vs. Thermal

We verify energy conservation by comparing the mechanical work done per second to the heat dissipated.

* **Mechanical Power ($P_{mech}$):**
$$P_{mech} = F \cdot v = \left( \frac{B^2 a^2 v}{R} \right) \cdot v = \frac{B^2 a^2 v^2}{R}$$

* **Thermal Power (Joule Heating $P_{term}$):**
$$P_{term} = I^2 R = \left( \frac{Bav}{R} \right)^2 \cdot R = \frac{B^2 a^2 v^2}{R}$$

**Conclusion:** $P_{mech} = P_{term}$. This proves that 100% of the mechanical energy used to pull the loop is converted into thermal energy within the wire.

---

### 5. Loop Entirely in the Uniform Field

When the loop is fully submerged:
* The magnetic flux $\Phi = B \cdot (a \cdot b)$ becomes **constant**.
* Therefore, $\frac{d\Phi}{dt} = 0$.
* **Result:** The induced EMF and the current both drop to **zero**. There is no longer a braking force, and the loop moves freely without resistance (ignoring friction).
