# What are Exceptions?

- Exceptions are runtime errors that occur while a program is running.

- If not handled, they will stop the program execution.

- Example: Dividing a number by zero → `ZeroDivisionError`.

# Why Handle Exceptions?

- To prevent the program from crashing.

- To display user-friendly messages instead of error codes.

- To gracefully continue execution even when errors occur.

# Keywords Used in Exception Handling

|**Keyword**|**Purpose**|
|---|---|
|**try**|Wrap the **risky code** that may cause an error.|
|**except**|Write **code to handle the error** if it occurs.|
|**else** _(optional)_|Runs **only if no error occurs** in the try block.|
|**finally** _(optional)_|Runs **no matter what**, used for **cleanup tasks** (e.g., closing files).|

# Basic Structure

```python
try:
    # Code that may cause error
    risky_code
except SomeError:
    # Code to handle the error
else:
    # Runs if no error occurs
finally:
    # Always runs (cleanup)
```

# Handling Division by Zero

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print("Result:", result)
except ZeroDivisionError:
    print("Error: Cannot divide by zero!")
```

# Handling Multiple Exceptions

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print("Result:", result)
except ZeroDivisionError:
    print("Error: Division by zero is not allowed.")
except ValueError:
    print("Error: Please enter a valid integer.")
```

# Using `else` and `finally`

```python
try:
    num = int(input("Enter a number: "))
    print("Square:", num * num)
except ValueError:
    print("Error: Invalid input! Enter a number only.")
else:
    print("No error occurred, calculation successful!")
finally:
    print("Program execution completed.")
```