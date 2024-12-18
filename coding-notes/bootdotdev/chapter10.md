---
id: chapter10
aliases:
  - chapter10
tags: []
---

# chapter10 - Dictionaries

Dictionaries in Python are used to store data values in ``key -> value`` pairs.
Dictionaries are a greate way to store groups of information.

```python
# use curly braces
#Add key-value pairs
car = {
  "brand": "Tesla",
  "model": "3",
  "year": 2019
}
```

Here, the car variable is assigned to a dictionary, with the keys
brand, model, and year, with the ``:`` separating the corresponding values.

## Duplicate keys

Because dictionaries rely on uniques keys, you can't have two of the same key in the same dictionary.
If you try to use the same key twiice, the first value will simply be overwritten.

## Accessing Dictionary values

Dictionary elements can be retrieved by specifying the corresponding key in square brackets ``[]``
The square brackets look similar to indexing in an array.

```python
car = {
    "make": "tesla",
    "model": "3"
}
print(car["make"])
# Prints: tesla
```

## Setting Dictionary values

You don't need to create a dictionary witih values already inside. It is common to create a blank dictionary,
then populate it later using dynamic values.
The syntax is the samme as getting data out of a key, just use the assignment operator ``=``
to give that key a value.

```python
planets = {}
planets["Earth"] = True
planets["Pluto"] = False
print(planets["Pluto"])
# Prints False
```

If you try to set the value of a key that already exists, you'll end up just updating the value of that key.

### Deleting values

You can also use the ``del`` keyword to delete dictionary values.
Note that if you try to delete a key that doesn't exist, you'll get an error.

### Checking for values/existence of values

If you're unsure whether or not a key exists in a dictionary, use the ``in`` keyword

```python
cars = {
    "ford": "f150",
    "tesla": "3"
}

print("ford" in cars)
# Prints: True

print("gmc" in cars)
# Prints: False
```


