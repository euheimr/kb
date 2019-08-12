# pass  Statements

*[Source](https://docs.python.org/3/tutorial/controlflow.html#pass-statements)*

*dir: %userprofile%/Dropbox/kb/lang/python*

*date: 07-16-2019*

*c. Jacob Betz*


The pass statement does nothing. It can be used when a statement is required syntactically but the program requires no action. For example:

```python
>>> while True:
...     pass  # Busy-wait for keyboard interrupt (Ctrl+C)
...
```

This is commonly used for creating minimal classes:

```python
>>> class MyEmptyClass:
...     pass
...
```

Another place pass can be used is as a place-holder for a function or conditional body when you are working on new code, allowing you to keep thinking at a more abstract level. The pass is silently ignored:

```python
>>> def initlog(*args):
...     pass   # Remember to implement this!
...
```