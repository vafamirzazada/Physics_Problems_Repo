# Problem 5: Superposition and the Phenomenon of Beats

This task explores how two harmonic waves with slightly different frequencies interfere to create a "beat" pattern.

---

### 1. Mathematical Derivation
Given two waves:
$$y_1 = A \sin(kx - \omega t)$$
$$y_2 = A \sin(kx - (\omega + \Delta\omega)t)$$

Using the sum-to-product trigonometric identity, the resultant wave is:
$$y = 2A \cos\left(\frac{\Delta\omega}{2}t\right) \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$$

### 2. Physical Interpretation
* **The Carrier:** The $\sin$ term represents the high-frequency average wave.
* [cite_start]**The Envelope:** The $\cos$ term represents the slow-moving amplitude modulation[cite: 61].
* **Beat Frequency:** The "beat" occurs twice per cycle of the envelope, meaning $f_{beat} = |\Delta f|$.

---

### 3. Numerical Simulation
[cite_start]I implemented a JS/HTML visualizer to show this interference in real-time[cite: 62]. By adjusting $\Delta\omega$, we can observe the "pinching" effect where the waves cancel each other out (destructive interference) and where they reinforce each other (constructive interference).
