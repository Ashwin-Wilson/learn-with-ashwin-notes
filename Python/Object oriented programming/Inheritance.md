# What is Inheritance

- Inheritance allows a class (child/subclass) to reuse attributes and methods from another class (parent/superclass).

- It helps in code reusability, organization, and reduces redundancy.

![[/image 63.png|image 63.png]]

- Avoids writing the same code repeatedly.

- Establishes a "is-a" relationship (e.g., a Student _is a_ Person).

- Makes code easier to extend and maintain.

```python
# Parent Class
class Person:
    def __init__(self, name, address):
        self.name = name
        self.address = address

    def show_details(self):
        print(f"Name: {self.name}, Address: {self.address}")


# Child Class - Student
class Student(Person):
    def __init__(self, name, address, roll_no, grade):
        super().__init__(name, address)  # Call parent constructor
        self.roll_no = roll_no
        self.grade = grade

    def show_student(self):
        self.show_details()  # Access parent method
        print(f"Roll No: {self.roll_no}, Grade: {self.grade}")


# Child Class - Teacher
class Teacher(Person):
    def __init__(self, name, address, teacher_id):
        super().__init__(name, address)  # Call parent constructor
        self.teacher_id = teacher_id

    def show_teacher(self):
        self.show_details()  # Access parent method
        print(f"Teacher ID: {self.teacher_id}")


# Creating objects
student = Student("Ashwin", "Kerala", "1", "A")
teacher = Teacher("Bob", "Kerala", "7")

# Display details
print("Student Details:")
student.show_student()

print("\nTeacher Details:")
teacher.show_teacher()
```

> Output
> 
> Student Details:  
> Name: Ashwin, Address: Kerala  
> Roll No: 1, Grade: A
> 
> Teacher Details:  
> Name: Bob, Address: Kerala  
> Teacher ID: 7

# super()

- `**super()**` is a **built-in function** in Python.

- It is used to **call methods or constructors of the parent (superclass)** from the child (subclass).

- Most commonly used in **inheritance** to **reuse parent class code** without rewriting it.

### Using `super()` in Constructor

```python
class A:
    def __init__(self):
        print("Class A Constructor")

class B(A):  # B inherits from A
    def __init__(self):
        super().__init__()  # Call parent constructor
        print("Class B Constructor")

obj = B()
```

> Output
> 
> Class A Constructor  
> Class B Constructor

### Calling Parent Method

```python
class A:
    def display(self):
        print("Hello from Class A")

class B(A):
    def display(self):
        super().display()  # Call A's display
        print("Hello from Class B")

obj = B()
obj.display()
```

> Output
> 
> Hello from Class A  
> Hello from Class B

# Method Overriding

- **Method Overriding** occurs when a **child class** defines a **method with the same name as a parent class method**.

- The **child class version** of the method **replaces (overrides)** the parent class version **when called using the child object**.

- To **customize or completely change** the behavior of a method **inherited from the parent class**.

## **Rules for Method Overriding**

1. The **method name** must be **the same** in both parent and child classes.

1. The **parameters** (number and type) should be the **same**.

1. The child class method **takes priority** when called from a child object.

```python
class A:
    def show(self):
        print("This is Class A method")

class B(A):  # Inherits from A
    def show(self):  # Overriding parent method
        print("This is Class B method")

# Creating objects
objA = A()
objB = B()

objA.show()  # Calls A's method
objB.show()  # Calls B's overridden method
```

> Output
> 
> This is Class A method  
> This is Class B method

**Explanation:**

- Both classes have a method `show()`.

- When `objB.show()` is called, **B's version overrides A's version**.

# Types of inheritance

## **Single Inheritance**

A child class inherits from only one parent class.

Simple one-to-one relationship.  
  

![[/image 1 16.png|image 1 16.png]]

```python
class A:
    def show_A(self):
        print("Class A Method")

class B(A):  # B inherits from A
    def show_B(self):
        print("Class B Method")

obj = B()
obj.show_A()
obj.show_B()
```

> Output
> 
> Class A Method  
> Class B Method

  

## **Multilevel Inheritance**

A chain of inheritance, where a class inherits from another child class.

Step-by-step inheritance like Grandparent → Parent → Child.

![[/image 2 10.png|image 2 10.png]]

```jsx
class A:
    def show_A(self):
        print("Class A Method")

class B(A):  # B inherits from A
    def show_B(self):
        print("Class B Method")

class C(B):  # C inherits from B (and indirectly from A)
    def show_C(self):
        print("Class C Method")

obj = C()
obj.show_A()
obj.show_B()
obj.show_C()
```

> Output
> 
> Class A Method  
> Class B Method  
> Class C Method

## **Multiple Inheritance**

A child class inherits from more than one parent class.  

![[/image 3 7.png|image 3 7.png]]

```python
class A:
    def show_A(self):
        print("Class A Method")

class B:
    def show_B(self):
        print("Class B Method")

class C(A, B):  # C inherits from A and B
    def show_C(self):
        print("Class C Method")

obj = C()
obj.show_A()
obj.show_B()
obj.show_C()
```

> Output
> 
> Class A Method  
> Class B Method  
> Class C Method

## **Hierarchical Inheritance**

Multiple child classes inherit from the same parent class.

When several classes share common features.

![[/image 4 7.png|image 4 7.png]]

```python
class A:
    def show_A(self):
        print("Class A Method")

class B(A):  # B inherits from A
    def show_B(self):
        print("Class B Method")

class C(A):  # C also inherits from A
    def show_C(self):
        print("Class C Method")

obj1 = B()
obj2 = C()

obj1.show_A()
obj1.show_B()

obj2.show_A()
obj2.show_C()
```

> Output
> 
> Class A Method  
> Class B Method  
> Class A Method  
> Class C Method

## **Hybrid Inheritance**

A combination of two or more types of inheritance.  
Used in complex programs where different relationships coexist.

![[/image 5 5.png|image 5 5.png]]

```python
class A:
    def show_A(self):
        print("Class A Method")

class B(A):  # Single inheritance
    def show_B(self):
        print("Class B Method")

class C(A):  # Hierarchical inheritance
    def show_C(self):
        print("Class C Method")

class D(B, C):  # Multiple inheritance
    def show_D(self):
        print("Class D Method")

obj = D()
obj.show_A()
obj.show_B()
obj.show_C()
obj.show_D()
```

> Output
> 
> Class A Method  
> Class B Method  
> Class C Method  
> Class D Method