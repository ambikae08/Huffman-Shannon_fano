# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google colab
# Program:
```
import numpy as np
import math

L = 0
hs = 0
p = []
lk = []

n = int(input("Enter the number of Samples : "))

for i in range(n):
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))
    p.append(pr)

for j in range(n):
    l = float(input(f"Enter the length of the sample values {j + 1}: "))
    lk.append(l)

# Avg length of the code word
for k in range(n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1

# Entropy
for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e

hs = round(hs, 3)

# Efficiency
eff = hs / L
eff = round(eff, 3)

# Redundancy
red = round(1 - eff, 3)

# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var = var + var1

var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:
<img width="868" height="1600" alt="image" src="https://github.com/user-attachments/assets/3e877124-de6c-4aa2-b454-8ad39f015e8c" />



<img width="1057" height="1572" alt="image" src="https://github.com/user-attachments/assets/bdc3def1-7a7d-4e1d-bb1f-915733a70c9e" />




<img width="984" height="1551" alt="image" src="https://github.com/user-attachments/assets/bc03d872-72c4-4b9c-ac60-9816deed66e5" />

# Output

<img width="809" height="536" alt="image" src="https://github.com/user-attachments/assets/a87f24ff-b170-4c2b-b01b-678acd9593d6" />

# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.`
