## 1. What is `@staticmethod`?
A static method is a method that belongs to a **class** rather than an **instance** of that class. 

* **No `self` or `cls`:** It doesn't take the traditional `self` (instance) or `cls` (class) arguments.
* **Isolated:** It cannot modify the state of the object or the class.
* **Utility Tool:** It’s used when you have a function that logically belongs inside a class because it's related to that class’s theme, but it doesn't actually need to "talk" to the rest of the class.

**Example:**
```python
class Calculator:
    @staticmethod
    def add(x, y):
        return x + y

# You don't need to create an object to use it
print(Calculator.add(5, 10)) 
```

---

## 2. What is `@abstractmethod`?
An abstract method is a "placeholder." It is used in a **Base Class** (parent) to say: *"Every class that inherits from me MUST implement this specific method, or I won't let you create an object."*

* **Found in:** The `abc` (Abstract Base Classes) module.
* **Enforcement:** It ensures consistency across different subclasses.
* **No Body:** Usually, the method body is just `pass`.

**Example:**
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * (5**2)
```

In the above example let's say I have another class:

```python

class square(Shape):
    def mesaure(self):
        return 3.14 * (5**2)

sq = square()

```

This fail's and give error, even if you just try to create an instance of it. That is beacuse, since your are inherting shape, you have to create
the abstract class. Eeven " sh = Shape() " failes, as you can't create an instance of the shape itself, as it a abstract class.


