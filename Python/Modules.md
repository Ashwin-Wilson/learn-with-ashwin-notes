# What is a Module?

- A module is a file containing Python code (functions, variables, or classes) that you can reuse in other programs.

- Helps to organize code into small, manageable parts.

- Python has built-in modules and you can also create your own modules.

# Using a Module

## Syntax:

```python
import module_name
```

or

```python
from module_name import specific_function
```

# Built-in Modules

## `math` Module – Mathematical Functions

```python
import math

print(math.sqrt(16))   # Square root
print(math.factorial(5))  # Factorial of 5
print(math.pi)          # Value of Pi
```

> Ouput
> 
> 4.0  
> 120  
> 3.141592653589793

## `random` Module – Generate Random Values

```jsx
import random

print(random.randint(1, 10))     # Random integer between 1 and 10
print(random.choice(['Apple', 'Banana', 'Mango']))  # Random choice
```

> Ouput
> 
> 5  
> Apple

## `datetime` Module – Work with Dates and Times

```python
from datetime import datetime

now = datetime.now()
print("Current Date and Time:", now)
print("Year:", now.year)
print("Month:", now.month)
```

> Ouput
> 
> Current Date and Time: 2025-09-05 22:58:08.063474  
> Year: 2025  
> Month: 9

## `time` Module – Time-related Functions

```jsx
import time

print("Start")
time.sleep(2)  # Pause for 2 seconds
print("End after 2 seconds")
```

> Ouput
> 
> Start  
> End after 2 seconds

# Renaming the Python Module

You can rename a module using `as` to make it shorter:

```jsx
import math as m

print(m.sqrt(25))
```

# Importing Specific Functions

```python
from math import sqrt, factorial

print(sqrt(36))
print(factorial(4))
```