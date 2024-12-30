---
id: chapter6
aliases:
  - chapter6
tags: []
---

# chapter6

## Computing numbers

All the basic arithmetic is there, like PEMDAS.
Integers are whole numbers and floats are decimals.

We also have floor division, which is like normal division except we take our answer,
and we round it DOWN to the nearest integer.

```python
7 // 3
# should equal 2 (an integer, rounded down from 2.33333...)
-7 // 3
# should equal -3 (an integer, rounded down from -2.33333...)
```

Python also has builtin support for exponents, but most other languages will require
importing/requiring/including some sort of external math library.

There is also reassignment, where we change the value of a variable based on its current value.

```python
score=4
score=score+1
#score is now 5! wow!
```

It's technically not valid math, but thats ok.
We calculate the right side first, then set the value on the left.
We can use += and -= and \*= and /= to simplify this

## Logical operator

Python also has logical operators "and", as well as "or". We use them with boolean values.
Logical "and" requires that BOTH inputs are true to return true.
Logical "or" requires that AT LEAST ONE input is true to return true.

```python
True and True == True
True and False == False
False and False == False

True or True == True
True or False == True
False or False == False
```

## Binary Numbers

Binary numbers are just "base 2" numbers. Instead of using ten symbols, 0 through 9,
we only use two symbols, 0 and 1, to represent all numbers.
Each digit in a binary number represents an ever-greater multiple of 2.
For example, in a 4 digit number you have eights place, the fours place, the twos place, and the ones place,
similar to how you would have the thousandths, hundredths, tenths, and ones place in a base 10 number.

```python
0001=1
0010=2
0011=3
0100=4
0101=5
0110=6
0111=7
1000=8
1001=9
1010=10
1011=11
1100=12
1101=13
1110=14
1111=15
```

As you can see, the number of digits we have determines how large of a number we can represent.
With 4 digits in binary, the largest number we can represent is 15.
We have 16 total values, 0 through 15.
The largest number we can represent is the total number of values we can represent minus 1.
If we have 5 digits, we'd be able to store 32 values, 0 through 31.
The total number of values we can represent in binary is 2 to the power of the number of digits.
2 to the power of 4 is 16, the total number of values we can represent with 4 digits of binary,
2 to the power of 5 is 32, the total number of values we can represent with 5 digits of binary,
etc, etc.

## Bitwise & and | operators

Bitwise operators are similar to the logical operator from before, except instead of operating on boolean values,
we apply the same logic to all the bits in a value by column.
For example, lets say we have 5 and 7 represented in binary. The bitwise ``and`` operation would have the result "5"

```python
0101 & 0111 = 0101
```

As described before, boolean values can be represented with 0s and 1s.
A 1 in binary is the same as ``True``, while a 0 is the same as ``False``.

```python
0 & 0 = 0
1 & 1 = 1
1 & 0 = 0
0 & 1 = 0
```

Lets take 5 and 7 again, but lets ``or`` them

```python
0101 | 0111 = 0111
```

So, 5 | 7 = 7
Funnily enough, 5 | 2 = 7 as well:

```python
0101 | 0010 = 0111
```

The rules for ``or`` look like this

```python
0 | 0 = 0
0 | 1 = 1
1 | 1 = 1
1 | 0 = 1
```
