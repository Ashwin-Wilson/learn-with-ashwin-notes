Function are used to write reusable block of code.

They help in maintaining the program organized.

# Syntax

![[/image 61.png|image 61.png]]

**Function sample:**

program to add two numbers using function.

```python
def add(num1, num2):
    s = num1 + num2
    return s

res = add(2, 3)
print(res)
```

> Output  
> 5

# Parameters

Functions can accept input called parameters.

The below code accepts the age as a parameter and prints the age.

```python
def print_age(age):
    print(age)

print_age(20)
```

> Output  
> 20

# Return

Function can return values after performing the task.

**return** keyword is used for that.

The following code will accept your year of birth as input and print your age as output

```python
def age_calc(year_of_birth):
    age = 2025 - year_of_birth
    return age

age = age_calc(2004)
print(age)
```

> Output  
> 21

# Execution Flow

```python
def fun1():
    print("Before fun2")
    fun2()
    print("After fun2")


def fun2():
    print("Inside fun2")


print("Before fun1")
fun1()
print("After fun1")
```

> Output
> 
> Before fun1  
> Before fun2  
> Inside fun2  
> After fun2  
> After fun1

# Default Arguments

These are used to set predefined values to parameters.

Default arguments must be placed at the end.

```python
def print_bill(item, price=10):
    print(f"Item: {item}\nPrice: {price}")

print_bill("Flower")
print_bill("Apple", 50)
```

> Output
> 
> Item: Flower  
> Price: 10  
> Item: Apple  
> Price: 50

# Keyword Arguments

This allows you to specify the parameter by their name.

There are two types of arguments in python:

## Positional arguments:

Arguments that need to be in the same order as the parameters in the function definition.

```python
def print_bill(item, price):
    print(f"Item: {item}\nPrice: {price}")

print_bill("Apple", 10)
```

> Output
> 
> Item: Apple  
> Price: 10

## Keyword arguments:

- Arguments that can be provided in any order by explicitly specifying the parameter name.

```python
def print_bill(item, price):
    print(f"Item: {item}\nPrice: {price}")

print_bill(price=10, item="Apple")
```

> Output
> 
> Item: Apple  
> Price: 10

# Variable Length Argument

## Using positional arguments

We can pass parameters of different length in python by using * in-front of the parameter name.

The variable length argument will be a tuple.

```python
def var_len_arg(initial_val, *tp):
    print(initial_val)
    print(type(initial_val))
    print(tp)
    print(type(tp))

var_len_arg(0, 1, 2, 3, 4)
```

> Output
> 
> 0  
> <class 'int'>  
> (1, 2, 3, 4)  
> <class 'tuple'>

## Using keyword arguments

Here we can pass variable length parameters by using ** in-front of the parameter name.

The variable length argument will be a dictionary.

```python
def var_len_arg(**d):
    print(d)
    print(type(d))

var_len_arg(name="Ashwin", age=20, place='kerala')
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'place': 'kerala'}  
> <class 'dict'>

# Parameter passing

The parameters passed in a function behaves differently based on whether the parameter is mutable of immutable.

## Pass by value

Here an integer value is passed as argument which is immutable.

Therefore the variable ‘a’ inside the function and and the ‘a’ outside the function are different.

```python
a = 20
def sample(a):
    a = 10
    print("Inside function", a)
print("Outside function", a)
sample(a)
print("Outside function", a)
```

> Output
> 
> Outside function 20  
> Inside function 10  
> Outside function 20

## Pass by reference

Here a list is passed as argument which is mutable.

Therefore when the list inside the function and outside the functions are the same.

So when the ‘lt’ was changed inside the function it was reflected outside also.

```python
lt = ["Ashwin", "Kerala"]
def sample(lt):
    lt.append("valaxia")
    print("Inside function: ",lt)
print("Outside function: ",lt)
sample(lt)
print("Outside function: ",lt)
```

> Output
> 
> Outside function: ['Ashwin', 'Kerala']  
> Inside function: ['Ashwin', 'Kerala', 'valaxia']  
> Outside function: ['Ashwin', 'Kerala', 'valaxia']

# Returning multiple values

We can return multiple values from a function

## Using tuple

```python
def calc(a, b):
    sum_res = a + b
    mul_res = a * b
    return sum_res, mul_res

s, m = calc(2, 3)
print(f"Sum: {s}, Mult: {m}")
```

> Output
> 
> Sum: 5, Mult: 6

## Using list

```python
def calc(a, b):
    sum_res = a + b
    mul_res = a * b
    sub_res = a - b

    return [sum_res, mul_res, sub_res]

res = calc(3, 2)
print(f"Result: {res}")
```

> Output
> 
> Result: [5, 6, 1]

## Using Dictionary

```python
def calc(a, b):
    return {
            "sum_res": a + b,
            "mul_res": a * b,
            "sub_res": a - b
           }

res = calc(3, 2)
print(f"Result: {res}")
```

> Output
> 
> Result: {'sum_res': 5, 'mul_res': 6, 'sub_res': 1}