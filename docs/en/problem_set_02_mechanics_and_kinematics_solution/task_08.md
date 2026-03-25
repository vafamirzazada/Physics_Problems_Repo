# Task 08: Relative Motion

---

## 1. Problem Restatement
We are given the constant velocities of two bodies, A and B, in a standard coordinate system.

**Given:**
* Velocity of body A: $\vec v_A = (3, 1)$
* Velocity of body B: $\vec v_B = (1, -2)$

**We need to:**
1. Determine the relative velocity $\vec v_{A/B}$ (velocity of A relative to B).
2. Determine the direction of this relative motion.
3. Note the requirements for visualizing the motion in three different reference frames (Origin, Body A, Body B).

---

## 2. Physical Model and Assumptions
* **Model:** 2D Kinematics and Galilean Relativity.
* **Assumptions:** * Both bodies move at constant velocities (zero acceleration).
    * Speeds are much lower than the speed of light, so classical velocity addition applies.

---

## 3. Mathematical Derivation

### Step 1: Determine Relative Velocity $\vec v_{A/B}$
The velocity of A *relative to* B means: "If I am sitting on body B and consider myself completely still, how fast does body A appear to be moving?"

The formula is the velocity of the target minus the velocity of the observer:
$$\vec v_{A/B} = \vec v_A - \vec v_B$$

Substitute the given vectors:
$$\vec v_{A/B} = (3, 1) - (1, -2)$$

Subtract the $x$ components and $y$ components separately:
$$\vec v_{A/B} = (3 - 1, \, 1 - (-2))$$

**$$\vec v_{A/B} = (2, 3)$$**

### Step 2: Determine the Direction of Relative Motion
The direction can be described by the angle $\theta$ that the relative velocity vector makes with the positive $x$-axis.

We use the tangent function, which is the $y$-component divided by the $x$-component:
$$\tan \theta = \frac{v_{y, A/B}}{v_{x, A/B}}$$

Substitute our relative velocity components:
$$\tan \theta = \frac{3}{2} = 1.5$$

Calculate the inverse tangent (arctan) to find the angle:
$$\theta = \arctan(1.5)$$

**Angle $\approx$ 56.3°**

---

## 4. Interpretation of Results
Even though body A is moving slightly upward and mostly to the right (3, 1), to an observer on body B (who is moving down and slightly right), body A appears to be flying away sharply upwards and to the right at a **56.3°** angle. 

---

## 5. Conceptual Explanation and Reference Frames
Velocity is never absolute; it always depends on who is measuring it. 
* **Frame of the Origin:** Both A and B are moving. A moves at $(3,1)$ and B moves at $(1,-2)$.
* **Frame of Body A:** Body A pretends it is the center of the universe $(0,0)$. To A, body B appears to be moving away in the exact opposite direction of $\vec v_{A/B}$, which is $\vec v_{B/A} = (-2, -3)$.
* **Frame of Body B:** Body B pretends it is the center of the universe $(0,0)$. To B, body A is moving away at $\vec v_{A/B} = (2, 3)$.

> **Note:** HTML visualization required (Phase 2).
> **Requirements:** An animation with three toggleable views:
> 1. Origin frame (both dots move).
> 2. Body A frame (Dot A is locked in the center, Dot B moves away down/left).
> 3. Body B frame (Dot B is locked in the center, Dot A moves away up/right).
