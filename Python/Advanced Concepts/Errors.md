- **Errors** are issues in a program that **stop it from running correctly**.

- Python shows error messages to help you **identify and fix problems** in the code.

# **Syntax Error**

Occurs when the **Python code is not written correctly** according to rules (grammar of the language).

```python
# Missing colon at the end of 'if'
if 5 > 2
    print("Five is greater than two")
```

# Runtime Error

Occurs **while the program is running**, even if the syntax is correct.

Example includes dividing by zero:

```python
print(10 / 0)
```

# Logical Error

The code **runs without crashing**, but **produces incorrect results** due to a mistake in logic.

```python
# Program to calculate average
total = 90
count = 2
average = total * count  # Wrong logic! Should be total / count
print("Average is:", average)
```

# Name Error

Occurs when you **use a variable or function that doesn’t exist**.

```python
print(age)  # 'age' is not defined
```

# Type Error

Occurs when you **perform an operation on incompatible data types**.

```python
num = 10
text = "Age"
print(num + text)  # Cannot add int and string
```

# Index Error

Occurs when you **access an index that doesn’t exist** in a list or tuple.

```python
fruits = ["Apple", "Banana"]
print(fruits[5])  # Index 5 doesn't exist
```

# Key Error

Occurs when you **access a non-existent key** in a dictionary.

```python
student = {"name": "Alice", "age": 20}
print(student["grade"])  # 'grade' key does not exist
```

# Attribute Error

Occurs when you **call a method or attribute that doesn’t exist** for an object.

```python
text = "Hello"
text.push("World")  # Strings don't have 'push' method
```

# Indentation Error

Occurs when **code is not properly indented**.

```python
if True:
print("Hello")  # No indentation
```

# Import Error

Occurs when Python **cannot find the module** you are trying to import.

```python
import my_fake_module  # This module does not exist
```

# Value Error

Occurs when the **data type is correct**, but the **value is inappropriate**.

```python
num = int("abc")  # Cannot convert letters to integer
```