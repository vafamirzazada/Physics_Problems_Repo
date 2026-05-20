# Problem 3: Voltage and Current Distribution Analysis

This task examines the electrical behavior of a mixed series-parallel resistor network connected to a constant DC voltage source ($U = 200\text{ V}$). We calculate the total network resistance, determine the main line current, and analyze the current distribution through a specific parallel branch monitored by an ideal ammeter.

---

### 1. System Parameters and Schematic Constants

The circuit network is defined by the following electrical properties:
* **Source Voltage ($U$):** $200\text{ V}$
* **Resistor 1 ($R_1$):** $20\ \Omega$
* **Resistor 2 ($R_2$):** $60\ \Omega$
* **Resistor 3 ($R_3$):** $30\ \Omega$
* **Resistor 4 ($R_4$):** $10\ \Omega$
* **Ammeter ($A$):** Ideal (internal resistance $R_A = 0\ \Omega$)

---

### 2. Step-by-Step Analytical Derivations

#### **Step A: Total Equivalent Resistance ($R_{eq}$)**
To determine the total resistance of the network, we collapse the parallel loop formed by $R_2$ and $R_3$ first:

$$R_{parallel} = \frac{R_2 \cdot R_3}{R_2 + R_3} = \frac{60 \cdot 30}{60 + 30} = \frac{1800}{90} = 20\ \Omega$$

This parallel sub-block is in series with the input resistor $R_1$ and output resistor $R_4$. The total equivalent resistance of the entire loop is:

$$R_{eq} = R_1 + R_{parallel} + R_4 = 20\ \Omega + 20\ \Omega + 10\ \Omega = 50\ \Omega$$

#### **Step B: Total Line Current ($I_{total}$)**
Using Ohm's Law for the entire closed system, we calculate the main line current leaving the positive terminal of the power supply:

$$I_{total} = \frac{U}{R_{eq}} = \frac{200\text{ V}}{50\ \Omega} = 4\text{ A}$$

#### **Step C: Parallel Node Voltage Drop ($U_3$)**
As the main $4\text{ A}$ current stream enters the parallel junction, we find the voltage drop across this shared node using the node's total equivalent resistance:

$$U_3 = I_{total} \cdot R_{parallel} = 4\text{ A} \cdot 20\ \Omega = 80\text{ V}$$

*Because parallel branches span the exact same node pairs, both $R_2$ and $R_3$ experience this identical potential drop of $80\text{ V}$.*

#### **Step D: Individual Branch Current and Ammeter Readout ($I_3$)**
Applying Ohm's Law specifically to the $R_3$ branch, we find the localized current flowing through the ammeter:

$$I_3 = \frac{U_3}{R_3} = \frac{80\text{ V}}{30\ \Omega} = \frac{8}{3}\text{ A} \approx 2.67\text{ A}$$

---

### 3. Verification and Conservation of Charge

To validate the calculations, we verify the remaining current splitting through the upper branch containing $R_2$:

$$I_2 = \frac{U_3}{R_2} = \frac{80\text{ V}}{60\ \Omega} = \frac{4}{3}\text{ A} \approx 1.33\text{ A}$$

According to **Kirchhoff's Current Law (KCL)**, the sum of currents entering a junction must equal the sum of currents leaving it:

$$I_{junction} = I_2 + I_3 = 1.33\text{ A} + 2.67\text{ A} = 4.00\text{ A} = I_{total}$$

**Physical Conclusion:** Since $R_3$ contains exactly half the electrical resistance of $R_2$, it naturally draws exactly twice the current flow ($2.67\text{ A}$ vs $1.33\text{ A}$). The network exhibits perfect mathematical symmetry and complies with the law of conservation of charge.
