# Function that returns grade of a student

Write a function that returns the grade of a student based on marks provided as input.

```python
def get_grade(marks):
    if marks >= 90:
        return "A"
    elif marks >= 80:
        return "B"
    elif marks >= 50:
        return "C"
    else:
        return "F"

print("Grade:", get_grade(82))
```

> Output  
> Grade: B

# Check if string is palindrome of not using functions

Write a function to check if a given string is palindrome of not.

```python
def is_palindrome(s):
    if s == s[::-1]:
        return True
    else: 
        return False

s = input("Enter a string: ")
res = is_palindrome(s)
print("Result: ", res)
```

> Output
> 
> Enter a string: malayalam  
> Result: True

# Find the correct order of the functions

Find the correct order to call the functions below to get the output “Hello World”

```python
def fun1():
    print("o", end=' ')
def fun2():
    fun4("Wor")
    print("ld")
def fun3():
    print("He", end='')
    fun5("ll")
def fun4(s):
    print(s, end='')
def fun5(s):
    print(s, end='')
    fun1()
```

- Answer
    
    ```python
    fun3()
    fun2()
    ```
    

> Output
> 
> Hello World

# Function to find Nth Prime number

```python
def is_prime(num):
    r = int(num ** 0.5)
    for i in range(2, r+1):
        if num % i == 0:
            return False
    return True
def nth_prime(n):
    num = 1
    while n != 0:
        num += 1
        if is_prime(num):
            n -= 1
    return num
n = int(input("Enter the a number: "))
res = nth_prime(n)
print(f"{n}th prime number is {res}")
```

> Output
> 
> Enter the a number: 3  
> 3th prime number is 5