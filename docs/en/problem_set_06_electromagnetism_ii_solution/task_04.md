# Problem 4: Electromagnetic Induction in a Rotating Loop

This task explores Faraday's Law of Induction applied to a conducting loop rotating within a uniform magnetic field. We derive the time-dependent magnetic flux, the resulting Electromotive Force (EMF), and analyze the relationship between rotational speed and power generation.

---

### 1. Determination of Magnetic Flux $\Phi(t)$

Magnetic flux $\Phi$ is the measure of the magnetic field $\vec{B}$ passing through the area $S$ of the loop. For a loop with $N$ turns rotating with angular velocity $\omega$:

$$\Phi(t) = N \vec{B} \cdot \vec{S} = N B S \cos(\theta)$$

Since the loop rotates at a constant rate, the angle $\theta$ changes with time as $\theta = \omega t$. Therefore:
$$\Phi(t) = N B S \cos(\omega t)$$

---

### 2. Determination of Induced EMF $\mathcal{E}(t)$

According to **Faraday's Law**, the induced Electromotive Force (EMF) is equal to the negative rate of change of the magnetic flux:

$$\mathcal{E}(t) = -\frac{d\Phi}{dt}$$

Substituting the expression for $\Phi(t)$:
$$\mathcal{E}(t) = -\frac{d}{dt} [N B S \cos(\omega t)]$$
$$\mathcal{E}(t) = N B S \omega \sin(\omega t)$$

This result shows that a rotating loop produces an **Alternating Current (AC)** voltage.

---

### 3. Calculation of the Amplitude $\mathcal{E}_0$

The amplitude (peak value) of the induced EMF occurs when the sine function reaches its maximum value ($\sin(\omega t) = 1$):

$$\mathcal{E}_0 = N B S \omega$$

---

### 4. Dependence on Angular Velocity $\omega$

From the amplitude formula $\mathcal{E}_0 = N B S \omega$, we observe a **linear relationship** between the peak voltage and the rotational speed:
$$\mathcal{E}_0 \propto \omega$$

* **Physical Insight:** If the loop rotates twice as fast, the rate at which the field lines are "cut" by the loop doubles, resulting in a doubling of the output voltage. This is why turbines in power plants must maintain a strictly constant rotation speed.

---

### 5. Interpretation of the EMF Generation Mechanism

The generation of EMF in this system is driven by **Magnetic Flux Linkage change**. 

As the loop rotates, its effective area (the area "seen" by the magnetic field) constantly changes. 
* When the loop is perpendicular to the field, flux is maximum but changing slowly (EMF is zero).
* When the loop is parallel to the field, flux is zero but changing at its maximum rate (EMF is peak).

This is the fundamental operating principle of the **AC Generator (Alternator)**. We are converting mechanical work (rotation) into electrical energy by forcing electrons to move in response to the changing magnetic environment.
