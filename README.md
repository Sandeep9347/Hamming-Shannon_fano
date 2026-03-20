# Huffman-Shannon_fano
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 

Aim:

To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance
for a discrete memoryless source using Huffman and Shannon-Fano coding based on the
given probabilities and codeword lengths.

Tools Required:

Python: A versatile language for scientific computing and signal processing.
NumPy & Matplotlib: Libraries for numerical operations and high-quality visualizations,
essential for demonstrating sampling

Program:
```
import numpy as np
import math
L = 0
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
for k in range (n):
Avg1 = p[k] * lk[k]
L = L + Avg1
for k in range (n):
e = p[k] * math.log(1 / p[k], 2)
hs = hs + e
hs = round(hs,3)
eff = hs / L
eff = round(eff,3)
red = round(1 - eff,3)
var = 0
for k in range(n):
var1 = p[k] * (lk[k]-L)**2
var = var + var1
var = round(var,3)
print()
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff*100} %")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
Output:

![image](https://github.com/user-attachments/assets/31f2bd7d-586a-4e6b-9990-818153a96f5c)

Calculation:


![WhatsApp Image 2025-03-28 at 13 08 17_15682bca](https://github.com/user-attachments/assets/9aff5589-0307-4c1a-b38d-1a96f55d0560)

![Screenshot 2025-03-28 130714](https://github.com/user-attachments/assets/7240c2fb-7e9b-4ada-8533-5831367e9007)

![Screenshot 2025-03-28 130714](https://github.com/user-attachments/assets/082a5d95-290d-48e5-9d44-0785664769a2)

Results:

For the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25.
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0 %
Redudancy is : 0.0
Variance is : 0.484.
