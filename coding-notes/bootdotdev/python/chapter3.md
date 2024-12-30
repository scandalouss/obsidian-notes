---
id: chapter3
aliases:
  - chapter3
tags: []
---

# chapter3

## Functions

Functions allow us to organize and reuse code.
We can take something like a complicated algorithm and store it in a function,
then simply call that function when we want to use said algorithm,
instead of having to rewrite out the whole algorithm every time we want to use it.

We can define parameters that our function can take in and use to return some sort of result.
Just like defining variables, we can have as many parameters in our function as we'd like.
Once we've defined parameters, we can then call that function and feed it arguments.
Arguments are just the actual values that go into the parameters of our functions.
```python
#a and b are paremeters
def add(a, b):
    return a+b

#5 and 6 are arguments
sum=add(5, 6)
````
[!NOTE]
if you intend to use variables declared outside a function inside said function,
they must be declared before the function.
All functions must be defined/declared before they can be used.
