# Reversing a List

## Method 1

```python
lt = [1, 2, 3, 4]
print(lt)
res = [
for i in range(len(lt)-1, -1, -1):
    res.append(lt[i])
print(res)
```

## Method 2

```python
lt = [1, 2, 3, 4]
res = lt[::-1]
print(res)
```

  

> Output
> 
> [1, 2, 3, 4]  
> [4, 3, 2, 1]

# Find Odd and Even items

From a list of numbers, create two separate list of odd and even numbers.

```python
lt = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
odd = []
even = []
for i in lt:
    if i % 2 == 0:
        even.append(i)
    else:
        odd.append(i)
print(f"Odd : {odd}")
print(f"Even : {even}")
```

> Output
> 
> Odd : [1, 3, 5, 7, 9]  
> Even : [2, 4, 6, 8, 10]

# Delete Duplicates

```python
fruits = ["Apple", "Orange", "Banana", "Mango", "Grapes", "Orange", "Apple"]
res = []
for fruit in fruits:
    if fruit not in res:
        res.append(fruit)
print(res)
```

> Output
> 
> ['Apple', 'Orange', 'Banana', 'Mango', 'Grapes']

# Shopping list

Write a program to create shopping list with following features.

Add items to the list.

Remove items from the list.

```python
shopping_lt = []
while True:
    item = input(f"\nShopping list: {shopping_lt}\n(press q to exit)\nEnter item to add to list: ")
    if item == 'q':
        break
    shopping_lt.append(item)
print("List inserting mode exited!\n\n")

while True:
    item = input(f"\nShopping list: {shopping_lt}\n(press q to exit)\nEnter the item to remove: ")
    if item == 'q':
        break
    if len(shopping_lt) == 0:
        print("List is empty")
        break
    if item not in shopping_lt:
        print("Item not in the list!\n\n")
        continue

    shopping_lt.remove(item)
```