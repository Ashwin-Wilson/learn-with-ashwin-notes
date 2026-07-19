# Print the triangle given below using “*”

![[/image 56.png|image 56.png]]

```python
num = int(input("Enter a number: "))
for i in range(num, 0, -1):
    for j in range(i):
        print("*", end=' ')
    print()
```

> Output:  
> Enter a number: 4  
> * * * *  
> * * *  
> * *  
> *

  

# Find the number of digits in a given number

![[/image 1 11.png|image 1 11.png]]

```python
num = int(input("Enter a number: "))
temp = num
count = 0
while temp != 0:
    count += 1
    temp = temp //10
print(f"Number of digits in {num} is: {count}")
```

> Output:
> 
> Enter a number: 1234  
> Number of digits in 1234 is: 4

# Reverse the number entered by user

Read a number from the user and print the reverse of that number.

```python
num = int(input("Enter a number: "))
temp = num
rev = 0
while temp != 0:
    rev *= 10
    rev += temp % 10
    temp = temp //10
print(f"Reverse of {num} is {rev}")
```

> Output:
> 
> Enter a number: 1234  
> Reverse of 1234 is 4321