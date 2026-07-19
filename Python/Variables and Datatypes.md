## Variables

![[/image 47.png|image 47.png]]

Variables in Python are containers used to store data in memory.

Python is a dynamically typed language, meaning you don’t need to declare the type of a variable explicitly.

A variable is created when a value is assigned to it.

### Data types

- **int :** To store integer data types. eg: 1, 2, 3, etc
    
    ```python
    a = 10
    print(a)
    ```
    

- **float :** To store decimal numbers eg: 10.5, 6.5, etc
    
    ```python
    mark = 10.5
    print(mark)
    ```
    

- **String** : To store strings like “Ashwin”, “Python”, etc
    
    ```jsx
    name = "Ashwin"
    print(name)
    print(name[0])
    ```
    
    - We can access each characters in string by using index
    
    - Strings are immutable (They can’t be modified)
    

- **Boolean Variables :** To store Boolean values (True or False)
    
    ```python
    a = True
    b = False
    print(a)
    print(b)
    ```
    

- **None** : Indicates that variable has no values
    
    ```python
    x = None
    print(x)
    ```
    

### type() function

It is used to check the type of a python variable

```python
roll_no = 1
name = "Ashwin"
mark = 10.5
print(type(roll_no))
print(type(name))
print(type(mark))
```

# String

Strings are used to store sequence of characters (a,b,c,… 1,2,3…., +,-,/,… $,…).

Strings are immutable(They are not modifiable).

Characters can be accessed by index.

Indexing starts from 0

![[/image 1 4.png|image 1 4.png]]