# Problem 5: Capacitor Energy and Force Analysis

This task explores the physical properties of a parallel-plate capacitor. We analyze how electrical energy is stored within an electric field and calculate the mechanical force resulting from the attraction between opposite charges on the plates.

---

### 1. Parameters of the System
We are given a parallel-plate capacitor with the following characteristics:
* **Surface Area ($S$):** $0.02 \, \text{m}^2$
* **Distance ($d$):** $5 \, \text{mm} = 0.005 \, \text{m}$
* **Voltage ($U$):** $500 \, \text{V}$
* **Vacuum Permittivity ($\varepsilon_0$):** $\approx 8.854 \times 10^{-12} \, \text{F/m}$

---

### 2. Analytical Derivations

#### **A. Capacitance ($C$)**
Capacitance represents the ability of the system to store charge per unit of potential. For a parallel-plate geometry:
$$C = \varepsilon_0 \frac{S}{d}$$

#### **B. Energy Stored ($W$)**
The work done to move charges onto the plates is stored as potential energy in the electric field:
$$W = \frac{1}{2} C U^2$$

#### **C. Electric Field Intensity ($E$)**
The field strength is the potential gradient between the plates. In a uniform field:
$$E = \frac{U}{d}$$

#### **D. Field Energy Density ($w$)**
Energy density is the amount of energy stored per unit volume ($V = S \cdot d$):
$$w = \frac{W}{S \cdot d} = \frac{1}{2} \varepsilon_0 E^2$$

#### **E. Force of Attraction ($F$)**
Because the plates carry opposite charges, they exert a mechanical force on each other. This can be derived from the change in energy relative to the distance:
$$F = \frac{W}{d} = \frac{1}{2} Q E = \frac{\varepsilon_0 S U^2}{2 d^2}$$

---

### 3. Physical Interpretation
* **Energy Storage:** This system proves that energy does not just exist "on the wires," but is actually stored in the **space (vacuum)** between the plates via the electric field.
* **Force Balance:** The calculated force represents the external mechanical tension required to keep the plates from snapping together.
* **Analogy:** Think of a capacitor like a **mechanical spring**. Increasing the voltage is like stretching the spring; the "capacitance" is the spring constant, determining how much energy is stored for every "centimeter" of electrical stretch.
