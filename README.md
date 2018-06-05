# Sets - Python
An introductory walkthrough for sets in Python.

## Introduction
Sets are one of several ways of organizing objects in Python - akin to lists, dictionaries, tuples, etc.  

Say you're organizing music.  You can think of a set like a playlist in shuffle mode.  It's unordered, does not repeat songs, and it's easy to see which songs are or are not in your playlist.

#### What Sets "Sets" Apart?

What can make sets very useful is that all elements are unique, and they can have a much better computational performance when running certain functions when compared to lists.

However, the inherent lack of order in sets makes them difficult to index.  Forutnately, it's easy to change back and forth between lists and sets using `list()` and `set()`.

## Working With Sets

There are two ways to create sets.  One is using "{}" brackets, similar to a dictionary, but with single elements instead of key/value pairs:
```python
set_x = {'a','b',3}
```

You can also create a set out of a list using the `set()` function.
```python
set_x = set(['a','b',3])
```

The `set()` funciton is especially useful for finding unique members of a list.  For example:
```python
list_x = ['a','a','b','a','c','c','d']
set(list_x)
```
