# What is Global and local variables?

## Global variable

Global variables are defined outside a function or class.

Can be accessed inside and outside functions.

Cannot be modified inside a function without using `global` keyword.

## Local variable

Created inside a function and can be used only inside that function.

Not accessible outside the function.

In the below code, initially global variable was created.

Inside the function fun when ==a = 7== was used, it didn’t modify the global variable instead it created a new local variable which is only accessible within the function.

```python
a = 10 # global variable

def fun():
    a = 7 # local variable 
    print(f"Local variable: {a}")

fun()
print(f"Global variable: {a}")
```

> Output
> 
> Local variable: 7  
> Global variable: 10

# How to modify the global variable inside a function?

Use ==global== keyword.

```python
a = 10 

def fun():
    global a
    a = 7
    print(f"Global variable: {a}")

fun()
print(f"Global variable: {a}")
```

> Output
> 
> Global variable: 7  
> Global variable: 7