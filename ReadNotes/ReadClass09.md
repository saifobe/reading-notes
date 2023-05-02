# Dunder Methods 

## What Are Dunder Methods?

Dunder methods are special methods in Python that have two underscores before and after their name. Dunder here means “Double Under (Underscores)”. These are commonly used for operator overloading. Few examples for magic methods are: `__init__`, `__add__`, `__len__`, `__repr__` etc.

## Example: Creating a Vector

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __repr__(self):
        return f"Vector({self.x}, {self.y})"
```

## Example: Using a Vector

```python
>>> v1 = Vector(1, 2)
>>> v2 = Vector(10, 20)
>>> v1 + v2
Vector(11, 22)
```

## Example: Creating a Vector

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __repr__(self):
        return f"Vector({self.x}, {self.y})"
```

# Things I want to know more about

* I want to know more about Dunder Methods
