---
title: 'Starting with Python 3.9, you can use the type[] annotation directly.'
date: 2024-02-11T14:50:26+09:00
draft: false
toc: false
comments: false
categories:
- python
- typings
tags:
- python
- typings
- chatGPT-4
---

# Starting with Python 3.9, you can use the `type[]` annotation directly:

```python
class MySuperClass:
    pass

class MySubClass(MySuperClass):
    pass

def get_class() -> type[MySuperClass]:
    return MySubClass
```

In the above example, the `get_class` function returns a class that is `MySubClass` or any 
subclass of `MySuperClass`.

Example:

```shell
➜ python3.10
Python 3.10.6 (main, Dec 16 2022, 11:02:44) [Clang 14.0.0 (clang-1400.0.29.202)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> class MySuperClass:
...     pass
...

>>> class MySubClass(MySuperClass):
...     pass
...

>>> def get_class() -> type[MySuperClass]:
...     return MySubClass
...

>>> get_class() # The return type of get_class is type[MySuperClass].
<class '__main__.MySubClass'>

>>> get_class()()  # We can instantiate the class returned by get_class.
<__main__.MySubClass object at 0x104e75c00>
```
