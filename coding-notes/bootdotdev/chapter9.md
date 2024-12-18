---
id: chapter9
aliases:
  - chapter9
tags: []
---

# chapter9 - Arrays

One way to organize and store data is in an array, or a list, of items.
We can store any type of data inside of an array, including other arrays.

Each item we define in our array can be accessed by it's index,
which is its position inside the array.
One thing to note is that we start at index 0, not 1.
The first item in the array would be index 0, the second index 1
so an array with 4 items would count upwards 0,1,2,3, not 1,2,3,4

## Loops and Arrays

It's common to create an empty array then fill it with values, using a loop.
In python, we can use the ``.append()`` method to add items to the end of an array:

```python
cards=[]
cards.append("nvidia")
cards.append("amd")
# the cards array is now ["nvidia", "amd"]
```

In python, the opposite of ``.append()`` is ``.pop()``
Pop removes the last element from an array, and returns it for use:

```python
vegetables = ["broccoli", "cabbage", "kale", "tomato"]
last_vegetable = vegetables.pop()
# vegetables = ['broccoli', 'cabbage', 'kale']
# last_vegetable = 'tomato'
```

we can also assign a number to ``.pop()`` to specify a specific index to remove.

Loops allow us to iterate over all the elements inside of an array. For example:

```python
for i in range(0, len(sports)):
    print(sports[i])

```

In Python specifically, we can iterate over an entire array,
without specifying any index numbers of any sort:

```python
trees = ['oak', 'pine', 'maple']
for tree in trees:
    print(tree)
# Prints:
# oak
# pine
# maple
```

``tree``, the variable declared using the ``in`` keyword,
directly accessess the values in the array rather than the index of the value.

## Modulo Operator: %

The modulo operator can be used to find a remainder.
For example, 7 modulo 2 would equal 1, because 2 can be multiplied evenly into 7 at most 3 times:
``2 * 3 = 6``
Then there is 1 remaining to get to 7:
``7 - 6 = 1``

## Slicing arrays (IN PYTHON)

It's very easy to slice arrays in python. There is a dedicated slicing operator for arrays, the colon ``:``
You can use this operator to specify where to start and end the slice, and how to step through the array.
List slicing returns a NEW LIST from the existing array.

Ex:
```python
my_array[start:stop:step]
```

```python
scores=[50,70,30,20,90,10,50]
#Display array
print(scores[1:5:2])
#prints [70,20]
```

The above reads as "give me a slice of the scores array from index 1,
up to but not including 5, skipping every 2nd value."
Every section is optional

You can omit individually the start, stop, and step sections.
For example, ``numbers[:3]`` means "get all items from the start up to, but not including, index 3."
``numbers[3:]`` means "get all items from index 3 to the end."
If you want to only use the step section, you can type ``numbers[::3]``


## Concatenating arrays

Concatenating arrays, or combining multiple arrays into one, is very simple in Python.
You can use the + operator to "glue" two arrays together

## Checking if an array contains in python

Checking whether a value exists in an array is really easy in python, we can simply use the ``in`` keyword.

```python
fruits = ["apple", "orange", "banana"]
print("banana" in fruits)
# Prints: True
```

## Deleting specific items in arrays

Python has a builtin keyword ``del`` that deletes items from objects.
In the case of an array, you can delete specific indices or entire slices.

```python
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9]

# delete the fourth item
del nums[3]
print(nums)
# Output: [1, 2, 3, 5, 6, 7, 8, 9]

# delete the second item up to (but not including) the fourth item
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9]
del nums[1:3]
print(nums)
# Output: [1, 4, 5, 6, 7, 8, 9]

# delete all elements
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9]
del nums[:]
print(nums)
# Output: []
```

## Tuples

Tuples are like arrays in that they are a collection of data,
but they have a fixed size, and the data is ordered and unchangeable.
Tuples are created with round brackets:

```python
my_tuple = ("this is a tuple", 45, True)
print(my_tuple[0])
# this is a tuple
print(my_tuple[1])
# 45
print(my_tuple[2])
# True
```

It's bad practice to store items of different types in arrays.
However, for tuples, this isn't a problem.
Because of the fixed size, it's simple to keep track of which indices store which kind of data.

Typically, tuples are used to store very small groups of data, 2 or 3 items usually,
but this isn't a hard rule.
For example, you might use a tuple to store a dogs name and age.

```python
dog = ("Fido",4)
```

[!NOTE]
There is a special case for creating single-item tuples.
You must include a comma, so Python knows it's a tuple,
and not regular parenthesis.
```python
dog = ("Fido",)
```

Because tuples hold their data, multiple tuples can be stored within an array.
Similar to storing other data in arrays, each tuple witihin the array is seperated by a comma.
When accessing an array of tuples, the first index specifies which tuple you want to access,
the second selects a value within that tuple:

```python
my_tuples = [("this is the first tuple in the list", 45, True),("this is the second tuple in the list", 21, False)]
print(my_tuples[0][0]) # this is the first tuple in the list
print(my_tuples[0][1]) # 45
print(my_tuples[1][0]) # this is the second tuple in the list
print(my_tuples[1][2]) # False
```

## Tuple Unpacking

You can easily assign the values of a tuple to variables using unpacking:

```python
dog = ("Fido", 4)
dog_name, dog_age = dog
print(dog_name)
# Fido
print(dog_age)
# 4
```

[!NOTE]
When you return multiple values from a function, you're actually returning a tuple.
(This is potentially python only)
