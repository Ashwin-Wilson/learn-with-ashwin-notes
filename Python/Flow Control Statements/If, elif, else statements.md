# Conditional Statement

They are used to execute a specific block of code if a condition is met.

In python “if-elif-else” can be used for implementing conditional statements.

# if statement

It is used to execute a block of code if the specified condition is true

![[/image 50.png|image 50.png]]

```python
num = int(input("Enter a number : "))
if num < 0:
    print("number is negative")
print("Entered number is : ", num)
```

> Output
> 
> Enter a number : -2  
> number is negative  
> Entered number is : -2

  

# if-else statement

It is used to execute a block of code if the specified condition is true and another block if condition is false.

![[/image 1 7.png|image 1 7.png]]

# **if-elif-else Statement**

```python
num = int(input("Enter a number : "))
if num < 0:
    print("number is negative")
else:
    print("number is positive")
```

> Output
> 
> Enter a number : 3  
> number is positive

  

It is used when multiple conditions has to be checked.

![[/image 2 5.png|image 2 5.png]]

```python
num = int(input("Enter a number : "))
if num < 0:
    print("number is negative")
elif num == 0:
    print("number is zero")
else:
    print("number is positive")
```

> Output
> 
> Enter a number : 0  
> number is zero

  

## if-else if ladder in python

  

![[/image 3 4.png|image 3 4.png]]

```python
num = int(input("Enter a number between 1 and 3: "))
if num == 1:
    print("number is 1")
elif num == 2:
    print("number is 2")
elif num == 3:
    print("number is 3")
else:
    print("Not a valid number")
```

> Output
> 
> Enter a number : 0  
> number is zero

## Nested if statement

![[/image 4 4.png|image 4 4.png]]

```python
age = int(input("Enter your age : "))

if age > 0:
    if age <= 18:
        print("Hello Baby!")
    else:
        print("Hello Bro!")
else:
    print("Enter a valid age!")

print("Your age is : ", age)
```

> Output
> 
> Enter your age : 18  
> Hello Baby!  
> Your age is : 18