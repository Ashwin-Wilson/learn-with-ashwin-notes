# print()

print() is a function used to display messages on the screen (terminal).

prints the value inside the parentheses.

```python
print("Hello World")
print(1)
print(10.5)
```

> Output
> 
> Hello World  
> 1  
> 10.5

### print value of variables

```python
a = 10
b = 20.5
s = "Hello World"
print(a)
print(b)
print(s)
```

> Output
> 
> 10  
> 20.5  
> Hello World

### sep Parameter

It is used to specify the separator between multiple values. Default separator is space.

```python
print("24","08","2024", sep='-')
```

> Output
> 
> 24-08-2024

### end Parameter

It is used to specify what should be printed at the end of a print statement. Default value is newline character (”\n”)

- print at line ending
    
    ```python
    print("Hi", end="!")
    ```
    
    > Output
    > 
    > Hi!
    

- to avoid newline
    
    ```python
    print("Hello", end=" ")
    print("Ashwin")
    ```
    
    > Output
    > 
    > Hello Ashwin
    

  

# input()

input() is a function used to take input from user.

```python
s = input("Enter your name: ")
print(s)
```

> Output
> 
> Enter your name: Ashwin Wilson  
> Ashwin Wilson

- input() reads as strings
    
    ```python
    age = input("Enter your age: ")
    print(age)
    print(type(age))
    ```
    
    > Output
    > 
    > Enter your age: 20  
    > 20  
    > <class 'str'>
    

# Type conversion

In the previous program the age was read as string data type but we need it in integer datatype.

Here we can perform type conversion.

In type conversion we can convert a data in one type to another type.

## Types of type conversion

- Implicit type conversion
    
    - Here python automatically converts the datatype.
    
    - In the below program the ‘a‘ is integer and ‘b’ is float during addition the integer values is automatically converted into float
    
    ```python
    a = 10 \#type : integer
    b = 1.5 \#type : float
    s = a + b \#type : float
    print(s)
    ```
    
    > Output
    > 
    > 11.5
    
    - In the below code True is a boolean value and it is converted into integer (True = 1, Flase = 0) during addition.
    
    ```python
    a = 10 \#type : integer
    b = True \#type : boolean
    s = a + b \#type : integer
    print(s)
    ```
    
    > Output
    > 
    > 11
    

- **Explicit Type Conversion**
    
    - Here we manually convert one datatype to another using functions such as int(), float(), str(), list(), etc
    
    ```jsx
    age = input("Enter your age : ")
    age = int(age)
    print(age)
    print(type(age))
    ```
    
    > Output
    > 
    > Enter your age : 20  
    > 20  
    > <class 'int'>