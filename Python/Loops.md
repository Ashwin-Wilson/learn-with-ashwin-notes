Loops are used to perform the same task multiple times.

The number of time a loop works is called its iteration.

# Why we need Loops ?

![[/image 51.png|image 51.png]]

  

**Without Loop**

```python
n = 3

i = 0
if i < n:
    print(i)
i += 1

if i < n:
    print(i)
i += 1

if i < n:
    print(i)
i += 1

if i < n:
    print(i)
i += 1
```

**With Loop**

```python
n = 3
i = 0
while i < n:
    print(i)
    i += 1
print("Hey")
```

> Output
> 
> 0  
> 1  
> 2

  

# Structure of a Loop

![[/image 1 8.png|image 1 8.png]]

# While loop

You can repeatedly execute a block of statements if a condition is true.

In the below code ‘i’ is the loop control variable.

Every statement that has proper indentation belong to the while loop’s block.

Program to print your name n times, were name and value of n is entered by user.

**Method 1**

```python
name = input("Enter your name : ")
n = int(input("Enter a number: "))
i = 0
while i < n:
    print(name)
    i += 1

print("Program executed successfully!")
```

> Output
> 
> Enter your name : Ashwin Wilson  
> Enter a number: 5  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Program executed successfully!

**Method 2**

```python
name = input("Enter your name : ")
n = int(input("Enter a number: "))

while n > 0:
    print(name)
    n -= 1

print("Program executed successfully!")
```

> Output
> 
> Enter your name : Ashwin Wilson  
> Enter a number: 5  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Ashwin Wilson  
> Program executed successfully!

## Infinite Loop

```python
while True:
    print("Hello")
```

To stop this click ==Ctrl + c==

- Reading values continuously from user without terminating the program

```python
while True:
    name = input("Enter your name: ")
    print(name)
```

# Break

It is a jump statement. It is used to break a loop.

```python
while True:
    name = input("Enter your name: ")
    print(name)
    if name == '0':
        break
```

The loop will break when the user enters ‘0’

# Continue

It is also a jump statement. It is used to skip an iteration of the loop.

![[/image 2 6.png|image 2 6.png]]

```python
for i in range(5):
    if i == 3:
        continue
    print(i, end=", ")
```

  

# For loop

Here also can repeatedly execute a block of statements if a condition is true.

Every statement that has proper indentation belong to the for loop’s block.

Here range() is used to get a sequence of numbers.

## range(stop)

Here you can decide where to stop. By default the starting value is 0

![[/image 3 5.png|image 3 5.png]]

```python
for i in range(5):
    print(i)
```

```python
for i in range(7):
    print(i)
```

### Print the sum of n numbers starting from 1. Where n is entered by user.

```python
n = int(input("Enter a number : "))
s = 0
for i in range(n+1):
    s += i
print(s)
```

> Output
> 
> Enter a number : 5  
> 15

## range(start, stop)

Here you can decide where to start and where to stop

![[/image 4 5.png|image 4 5.png]]

```python
for i in range(1, 5):
    print(i)
```

```python
for i in range(2, 7):
    print(i)
```

  

### Program to print the multiplication table of n, where n is entered by user.

```python
n = int(input("Enter a number : "))
for i in range(1, 11):
    print(f"{i} x {n} = {i*n}")
```

> Output
> 
> Enter a number : 2  
> 1 x 2 = 2  
> 2 x 2 = 4  
> 3 x 2 = 6  
> 4 x 2 = 8  
> 5 x 2 = 10  
> 6 x 2 = 12  
> 7 x 2 = 14  
> 8 x 2 = 16  
> 9 x 2 = 18  
> 10 x 2 = 20

## range(start, stop, step)

Here you can decide the start, stop and the step (updation)

![[/image 5 3.png|image 5 3.png]]

```python
for i in range(2, 20, 2):
    print(i, end=", ")
```

> Output
> 
> 2, 4, 6, 8, 10, 12, 14, 16, 18,

### Program to print odd numbers from 1 to n. Where n is entered by user

```python
n = int(input("Enter a number : "))
for i in range(1, n+1, 2):
    print(i, end=", ")
```

> Output
> 
> Enter a number : 20  
> 1, 3, 5, 7, 9, 11, 13, 15, 17, 19,

## Negative step

Here you can start from a large value and use negative value as step to reach a smaller value.

![[/image 6 3.png|image 6 3.png]]

In the below program we start from i=10

during each iteration we add -1 to i (i = i + -1)

If i is > 0 then we execute the while loop block.

```python
for i in range(10, 0, -1):
    print(i, end=", ")
```

> Output
> 
> 10, 9, 8, 7, 6, 5, 4, 3, 2, 1,

  

### Program to print sequence of numbers in reverse order starting from n to 0. Where n is entered by user

```python
n = int(input("Enter a number : "))
for i in range(n, 0, -1):
    print(i, end=", ")
```

> Output
> 
> Enter a number : 5  
> 5, 4, 3, 2, 1,

# Iterate a string

![[/image 51.png|image 51.png]]

len() is used to find the length of a string.

```python
name = input("Enter your name: ")
for i in range(len(name)):
    print(name[i])
```

> Output
> 
> Enter your name: Ashwin  
> A  
> s  
> h  
> w  
> i  
> n

# Nested Loop

Here you can write a loop inside another loop.

The loop outside is called outer loop and the one inside is called inner loop.

![[/image 7 3.png|image 7 3.png]]

```python
for i in range(3):
    print(i, end=': ')
    for j in range(4):
        print(j, end=', ')
    print()
```

> Output
> 
> 0: 0, 1, 2, 3,  
> 1: 0, 1, 2, 3,  
> 2: 0, 1, 2, 3,

  

![[/image 1 8.png|image 1 8.png]]