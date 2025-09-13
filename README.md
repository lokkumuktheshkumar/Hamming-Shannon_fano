# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4, 0.2, 0.1, 0.2, 0.1} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Colab with laptop
# Program:
```
import math
p = [0.4, 0.2, 0.2, 0.1, 0.1]
lk = [2, 2, 2, 3, 3]
n = len(p)
L = sum(p[k] * lk[k]
for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
eff = round(hs / L, 3)
red = round(1 - eff, 3)
var = sum(p[k] * (lk[k] - L) ** 2
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
![huff](https://github.com/user-attachments/assets/5b077fe2-fc1d-41d6-b385-b0e626c10aca)

# Output
<img width="407" height="139" alt="image" src="https://github.com/user-attachments/assets/e7916f8a-9104-4f78-b42b-f551e8991519" />

# Results:
Thus the average code word length, entropy, variance, redundancy, and efficiency was calculated and verified with observed values.
