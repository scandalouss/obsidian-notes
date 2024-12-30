---
id: chapter11
aliases:
  - chapter11
tags: []
---

# chapter11 - Sets

Sets are like arrays, but they are UNORDERED, and they guarantee uniqueness.
Only ONE of each value can be in a set.

```python
fruits = {'apple', 'banana', 'grape'}
print(type(fruits))
# Prints: <class 'set'>

print(fruits)
# Prints: {'banana', 'grape', 'apple'}
```

## Adding values

```python
fruits = {'apple', 'banana', 'grape'}
fruits.add('pear')
print(fruits)
# Prints: {'banana', 'grape', 'pear', 'apple'}
```

[!NOTE]
No error wiill be raised if you add an item already in the set.

## Empty set

Because the empty bracket ``{}`` syntax creates an empty dictionary, to create an empty set,
you need to use the ``set()`` function

```python
fruits = set()
fruits.add('pear')
print(fruits)
# Prints: {'pear'}
```

## Iterating over values in a set 

[!NOTE]
Remember! Order is not guaranteed!!!

```python
fruits = {'apple', 'banana', 'grape'}
for fruit in fruits:
    print(fruit)
    # Prints:
    # banana
    # grape
    # apple
```
