# Experiment 4: Markov Chain Simulation of Weather Prediction

**QUESTION:**
 
 Write a Python program to simulate a Markov Chain for weather prediction, 
      where  the weather can be either Sunny or Rainy.

**AIM:**

To implement a Markov Chain using Python and simulate the transition of weather 
conditions based on given probabilities. 

**SOFTWARE REQUIRED:** Python and numpy library. 

**Mathematical Explanation:**

<img width="771" height="327" alt="{9D502516-C254-489A-B2F3-C85C85994B19}" src="https://github.com/user-attachments/assets/2023fc79-3ce1-4f00-bb5a-a9c83257d66f" />

**Algorithm:**

<img width="744" height="382" alt="{65CC0939-C278-49D8-AA7E-5A8ADDD1C89E}" src="https://github.com/user-attachments/assets/fa7554e6-1148-4cc2-8dde-e841703900b9" />

**PROGRAM**
```
import numpy as np 
 
# Get transition probabilities 
p_sr = float(input("Enter P(Sunny→Rainy): ")) 
p_rs = float(input("Enter P(Rainy→Sunny): ")) 
 
# Transition matrix 
P = [[1 - p_sr, p_sr], 
     [p_rs, 1 - p_rs]] 
 
states = ["Sunny", "Rainy"] 
 
# Initial state and steps 
current_state = int(input("Enter initial state (0 for Sunny, 1 for Rainy): ")) 
steps = int(input("Enter number of steps: ")) 
 
print("\n--- Markov Chain Simulation of Weather ---") 
for i in range(steps): 
    print(f"Step {i+1}: {states[current_state]}") 
    current_state = np.random.choice([0, 1], p=P[current_state])
```
**OUTPUT:**

<img width="519" height="244" alt="{E3CF9BD5-30AB-4A3D-9EE1-03D567204266}" src="https://github.com/user-attachments/assets/ba9b5546-499a-44ef-aed2-4b5ebb4af888" />


**RESULT:**
The program successfully simulates a Markov Chain for weather prediction.
