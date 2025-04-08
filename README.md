## HAMMING SHANON FANNON CODING
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
## AIM :
To implement Shannon-Fano coding technique for a given set of symbol probabilities and calculate the average codeword length, entropy, efficiency, redundancy, and variance of the code.
## TOOLS REQUIRED:
Python IDE with Numpy and Scipy
## PROGRAM:
````

import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
````
## Calculation:
![WhatsApp Image 2025-04-08 at 10 27 07_5f73bc2b](https://github.com/user-attachments/assets/5d072af5-6dd2-445d-a3ad-8adde608c092)
![WhatsApp Image 2025-04-08 at 10 32 04_e195f2c2](https://github.com/user-attachments/assets/887f5aa1-2ac5-4e7c-bc3c-e25c9de4b69f)
![WhatsApp Image 2025-04-08 at 10 32 25_dd5fa832](https://github.com/user-attachments/assets/2788fe3e-63dc-4752-adf7-a94ae0f2fa43)
![WhatsApp Image 2025-04-08 at 10 31 50_31951ee2](https://github.com/user-attachments/assets/b34ddffa-f2a5-4c6a-bd11-e787dfe25ce7)

## RESULTS :
![WhatsApp Image 2025-04-08 at 10 28 04_c9f15d48](https://github.com/user-attachments/assets/73d5498e-abca-4618-80c6-c29cea0c46fc)
## RESULTS :
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified

