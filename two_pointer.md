# same direction two pointer
```
j = 1
for i from 0 to n
    (optional) keep the j on the right side of i
    while j < n  and i, j doesn't match the condition:
        j += 1
    if j >= n:
        break
    deal with current i, j
```
most important, the both pointers don't go back and always move in one direction. So i and j are kind of independent and they only iterates the array once.