# Odd or Even

Write a program that reads a number from the user.

Print whether the number is odd or even

```python
num = int(input("Enter a number : "))
if num % 2 == 0:
    res = "Even"
else:
    res = "Odd"
print(f"Enter number {num} is {res}")
```

> Output
> 
> Enter a number : 3  
> Enter number 3 is Odd

# Largest among three numbers

Write a program that reads three numbers from the user.

Find the largest among the three numbers and print it.

## Method 1

```python
a = int(input("Enter first number : "))
b = int(input("Enter second number : "))
c = int(input("Enter third number : "))

if a > b and a > c:
    res = a
elif b > a and b > c:
    res = b
else:
    res = c

print(f"{res} is greater")
```

> Output
> 
> Enter first number : 1  
> Enter second number : 2  
> Enter third number : 3  
> 3 is greater

## Method 2

```python
a = int(input("Enter first number : "))
b = int(input("Enter second number : "))
c = int(input("Enter third number : "))

if a > b:
    if a > c:
        res = a
    else:
        res = c
else:
    if b > c:
        res = b
    else:
        res = c
  
print(f"{res} is greater")
```

> Output
> 
> Enter first number : 1
> 
> Enter second number : 2  
> Enter third number : 3  
> 3 is greater

  

# Simple Online Store

Consider you run an online store. You have the following items in you store: Laptop : 1 quantity, Mouse: 0(out of stock), Keyboard: 2 quantity.

Display the items details (name and quantity). Ask the choice of user and display the message saying that selected item is purchased.

Display the remaining items details (name and quantity).

```python
laptop = 1
mouse = 0
keyboard = 2
print(f"Items:\n1.Laptop:{laptop}, \n2.Mouse:{mouse}\n3.keyboard:{keyboard}")

item = int(input("Enter the item you want : "))
if item == 1:
    laptop -= 1
    print("You have purchased a Laptop")
elif item == 2:
    print("Sorry, mouse is not available")
elif item == 3:
    print("You have purchased a Keyboard")
    keyboard -= 1

print(f"Remaining Items:\n1.Laptop:{laptop}, \n2.Mouse:{mouse}\n3.keyboard:{keyboard}")
```

> Output
> 
> Items:  
> 1.Laptop:1,  
> 2.Mouse:0  
> 3.keyboard:2  
> Enter the item you want : 3  
> You have purchased a Keyboard
> 
>   
> Remaining Items:  
> 1.Laptop:1,  
> 2.Mouse:0  
> 3.keyboard:1

# Simple Calculator

Write a program to create a simple calculator that performs simple operations like +, - ,* and /

```python
print("""
Enter your choice:
      1. Addition : +
      2. Subtraction : -
      3. Multiplication : *
      4. Division : /
""")
choice = input("Enter your choice : ")
num1 = int(input("Enter 1st number : "))
num2 = int(input("Enter 2nd number : "))
if choice == '+':
    res = num1 + num2
elif choice == '-':
    res = num1 - num2
elif choice == '*':
    res = num1 * num2
elif choice == '/':
    res = num1 / num2
else:
    print("Invalid Input")

print(f"{num1} {choice} {num2} = {res}")
```

> Output
> 
> Enter your choice:  
> 1. Addition : +  
> 2. Subtraction : -  
> 3. Multiplication : *  
> 4. Division : /
> 
> Enter your choice : *  
> Enter 1st number : 2  
> Enter 2nd number : 3  
> 2 * 3 = 6