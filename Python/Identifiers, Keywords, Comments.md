# Identifiers

They include variable name, function name, class name, etc

We can’t used keywords as Identifiers.

```python
num = 10
```

> Here ‘num’ is an identifier

# Keywords

They are reserved words that perform specific tasks in a programming language

They can’t be used as Identifiers.

```python
flag = True
if condition:
	....Statements
else:
	....Statements
```

> Here ‘True’ is a keyword  
> ’if’ & ‘else’ are also keywords

# Comments

They are used to explain what the code is doing.

They are not executed by the compiler.

Comments can be used to explain the logic behind the code.

We often forget the code logic after a while. Comments are helpful to remind the logic.

- Single line comment (use # in the beginning)
    
    ```python
    \#This code prints the value of a
    a = 10
    print(a)
    ```
    

- Multi-Line comment (if we have multiple lines to comment)
    
    ```python
    \#This code prints the value of a
    a = 10
    print(a)
    
    \#This code prints the value of b
    b = 20
    print(b)
    ```
    

- Docstring (documentation string)
    
    ```python
    a = 10
    b = 20
    	"""
    	This program is used to add the values 
    	variables are a & b
    	"""
    a + b
    ```