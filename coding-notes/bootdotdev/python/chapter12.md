---
id: chapter12
aliases:
  - chapter12
tags: []
---

# chapter12 - Errors and Exceptions

## Syntax errors

Syntax errors are fairly straightforward, it's simply the language interpreter telling you that
whatever code you've written doesn't follow formatting standards, and that it won't compile.

In other words, you typed something wrong, like a semi-colon or colon in the wrong spot, or an extra set
of parenthesis where there doesn't need to be any. A syntax error could get caught quickly
by the interpreter/compiler, but it could also result in *technically* valid code, but produces unintended results,
or errors out in an unexpected way. Always watch what you type, and make sure you're following standards!!

## Exceptions

Even if your code has the right syntax, however, it may still cause an error when an attempt is made to
execute it. Errors detected during the execution of your code are called an exception, and can be handled
gracefully by your code. You can even raise your own exceptions when bad things happen in your code.

Python uses a ``try-except`` pattern for handling errors:

```python
try:
  10 / 0
except Exception:
  print("can't divide by zero")
```

the ``try`` block is executed until an exception is raised or it completes, whichever happens first.
In this case, an exceptiion is raised because division by 0 is impossible.
The ``except`` block is only executed if an exception is raised in the ``try`` block

IIf we want to access the data from the exception, we use the following syntax:

```python
try:
    10 / 0
except Exception as e:
    print(e)

#prints "division by 0"
```

Wrapping potential errors in ``try/except`` blocks allows the program to handle the exception gracefully,
with no crashes.
