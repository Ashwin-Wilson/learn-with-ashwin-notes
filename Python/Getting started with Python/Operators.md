# **Arithmetic operators**

Used to perform mathematical operations like addition, subtraction, multiplication, and division.

- Addition
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 + num2
    print(s)
    ```
    
    > Output  
    > 27
    

- Subtraction
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 - num2
    print(s)
    ```
    
    > Output  
    > 19
    

- Multiplication 
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 * num2
    print(s)
    ```
    
    > Output  
    > 92
    

![[/image 49.png|image 49.png]]

- Division 
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 / num2
    print(s)
    ```
    
    > Output  
    > 5.75
    
      
    

![[/image 1 6.png|image 1 6.png]]

- Modulo 
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 % num2
    print(s)
    ```
    
    > Output  
    > 3
    

-  Floor Division
    
    ```python
    num1 = 23
    num2 = 4
    s = num1 // num2
    print(s)
    ```
    
    > Output  
    > 5
    

![[/image 2 4.png|image 2 4.png]]

- Exponentiation 
    
    ```python
    num1 = 3
    num2 = 2
    s = num1 ** num2
    print(s)
    ```
    
    > Output  
    > 9
    

  

# **Assignment  Operators**

|   |   |   |
|---|---|---|
|Operator|How to use|Same As|
|=|x = 5|x = 5|
|+=|x += 3|x = x + 3|
|-=|x -= 3|x = x - 3|
|*=|x *= 3|x = x * 3|
|/=|x /= 3|x = x / 3|
|%=|x %= 3|x = x % 3|
|//=|x //= 3|x = x // 3|
|**=|x **= 3|x = x ** 3|

  

# **Operator Precedence and Associativity**

## **Operator Precedence**

Operators with higher precedence are evaluated before operators with lower precedence.

Precedence of the above operators are:

- ****** (Exponentiation)

- ***, /, //, %** (Multiplication, Division, Floor Division, Modulus)

- **+, -** (Addition, Subtraction)

```python
print(4 + 3 * 2)
print(5 + 4 * 3 ** 2)
```

> Output
> 
> 10  
> 41

  

## **Operator Associativity**

Associativity is the order in which operators of the same precedence are processed in an expression. It can be either left-to-right or right-to-left.

### **Left-to-Right Associativity:**

Addition ( **+** ) and Subtraction ( **-** ) operators are left-to-right associative. This means they are evaluated from left to right in the expression.

```python
print(6 + 7 - 3)
```

> Output
> 
> 10

### **Right-to-Left Associativity**

```python
print(3**2**3)
print((3**2)**3)
```

> Output
> 
> 6561  
> 729

  

  

# **Comparison Operators**

|   |   |   |
|---|---|---|
|Operator|Name|Example|
|==|Equal|x == y|
|!=|Not equal|x != y|
|>|Greater than|x > y|
|<|Less than|x < y|
|>=|Greater than or equal to|x >= y|
|<=|Less than or equal to|x <= y|

  

```python
a = 2
b = 2
if a == b:
    print("a and b are equal")
else:
    print("a and b are equal")
print(a == b)
```

> Output
> 
> a and b are equal  
> True

# Logical operators

![[/image 3 3.png|image 3 3.png]]

  

```python
print("AND")
print(False and False)
print(False and True)
print(True and False)
print(True and True)

print("\n\nOR")
print(False or False)
print(False or True)
print(True or False)
print(True or True)

print("\n\nNOT")
print(not False)
print(not True)
```

- Click to see Output
    
    > Output  
    > AND  
    > False  
    > False  
    > False  
    > True  
    >   
    > OR  
    > False  
    > True  
    > True  
    > True  
    >   
    > NOT  
    > True  
    > False
    
      
    
      
    

# Binary Representation

![[/image 4 3.png|image 4 3.png]]

  

## Binary Conversion using python

```python
print(bin(18))
```

> Output  
> 0b==10010==

# Bitwise Operators

## **Bitwise**  AND (&)

![[/image 5 2.png|image 5 2.png]]

```python
print("7: ", bin(7))
print("5: ",bin(5))
print("111 & 101 : ", bin(7&5))
print("7 & 5: ",7&5)
```

> Output
> 
> 7: 0b111  
> 5: 0b101  
> 111 & 101 : 0b101  
> 7 & 5: 5

## Bitwise OR (|)

![[/image 6 2.png|image 6 2.png]]

```python
print("7: ", bin(7))
print("5: ",bin(5))
print("111 | 101 : ", bin(7|5))
print("7 | 5: ",7|5)
```

> Output
> 
> 7: 0b111  
> 5: 0b101  
> 111 | 101 : 0b111  
> 7 | 5: 7

## **Bitwise XOR (^)**

![[/image 7 2.png|image 7 2.png]]

```python
print("7: ", bin(7))
print("5: ",bin(5))
print("111 ^ 101 : ", bin(7^5))
print("7 ^ 5: ",7^5)
```

> Output
> 
> 7: 0b111  
> 5: 0b101  
> 111 ^ 101 : 0b10  
> 7 ^ 5: 2

## **Bitwise NOT (~)**

### 1’s Compliment

Convert all the 1 to 0 and 0 to 1

![[/image 8 2.png|image 8 2.png]]

  

  

### 2’s Compliment

Add 1 to the 1’s compliment

![[/image 9 2.png|image 9 2.png]]

### **Bitwise NOT (~)**

![[/image 10 2.png|image 10 2.png]]

```python
print("5: ", bin(5))
print("~5: ", bin(~5))
print("-6: ",bin(-6))
```

> Output
> 
> 5: 0b101  
> ~5: -0b110  
> -6: -0b110
> 
>   

## Left shift (<<)

![[/image 11 2.png|image 11 2.png]]

```python
a = 5
print("5 : ", bin(a))
print("a << 1: ", bin(a << 1))
print("a << 2: ", bin(a << 2))
```

> Output
> 
> 5: 0b101  
> ~5: -0b110  
> -6: -0b110

## Right shift (<<)

![[/image 12 2.png|image 12 2.png]]

```python
a = 12
print("12 : ", bin(a))
print("a >> 1: ", bin(a >> 1))
print("a >> 2: ", bin(a >> 2))
```

> Output
> 
> 12 : 0b1100  
> a >> 1: 0b110  
> a >> 2: 0b11