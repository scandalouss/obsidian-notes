---
id: chapter8
aliases:
  - chapter8
tags: []
---

# chapter8 - Loops: A programmers best friend (no seriously)

Loops allow us to perform the same operation multiple times,
without having to write it explicitly each time.
For example,

## For loop:

```python
for i in range(0,10):
    print(i)
```
This code will start with i=0 (i in range(0,10))
then it will print i to the console (print(i))
then it will add 1 to i (default behavior of the range() function)
once it has done all that, it will return to the first step,
as long as i<10

## While loop:

```python
while 1:
    print("1 evaluates to true")
```

This code is an infinite loop. ``while 1:`` will always evaluate to ``True``.
While loops will do whatever is defined inside them,
as long as the defined condition is met.
This code will forever print "1 evaluates to true" to the console.

```python
num = 0
while num < 3:
    num = num + 1
    print(num)
```

this code will add 1 to ``num`` and then print it, until the value of ``num`` reaches 3.
