- Encapsulation is the process of binding data (attributes) and methods (functions) together into a single unit called a class.

- It is used to restrict direct access to some data to protect it from accidental changes.

- This is achieved by controlling access levels using public, protected, and private members.

```python
class Student:
    def __init__(self, name, marks):
        self.__name = name      # private attribute
        self.__marks = marks    # private attribute

    # Getter method to access private data
    def get_marks(self):
        return self.__marks

    # Setter method to update private data safely
    def set_marks(self, new_marks):
        if 0 <= new_marks <= 100:     # validation
            self.__marks = new_marks
        else:
            print("Invalid marks! Must be between 0 and 100.")

    def display(self):
        print(f"Name: {self.__name}, Marks: {self.__marks}")

# Create object
s = Student("Alice", 85)

s.display()               # Access data using method
print("Marks:", s.get_marks())

# Update marks using setter
s.set_marks(92)
s.display()

# Attempt to directly modify private variable (not allowed)
s.__marks = 50
s.display()  # No change because __marks is private

s.set_marks(101)
```

> Output
> 
> Name: Alice, Marks: 85  
> Marks: 85  
> Name: Alice, Marks: 92  
> Name: Alice, Marks: 92  
> Invalid marks! Must be between 0 and 100.