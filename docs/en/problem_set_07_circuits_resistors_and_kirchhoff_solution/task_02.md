
### **Step-by-Step Simplification**

#### **Step 1: The Top "Hat" Loop**

Look at the very top loop sitting above the middle horizontal resistor.

* There are three resistors forming this upper arch (left vertical, top horizontal, and right vertical).
* Because they are connected end-to-end, they are in **series**.

$$R_{top\_arch} = 3 \, \Omega + 3 \, \Omega + 3 \, \Omega = 9 \, \Omega$$



#### **Step 2: Combining with the Middle Bridge**

This $9 \, \Omega$ top arch sits perfectly in **parallel** with the horizontal bridge resistor in the middle ($3 \, \Omega$).


$$R_{upper\_block} = \frac{R_{top\_arch} \cdot R_{bridge}}{R_{top\_arch} + R_{bridge}} = \frac{9 \cdot 3}{9 + 3} = \frac{27}{12} = 2.25 \, \Omega$$

#### **Step 3: Extending Down the Legs**

Now, this entire upper block ($2.25 \, \Omega$) is connected in **series** with the two vertical resistors below it (the lower legs of the "A").

* The current has to flow down through the left leg, through our combined upper block, and down the right leg.

$$R_{legs\_and\_top} = 3 \, \Omega + 2.25 \, \Omega + 3 \, \Omega = 8.25 \, \Omega$$



#### **Step 4: The Bottom Parallel Battle**

This whole central structure ($8.25 \, \Omega$) is connected in **parallel** with the bottom horizontal resistor ($3 \, \Omega$) spanning across the two terminals.


$$R_{parallel\_core} = \frac{8.25 \cdot 3}{8.25 + 3} = \frac{24.75}{11.25} = 2.2 \, \Omega$$

#### **Step 5: The Final Gatekeeper**

Lastly, this entire network ($2.2 \, \Omega$) is in **series** with the very first input resistor on the far bottom-left before the circuit splits.


$$R_{eq} = 3 \, \Omega + 2.2 \, \Omega = 5.2 \, \Omega$$

---
