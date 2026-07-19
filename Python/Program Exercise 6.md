# Test if Tuple is distinct

Check if all the elements in a tuple are distinct.

![[/image 60.png|image 60.png]]

```python
tp = (1, 2, 3, 4, 4, 5)
res = True
count = {}
for item in tp:
    count[item] = 1 + count.setdefault(item, 0)
for val in count.values():
    if val > 1:
        res = False
        break
print(res)
```

> Output  
> True

# Find common hobbies between two friends.

You are given a list of hobbies of your two friends. Find the common hobbies they have.

```python
f1 = ["reading", "music", "cricket"]
f2 = ["music", "traveling", "cricket"]
fs1 = set(f1)
fs2 = set(f2)
print(fs1 & fs2)
```

> Output  
> {'cricket', 'music'}

# Create a student database

Create a student database and perform the following operations

Insert students with details like roll no, name, mark

Feature to find students,

Feature to delete students

```python
students = {}
while True:
    print(students)

    print("""
    1. Enter student details
    2. Find a student
    3. delete a student
    4. Exit
    """)
    ch = int(input("Enter choice: "))
    
    if ch == 1:
        roll_no = int(input("\nEnter roll no: "))
        details = tuple(map(str, input("Enter name, mark: ").split()))
        students[roll_no] = details
    elif ch == 2:
        roll_no = int(input("\nEnter roll no: "))
        print(students.get(roll_no, "Student not found"))
    elif ch == 3:
        roll_no = int(input("\nEnter roll no: "))
        s = students.pop(roll_no, "No student")
        print(f"{s} is deleted")
    elif ch == 4:
        break
    else:
        print("Invalid choice")
```

# Character frequency counter

Read a string from the user and display the character count of the string.

## Method 1

```python
s = input("Enter a string: ")
count = {}
for ch in s:
    count[ch] = count.get(ch, 0) + 1
print(count)
```

> Output
> 
> Enter a string: hello  
> {'h': 1, 'e': 1, 'l': 2, 'o': 1}

## Method 2

```python
from collections import Counter
s = input("Enter a string: ")
count = Counter(s)
print(count)
```

> Output
> 
> Enter a string: hello  
> Counter({'l': 2, 'h': 1, 'e': 1, 'o': 1})