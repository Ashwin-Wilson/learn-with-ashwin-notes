# What is Polymorphism?

- Polymorphism means "many forms".

- In Python OOP, it allows one function name or method to perform different tasks, depending on the object or data type.

- Goal: Write flexible and reusable code.

## Real-Life Example

- A person can act as:
    
    - **Student** in a classroom,
    
    - **Customer** in a shop,
    
    - **Player** in a sports club.
    
    > Same person, different roles → Polymorphism!
    

# Polymorphism with Classes

```python
class Dog:
    def sound(self):
        print("Dog barks")

class Cat:
    def sound(self):
        print("Cat meows")

# Polymorphism in action
for animal in (Dog(), Cat()):
    animal.sound()  # Same method name, different behavior
```

> Output
> 
> Dog barks  
> Cat meows

Explanation:

- Both `Dog` and `Cat` have a method named `sound()`.

- Python calls the method based on the object type at runtime.

# Polymorphism with Method Overriding

Already discussed with Inheritance

# Built-in Polymorphism

- Python has built-in functions that work with different data types.

- The behavior of these functions changes based on the type of object passed.

- Example: `len()`, `max()`, `min()`, etc.

```python
# len() works with multiple data types
print(len("Hello"))       # String → Counts characters
print(len([1, 2, 3]))     # List → Counts elements
print(len((10, 20, 30)))  # Tuple → Counts elements
```

> Output
> 
> 5  
> 3  
> 3

Explanation:

- Same function `len()` → behaves differently depending on whether it receives a string, list, or tuple.

- This is built-in polymorphism.

# Operator Overloading Polymorphism

- In Python, operators are polymorphic, meaning the same operator performs different actions depending on the data type of operands.

- This is called Operator Overloading.

```python
# '+' operator behaves differently
print(10 + 20)            # Adds numbers
print("Hello " + "World") # Concatenates strings
print([1, 2] + [3, 4])    # Merges lists
```

> Output
> 
> 30  
> Hello World  
> [1, 2, 3, 4]

Explanation:

- The `+` operator:
    
    - **Adds** integers,
    
    - **Concatenates** strings,
    
    - **Merges** lists.
    

- Same operator, different behavior based on operands → Operator Overloading.