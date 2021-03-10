# python-manual-quartile
Finding quartiles without importing numpy

```
data = sorted(list(map(int,input("Input numbers with space > ").split())))
n = len(data)
i = n // 2

if n % 2 == 0:
	median = (data[i-1] + data[i])/2
	q3i = 0
else:
	median = data[i]
	q3i = 0

nquartile = n // 2
i = nquartile // 2

if nquartile % 2 == 0:
	q1 = (data[i-1] + data[i])/2
	q3 = (data[q3i + nquartile + i - 1] + data[q3i + nquartile + i]) / 2
else:
	q1 = data[i]
	q3 = data[q3i + nquartile + i]

print(data)
print("Q1 =", q1)
print("Q2 =", median, "(median)")
print("Q3 =", q3)
print("Interquartile =", q3 - q1)
```
