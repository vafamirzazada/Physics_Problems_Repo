# Task 09: Change of Reference Frame (Copernican to Geocentric)

---

## 1. Problem Restatement
We are analyzing the motion of Earth and Mars. Both planets move in circular orbits around the Sun in the same direction.

**Given (Heliocentric Model):**
* Position of Earth (Z): 
  $$\vec r_Z(t) = R_Z (\cos(\omega_Z t), \sin(\omega_Z t))$$
* Position of Mars (M): 
  $$\vec r_M(t) = R_M (\cos(\omega_M t), \sin(\omega_M t))$$

*(Note: The subscript $Z$ is used for Earth, likely from the Polish word "Ziemia").*

**We need to:**
1. Determine the position of Mars *relative* to Earth (the geocentric system).
2. Explicitly write down the $x$ and $y$ components of this relative position: $x_{M/Z}(t)$ and $y_{M/Z}(t)$.
3. Note the requirements for a side-by-side HTML animation of both models.

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics and relative motion.
* **Assumptions:** * Both planets move in perfect circles.
    * The orbits are in the exact same 2D plane (coplanar).
    * Angular velocities ($\omega_Z$ and $\omega_M$) are constant. 
    * The Sun is stationary at the origin $(0,0)$ for the heliocentric model.

---

## 3. Mathematical Derivation

To find the position of Mars as seen from Earth, we must subtract Earth's position vector from Mars's position vector. 

This shifts the origin of our coordinate system from the Sun directly to the Earth.

### Step 1: Define the Individual Components
First, let's write out the $x$ and $y$ coordinates for each planet separately.

**For Mars (Target):**
$$x_M(t) = R_M \cos(\omega_M t)$$

$$y_M(t) = R_M \sin(\omega_M t)$$

**For Earth (Observer):**
$$x_Z(t) = R_Z \cos(\omega_Z t)$$

$$y_Z(t) = R_Z \sin(\omega_Z t)$$

### Step 2: Calculate Relative Position Components
The relative position vector is defined as:
$$\vec r_{M/Z}(t) = \vec r_M(t) - \vec r_Z(t)$$

We find the new components by simply subtracting the observer's coordinates from the target's coordinates.

**The relative X-component:**
$$x_{M/Z}(t) = x_M(t) - x_Z(t)$$

**$$x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)$$**

**The relative Y-component:**
$$y_{M/Z}(t) = y_M(t) - y_Z(t)$$

**$$y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)$$**

### Step 3: Final Relative Position Vector
Combine the components back into a single vector equation:

$$\vec r_{M/Z}(t) = \Bigl( R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t), \quad R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t) \Bigr)$$

---

## 4. Interpretation of Results
The resulting equations describe a complex curve known as an **epitrochoid**. Because Earth moves faster on its inside track ($\omega_Z > \omega_M$), there are times when Earth "laps" Mars. In the geocentric equations we just derived, this lapping effect causes the math to produce a "loop" where Mars appears to briefly stop, move backward (retrograde motion), and then move forward again.

---

## 5. Conceptual Explanation
If you lock your camera onto the Sun (Heliocentric), you see two simple, elegant circles. But if you lock your camera onto a moving Earth (Geocentric), the Sun orbits you in a simple circle, but Mars's motion becomes the sum of its own orbit *plus* the reverse of Earth's orbit. This mathematical subtraction is exactly why ancient astronomers like Ptolemy had to invent "epicycles" (circles moving on circles) to explain the night sky!

> **Note:** HTML visualization required (Phase 2).
> **Requirements:** A dual-panel animation. 
> * **Panel A (Heliocentric):** Sun in the center, Earth and Mars orbiting on simple concentric circles.
> * **Panel B (Geocentric):** Earth fixed in the center, with Mars tracing the looping epitrochoid path defined by $\vec r_{M/Z}(t)$.
