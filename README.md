# Sets - Python
An introductory walkthrough for sets in Python.

## Introduction
Sets are one of several ways of organizing objects in Python - akin to lists, dictionaries, tuples, etc. If you don't know about lists yet, make sure to get caught up on those first. 

Say you're organizing music.  You can think of a "set" like a playlist in shuffle mode.  It's unordered, does not repeat songs, and it's easy to see which songs are or are not in your playlist.

#### What Sets "Sets" Apart?

What can make sets very useful is that all elements are unique, and they can have a much better computational performance when running certain functions when compared to lists.  For example, `i in set` performs much faster than `i in list`.  These code snippets will return either `True` or `False`, and it is often useful to use similar code iteratively (in a loop), so time can matter if you're performing a loop on a whole column of a dataset, for example.

However, sets lack order making them difficult to index, iterate through, and otherwise select individual elements.  Forutnately, it's easy to change back and forth between lists and sets using `list()` and `set()`.

You can even nest those functions like so: `list(set(original_list))`, if you wanted to eliminate duplicates in `original_list`.

Also, sets are mutable, so methods like `.add()` will change the set.

## Working With Sets

#### Creating Sets
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
will return `{'a','b','c','d'}`

#### Using Sets for Reference
Sets are especially useful for generating booleans and referring to other objects.
```python
4 in {1,2,3}
False

'orange' in {'red','orange','yellow}
True
```

This is especially useful in loops.
```python
for i in [1,2,3,4]:
  i in {1,3,5,9}

True
False
True
False
```

#### Set Methods
Sets have several built-in functions that expand their functionality.

Let's start with two sets.
```python
x = {1,3,5,7,9}
y = {1,2,3,4}
```

The add function will add another element to the set.  If it already exists, nothing changes.
Remove removes an element.
```python
x.add(10)
{1, 3, 5, 7, 9, 10}

x.add(1)
{1, 3, 5, 7, 9, 10}

x.remove(9)
{1, 3, 5, 7, 10}
```
Intersection and Union are two ways of combining sets.  Union returns both sets combined, of course eliminating duplicates.  Union gives only the elements in both.  These functions do not change `x` and `y` themselves. 
```python
x.intersection(y)
{1, 2, 3, 4, 5, 7, 10}

x.union(y)
{1, 3}
```


You can find more info in the official Python documentation here: https://docs.python.org/2/library/sets.html
