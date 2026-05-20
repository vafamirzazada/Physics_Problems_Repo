Step-by-Step Circuit Solution
Step 1: Simplify the Resistor Network
First, let's find the total equivalent resistance (R 
eq
​	
 ) so we know how much total current leaves the power supply.
The Parallel Sub-block: Notice that R 
2
​	
  and R 
3
​	
  are in parallel with each other.
R 
parallel
​	
 = 
R 
2
​	
 +R 
3
​	
 
R 
2
​	
 ⋅R 
3
​	
 
​	
 = 
60+30
60⋅30
​	
 = 
90
1800
​	
 =20 Ω
The Total Path: Now, the entire circuit is just R 
1
​	
 , our new R 
parallel
​	
  block, and R 
4
​	
  connected back-to-back in series.
R 
eq
​	
 =R 
1
​	
 +R 
parallel
​	
 +R 
4
​	
 =20 Ω+20 Ω+10 Ω=50 Ω
Step 2: Find the Total Current (I 
total
​	
 )
Using Ohm's Law (I=U/R) for the entire circuit:
I 
total
​	
 = 
R 
eq
​	
 
U
​	
 = 
50 Ω
200 V
​	
 =4 A
This means a total of 4 A of current flows out of the source, straight through R 
1
​	
 , and arrives at the parallel junction.
Step 3: Calculate the Voltage Across the Parallel Block (U 
3
​	
 )
The voltage across a parallel combination is identical for both branches. Let's find the voltage drop across this entire parallel block using its combined resistance (20 Ω) and the total current flowing through it (4 A):
U 
3
​	
 =I 
total
​	
 ⋅R 
parallel
​	
 =4 A⋅20 Ω=80 V
Answer Part 1: The voltage across resistor R 
3
​	
  is 80 V.
Step 4: Calculate the Current Flowing Through R 
3
​	
  (I 
3
​	
 )
Now that we know the exact voltage pushing through the R 
3
​	
  branch is 80 V, we apply Ohm's Law specifically to R 
3
​	
 :
I 
3
​	
 = 
R 
3
​	
 
U 
3
​	
 
​	
 = 
30 Ω
80 V
​	
 ≈2.67 A
Answer Part 2: The current flowing through resistor R 
3
​	
  (which the ammeter would read) is 2.67 A (or  
3
8
​	
  A).
