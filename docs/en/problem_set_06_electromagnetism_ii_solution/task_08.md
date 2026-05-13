# Problem 8: Self-Induction and Energy Decay in an RL Circuit

This task investigates the behavior of a coil (inductor) in a DC circuit. We analyze the steady-state conditions, the exponential decay of current upon disconnection, and the conversion of stored magnetic energy into thermal energy.

---

### 1. Steady Current $I_0$ Before Disconnection

In a DC circuit, after a "long time," an inductor acts as a simple wire with zero resistance (ideally). The current is limited only by the resistor $R$.

**Given Data:**
* $U = 12 \, \text{V}$
* $R = 5.0 \, \Omega$
* $L = 0.20 \, \text{H}$

**Calculation:**
$$I_0 = \frac{U}{R} = \frac{12}{5.0} = 2.4 \, \text{A}$$

---

### 2. Post-Disconnection: Current and Voltage Dynamics

When the power supply is removed at $t = 0$, the inductor uses its stored magnetic field to maintain the current, which then decays through the resistor.

* **Time Constant ($\tau$):** Defines the speed of decay.
$$\tau = \frac{L}{R} = \frac{0.20}{5.0} = 0.04 \, \text{s}$$

* **Current Decay $I(t)$:**
$$I(t) = I_0 e^{-t/\tau} = 2.4 e^{-25t} \, \text{A}$$

* **Voltage Across the Coil $U_L(t)$:**
According to Ohm's Law for the remaining circuit ($U_L = I \cdot R$):
$$U_L(t) = I(t) \cdot R = 12 e^{-25t} \, \text{V}$$

---

### 3. Stored Magnetic Energy

The energy $W$ stored in the magnetic field of the coil during the steady state is:
$$W = \frac{1}{2} L I_0^2$$

**Calculation:**
$$W = \frac{1}{2} \cdot 0.20 \cdot (2.4)^2 = 0.1 \cdot 5.76 = 0.576 \, \text{J}$$

---

### 4. Conversion to Joule Heat

As the current decays, the energy stored in the magnetic field is "leaked" into the resistor and converted into heat. We verify this by integrating the instantaneous power ($P = I^2 R$) over all time:

$$W_{heat} = \int_{0}^{\infty} I(t)^2 R \, dt = R \int_{0}^{\infty} (I_0 e^{-R/L t})^2 \, dt$$
$$W_{heat} = R I_0^2 \left[ \frac{-L}{2R} e^{-2R/L t} \right]_{0}^{\infty} = \frac{1}{2} L I_0^2$$

**Conclusion:** The integral perfectly matches the initial stored energy ($0.576 \, \text{J}$), proving that 100% of the magnetic energy is converted into heat.

---

### 5. The Phenomenon of Overvoltage

When a circuit with high inductance is suddenly broken (disconnected), the rate of change of current ($dI/dt$) is extremely high (the current tries to drop to zero instantly). 

According to the formula for self-induced EMF:
$$\mathcal{E} = -L \frac{dI}{dt}$$

Because $dt$ is nearly zero during a mechanical disconnection, $\mathcal{E}$ can reach thousands of volts, far exceeding the original battery voltage ($12 \, \text{V}$). This **overvoltage** is what causes the air to ionize, resulting in a visible **spark** at the switch.
