# Smallest-Positive-Missing-Number in python
n = int(input())
a = [int(x) for x in input().split()]
a.sort()
missing = 1
for i in range(n):
    if a[i] <= 0:
        continue
    if a[i] == missing:
        missing += 1
    elif a[i] > missing:
        break
print(missing)
