# Lists (python)

*[Source](https://docs.python.org/3/library/stdtypes.html#range)*

*dir: %userprofile%/Dropbox/kb/lang/python*

*date: 07-16-2019*

*c. Jacob Betz*


It is convenient to use the [enumerate()](https://docs.python.org/3/library/functions.html#enumerate) function, see [Looping Techniques](https://docs.python.org/3/tutorial/datastructures.html#tut-loopidioms).


If you need to iterate over a sequence of numbers; It generates arithmetic progressions:
```python
>>> for i in range(5):
...     print(i)
...
0
1
2
3
4
```


The given end point is never part of the generated sequence; range(10) generates 10 values, the legal indices for items of a sequence of length 10. It is possible to let the range start at another number, or to specify a different increment (even negative; sometimes this is called the ‘step’):
```python
range(5, 10)
   5, 6, 7, 8, 9

range(0, 10, 3)
   0, 3, 6, 9

range(-10, -100, -30)
  -10, -40, -70
```

A strange thing happens if you just print a range:

```python
>>> print(range(10))
range(0, 10)
```


In many ways the object returned by range() behaves as if it is a list, but in fact it isn’t. It is an object which returns the successive items of the desired sequence when you iterate over it, but it doesn’t really make the list, thus saving space.

We say such an object is iterable, that is, suitable as a target for functions and constructs that expect something from which they can obtain successive items until the supply is exhausted. We have seen that the for statement is such an iterator. The function list() is another; it creates lists from iterables:

```python
>>> list(range(5))
[0, 1, 2, 3, 4]
```











