# Why OOP

Imagine you are building a management software for university.

You need to manage details and functions for students, teacher, courses, etc.

You can use either Procedural of OOP method for this.

- **Procedural:** Like having **one big bag** with student, teacher, and course papers mixed together. You must **search manually** whenever you need something.

- **OOP:** Like having **separate labeled folders** for each student, teacher, and course. Everything is **organized**, and you can find or update info easily.

  

![[/image 62.png|image 62.png]]

# Class and object definition

Imagine class as a blueprint to build a house, then objects are the different houses built using that blueprint (class)

![[/image 1 15.png|image 1 15.png]]

## Class

Class is a blueprint of object that can be made using the class.

It specified the attribute (variables inside a class) and method (functions inside a class)

## Objects

Objects are instance of class.

Every object has separate memory.

# How to create class and object

![[/image 2 9.png|image 2 9.png]]

```python
class Student:
    def __init__(self, roll_no, name, grade):
        self.roll_no = roll_no
        self.name = name
        self.grade = grade
    def show_student(self):
        print(f"Name: {self.name}\n Roll no: {self.roll_no}\n Grade: {self.grade}")

s1 = Student(1, "Ashwin", 90)
s2 = Student(2, "Bob", 95)
s1.show_student()
s2.show_student()
```

> Output
> 
>   
> 
> Name: Ashwin  
> Roll no: 1  
> Grade: 90  
> 
> Name: Bob  
> Roll no: 2  
> Grade: 95

# Constructor

- A **constructor** is a **special method** in a Python class that **runs automatically** when a new **object** is created.

- It is mainly used to **initialize object attributes** with values.

- In Python, the constructor is always named `**__init__()**`.

```python
class ClassName:
    def __init__(self, parameters):
        self.attribute = parameters   # initializing instance variable
```

# Self

- `self` is a **reference to the current object** of the class.

- It is **used inside class methods** to:
    
    1. Access **instance variables** (object attributes).
    
    1. Call **other methods** of the same class.
    

- `self` is **automatically passed** as the **first parameter** to every method in a class.

```python
class ClassName:
    def method_name(self, parameters):
        # use self to refer to current object
        self.variable_name = value
```

# Class attribute and Instance Attribute

## Instance Attribute

- Attributes that belong to a specific object (instance).

- Defined inside the constructor (`__init__`) using `self`.

- Each object has its own copy of these attributes.

- Used to store unique data for each object.

In the below code :

- `s1` and `s2` have separate copies of `name` and `age`.

- Changing `s1.name` won't affect `s2.name`.

```python
class Student:
    def __init__(self, name, age):
        self.name = name        # instance attribute
        self.age = age          # instance attribute

# Creating two different objects
s1 = Student("Alice", 20)
s2 = Student("Bob", 22)

print(s1.name, s1.age)
print(s2.name, s2.age)
```

> Output
> 
> Alice 20  
> Bob 22

## Class Attributes

- Attributes that belong to the class itself, shared by all objects.

- Defined outside any method, inside the class directly.

- Changing a class attribute affects all objects (unless overridden in an instance).

In the below code `school_name` is **shared by all students** because it’s a **class attribute**.

```python
class Student:
    school_name = "ABC High School"  # class attribute

    def __init__(self, name, age):
        self.name = name            # instance attribute
        self.age = age

# Creating objects
s1 = Student("Alice", 20)
s2 = Student("Bob", 22)

print(s1.name, "-", s1.school_name)
print(s2.name, "-", s2.school_name)
```

> Output
> 
> Alice - ABC High School  
> Bob - ABC High School

# Accessing Members

In Python, class members (variables and methods) can have different levels of access control.  
Python does not strictly enforce access control but uses naming conventions to indicate the level of access.

## Public Members

- Accessible from anywhere — inside or outside the class.

- Default type of member in Python.

- Written normally (no underscores).

In the below code `name` can be freely accessed and modified from outside the class.

```python
class Student:
    def __init__(self, name):
        self.name = name   # public member

    def display(self):
        print("Student Name:", self.name)

s = Student("Ashwin")
s.display()

# Accessing directly from outside the class
print("Accessing directly:", s.name)
```

> Output
> 
> Student Name: Ashwin  
> Accessing directly: Ashwin

## Protected Members

- Accessible within the class and its subclasses, but should not be accessed directly from outside the class.

- Used to indicate that the member is intended for internal use only.

- Start the name with a single underscore (`_`).

- Python does not enforce protection it's just a convention, so the member can still be accessed directly, but it’s discouraged.

```python
class Student:
    def __init__(self, name, age):
        self.name = name   # public member
        self._age = age    # protected member

    def display(self):
        print(f"Student Name: {self.name}, Age: {self._age}")

s = Student("Ashwin", 20)
s.display()

# Accessing directly from outside the class
print("Accessing public member:", s.name)
print("Accessing protected member:", s._age)
```

> Output
> 
> Student Name: Ashwin, Age: 20  
> Accessing public member: Ashwin  
> Accessing protected member: 20

## Private Members

- Accessible **only inside the class** where they are defined.

- **Cannot be accessed directly** from outside or by subclasses.

- Start the name with **two underscores (**`**__**`**)**.

- Python internally **renames private members** using **name mangling**
    
    - `__variable` becomes `_ClassName__variable`.  
        
    

```python
class Student:
    def __init__(self, name, age, roll_no):
        self.name = name   # public member
        self._age = age    # protected member
        self.__roll_no = roll_no # private member

    def display(self):
        print(f"Student Name: {self.name}, Age: {self._age}, Roll no: {self.__roll_no}")

s = Student("Ashwin", 20, 1)
s.display()

# Accessing directly from outside the class
print("Accessing public member:", s.name)
print("Accessing protected member:", s._age)
print("Accessing private member:", s._Student__roll_no)
# The below code will raise error
# print("Accessing protected member:", s.__roll_no)
```

> Output
> 
> Student Name: Ashwin, Age: 20, Roll no: 1  
> Accessing public member: Ashwin  
> Accessing protected member: 20  
> Accessing private member: 1

# Instance, Class vs Static methods

In Python, methods are functions defined inside a class.  
They are used to perform operations on object data or class data.

## Instance Method

- Works with **instance attributes** (unique to each object).

- **First parameter is always** `**self**`, which represents the **current object**.

- Most commonly used type of method.

- To access or modify the **data specific to an object**.

```python
class Student:
    def __init__(self, name, marks):
        self.name = name        # instance attribute
        self.marks = marks

    # instance method
    def display(self):
        print(f"Name: {self.name}, Marks: {self.marks}")

s1 = Student("Ashwin", 85)
s2 = Student("Bob", 92)

s1.display()
s2.display()
```

> Output
> 
> Name: Ashwin, Marks: 85  
> Name: Bob, Marks: 92

## Class Method

- Works with class-level attributes (shared by all objects).

- First parameter is `cls`, which refers to the class itself (not the object).

- Declared using `@classmethod` decorator.

- To work with shared data for all instances.

In the below code `cls.school_name` updates the class attribute, affecting all objects.

```jsx
class Student:
    school_name = "ABC High School"  # class attribute

    def __init__(self, name):
        self.name = name

    @classmethod
    def change_school(cls, new_name):
        cls.school_name = new_name    # modifies class attribute

s1 = Student("Ashwin")
s2 = Student("Bob")

print("Before change:", s1.school_name, "|", s2.school_name)

# Call class method
Student.change_school("XYZ International School")

print("After change:", s1.school_name, "|", s2.school_name)
```

> Output
> 
> Before change: ABC High School | ABC High School  
> After change: XYZ International School | XYZ International School

## Static Method

- Does not need access to either instance (`self`) or class (`cls`) data.

- Behaves like a regular function, but is logically grouped inside a class.

- Declared using `@staticmethod` decorator.

- To perform utility tasks related to the class but independent of object or class state.

```jsx
class Student:
    school_name = "ABC High School"  # class attribute

    def __init__(self, name):
        self.name = name

    @staticmethod
    def isAdult(age):
        if age > 18:
            print("Yes")
        else:
            print("No")

s1 = Student("Ashwin")
s2 = Student("Bob")

s1.isAdult(19)
s2.isAdult(17)
```

> Output
> 
> Yes  
> No

## Comparison Table

|**Feature**|**Instance Method**|**Class Method**|**Static Method**|
|---|---|---|---|
|**Decorator**|❌ None|✅ `@classmethod`|✅ `@staticmethod`|
|**First Parameter**|`self` (object)|`cls` (class)|No default parameter|
|**Accesses**|Instance attributes|Class attributes|Neither instance nor class attributes|
|**Called By**|Object or Class|Object or Class|Object or Class|
|**Use Case**|Object-specific operations|Work with shared data|Utility/helper functions|