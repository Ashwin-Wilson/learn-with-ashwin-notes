# Draw a square using only ‘*’

![[/image 55.png|image 55.png]]

Draw a square using only “*”.

The dimension must be n x n, where n is entered by user.

```python
num = int(input("Enter a number: "))
for i in range(num):
    for j in range(num):
        print("*", end='')
    print()
```

> Output:  
> 
> Enter a number: 4
> 
> ****  
> ****  
> ****  
> ****

# Print the triangle given below using only ‘*’

Draw a triangle using only “*”.

The height and base must be n, where n is entered by user.

![[/image 1 10.png|image 1 10.png]]

```python
num = int(input("Enter a number: "))
for i in range(num):
    for j in range(i+1):
        print("*", end='')
    print()
```

> Output:  
> 
> Enter a number: 3
> 
> *
> 
> * *
> 
> * * *

  

# Find the number of vowels in give string

Read a string from user.

Find and print the number of vowels in the string.

![[/image 2 7.png|image 2 7.png]]

  

```python
name = input("Enter your name: ")
vowels = "aeiou"
count = 0
for i in range(len(name)):
    for j in range(len(vowels)):
        if name[i] == vowels[j]:
            count += 1
print(f"Number of vowels in {name}: {count}")
```

> Output:
> 
> Enter your name: ashwin  
> Number of vowels in ashwin: 2

# Multiplication quiz game

Read the number of students and number of questions to be asked to each students, from user.

Generate two random number and ask their product to the students.

If the answer is right then increment students score.

Otherwise show them the right answer.

```python
import random
num_s = int(input("Enter the number of students: "))
num_q = int(input("Enter the number of questions: "))
score = 0
for i in range(num_s):
    print(f"Let's start student {i}")
    for j in range(num_q):
        rand_num1 = random.randint(0,9)
        rand_num2 = random.randint(0,9)
        ans = int(input(f"What is {rand_num1} x {rand_num2} = "))
        if ans == rand_num1 * rand_num2:
            score += 1
            print(f"Correct answer! Score : {score}")
        else:
            print(f"Wrong answer! Answer is : {rand_num1 * rand_num2}")
            print(f"Score is  : {score}")
    score = 0
```

> Output:  
> 
> Enter the number of students: 2  
> Enter the number of questions: 2
> 
>   
> Let's start student 0  
> What is 8 x 9 = 72  
> Correct answer! Score : 1  
> What is 5 x 0 = 0  
> Correct answer! Score : 2
> 
>   
> Let's start student 1  
> What is 3 x 7 = 21  
> Correct answer! Score : 1  
> What is 2 x 5 = 11  
> Wrong answer! Answer is : 10  
> Score is : 1