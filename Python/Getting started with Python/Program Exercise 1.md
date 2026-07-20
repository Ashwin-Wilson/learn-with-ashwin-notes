## To add the values

![[/image 48.png|image 48.png]]

```python
a = 10
b = 20
s = a + b
print(s)
```

## To swap values

Program to swap the values in two variables.

![[/image 1 5.png|image 1 5.png]]

Usual approach

```python
a = 10
b = 20
print(a, b)
temp = a
a = b
b = temp
print(a, b)
```

Python way!

```python
a = 10
b = 20
print(a, b)
a, b = b, a
print(a, b)
```

## First Error

NameError in python.

Error occurred because variable ‘a’ is not defined (No values is assigned to it).

```python
print(a)
```

> Error:
> 
> ==Traceback (most recent call last):==  
> ==File "C:\Users\VICTUS\Desktop\Online tutorials\Python tutorial\code\[test.py](http://test.py/)", line 1, in <module>==  
> ==print(a)==  
> ==^==  
> ==NameError: name 'a' is not defined==

## To calculate the total mark

```python
bio = 80.4
math = 90.5
phy = 95.9
chem = 85.3
total_mark = bio + math + phy + chem
print(total_mark)
```

## To print full name

```python
first_name = "first_name"
last_name = " last_name"
full_name = first_name + last_name
print(full_name)
```

- number inside “ ” is considered as string itself

```python
a = '1'
b = '2'
print(a + b)
```