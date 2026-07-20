# What is Abstraction?

- Abstraction means hiding complex implementation details and showing only essential features to the user.

- It focuses on what an object does, rather than how it does it.

- Achieved in Python using Abstract Base Classes (ABC) and the `@abstractmethod` decorator.

## Real-Life Example

- When you drive a car, you just use the steering, accelerator, and brake without knowing the complex engine mechanics.

- Similarly, abstraction lets the user interact with simple methods, while the complex code stays hidden inside.

# Implementing Abstraction in Python

Python provides a module called `abc` (Abstract Base Class) for creating abstract classes.

## Rules:

1. Import `ABC` and `abstractmethod` from `abc` module.

1. An abstract class cannot be instantiated directly.

1. A child class must implement all abstract methods, otherwise the child class becomes an abstract class.

```python
from abc import ABC, abstractmethod

# Abstract class
class Person(ABC):
    def __init__(self, name):
        self.name = name

    @abstractmethod
    def display_role(self):  # Abstract method
        pass

# Child class - Student
class Student(Person):
    def display_role(self):  # Implementing abstract method
        print(f"{self.name} is a Student")

# Child class - Teacher
class Teacher(Person):
    def display_role(self):
        print(f"{self.name} is a Teacher")

# Creating objects
s = Student("Bob")
t = Teacher("Ashwin")

s.display_role()
t.display_role()
```

> Output
> 
> Bob is a Student  
> Ashwin is a Teacher

## Explanation:

1. `Person` class is abstract and contains an abstract method `display_role()`.

1. You cannot create an object of `Person` directly:
    
    ```python
    obj = Person("Someone")  # Error: Can't instantiate abstract class
    ```
    

1. Student and Teacher classes must implement `display_role()`; otherwise, they will also be treated as abstract.