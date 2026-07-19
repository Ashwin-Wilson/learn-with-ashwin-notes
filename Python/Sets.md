- A **set** is an **unordered**, **mutable**, and **unindexed** collection.

- Written using **curly braces** `**{}**` or `set()`.

- **No duplicate elements** are allowed.

```python
s = {1, 2, 3}
print(s)
print(type(s))
```

> Output
> 
> {1, 2, 3}  
> <class 'set'>

# Characteristics

## **Distinct Items**

Set always contains unique items.

Even though in the below code, there was two 3’s in the set only one 3 will be present in the set.

```python
s = {1, 2, 3, 3}
print(s)
```

> Output
> 
> {1, 2, 3}

## **Unordered**

Sets do not maintain any order.

If you add items to set in a particular order and print it may appear in any other order.

Here in the below print statements the order of set items might be different.

```python
s = {1, 2, 3}
print(s)
print(s)
```

> Output
> 
> {1, 2, 3}  
> {1, 3, 2}

## **No Indexing**

Unlike list, we cannot access set items with index.

## **Fast Operations**

Operations like _union_, _intersection_, and _difference_ are performed quickly on sets.

# Creating Set

## Using set() constructor

```python
lt = ["Ashwin", 20, "Valaxia"]
s = set(lt)
print(s)
```

> Output
> 
> {'Valaxia', 'Ashwin', 20}

## Using curly braces {}

```python
s = {"Ashwin", 20, "Valaxia"}
print(s)
```

> Output
> 
> {'Valaxia', 'Ashwin', 20}

# Adding items

## Using add()

It can be used to add single items

```python
s = {"Ashwin", 20}
print(s)

s.add("Valaxia")
print(s)
```

> Output
> 
> {'Ashwin', 20}  
> {'Valaxia', 'Ashwin', 20}

## Using update()

Used to add items from another collection like list or set itself.

```python
lt = [10, 20]
s = {"Ashwin", 50}
print(s)
s.update(lt)
print(s)
```

> Output
> 
> {'Ashwin', 50}  
> {'Ashwin', 10, 50, 20}

# Removing items

## Using remove()

Removes an item if it exists. If the item is not present, it raises an error.

```python
s = {1, 2, 3, 4, 5}
print(s)
s.remove(3)
print(s)
```

> Output
> 
> {1, 2, 3, 4, 5}  
> {1, 2, 4, 5}

## Using discard()

Removes an item if it exists. If the item is not present, it does nothing.

```python
s = {1, 2, 3, 4, 5}
print(s)
s.discard(3)
print(s)
```

> Output
> 
> {1, 2, 3, 4, 5}  
> {1, 2, 4, 5}

## Using clear()

Removes all the items in a set.

```python
s = {1, 2, 3, 4, 5}
print(s)
s.clear()
print(s)
```

> Output
> 
> {1, 2, 3, 4, 5}  
> set()

## Using del

Delete the entire set. The set can no longer be accessed. It returns error while accessing a deleted set.

```python
s = {1, 2, 3, 4, 5}
print(s)
del s
print(s)
```

> Output
> 
> {1, 2, 3, 4, 5}==Traceback (most recent call last):==  
> ==File "C:\Users\VICTUS\Desktop\Online tutorials\Python tutorial\code\[temp.py](http://temp.py/)", line 4, in <module>==  
> ==print(s)==  
> ==^==  
> ==NameError: name 's' is not defined==

# Set operations

## Union

Combine unique elements from 2 sets.

![[/image 59.png|image 59.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {4, 5, 6, 7}
print(s1 | s2)
```

> Output
> 
> {1, 2, 3, 4, 5, 6, 7}

## Intersection

Give common elements in both sets

![[/image 1 14.png|image 1 14.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {4, 5, 6, 7}
print(s1 & s2)
```

> Output
> 
> {4, 5}

## Difference

Give element in the fist set but not in the second set.

![[/image 2 8.png|image 2 8.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {4, 5, 6, 7}
print(s1 - s2)
```

> Output
> 
> {1, 2, 3}

## **Symmetric Difference**

Returns elements present in either set but not in both.

![[/image 3 6.png|image 3 6.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {4, 5, 6, 7}
print(s1 ^ s2)
```

> Output
> 
> {1, 2, 3, 6, 7}

## Disjoint set

Returns `True` if the two sets have no elements in common.

![[/image 4 6.png|image 4 6.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {4, 5, 6, 7}
s3 = {8, 9}
print(s1.isdisjoint(s2))
print(s1.isdisjoint(s3))
```

> Output
> 
> False  
> True

## Subset

Checks if all elements of the first set are in the second set.

![[/image 5 4.png|image 5 4.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {1, 2, 3}
s3 = {1, 2, 3, 4, 5}
s4 = {1, 2, 3, 4, 5, 6, 7}

print(s2 <= s1)
print(s3 <= s1)
print(s4 <= s1)
```

> Output
> 
> True  
> True  
> False

## **Proper Subset**

Similar to subset but does not allow both sets to be equal.

![[/image 6 4.png|image 6 4.png]]

```jsx
s1 = {1, 2, 3, 4, 5} 
s2 = {1, 2, 3}
s3 = {1, 2, 3, 4, 5}
s4 = {1, 2, 3, 4, 5, 6, 7}

print(s2 < s1)
print(s3 < s1)
print(s4 < s1)
```

> Output
> 
> True  
> False  
> False

## **Superset** 

Checks if the first set contains all elements of the second set.

![[/image 7 4.png|image 7 4.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {1, 2, 3}
s3 = {1, 2, 3, 4, 5}
s4 = {1, 2, 3, 4, 5, 6, 7}

print(s1 >= s2)
print(s1 >= s3)
print(s1 >= s4)
```

> Output
> 
> True  
> True  
> False

## **Proper Superset**

Similar to superset but does not allow both sets to be equal.

![[/image 8 3.png|image 8 3.png]]

```python
s1 = {1, 2, 3, 4, 5} 
s2 = {1, 2, 3}
s3 = {1, 2, 3, 4, 5}
s4 = {1, 2, 3, 4, 5, 6, 7}

print(s1 > s2)
print(s1 > s3)
print(s1 > s4)
```

> Output
> 
> True  
> False  
> False

# General set functions

## len()

Use to find the number of items in a set

```python
s1 = {1, 2, 3, 4, 5} 
print(len(s1))
```

> Output
> 
> 5

## max() and min()

To find the max() and min() item in a set.

```python
s1 = {1, 2, 3, 4, 5} 
print(max(s1))
print(min(s1))
```

> Output
> 
> 5  
> 1

## sum()

To find the sum of items in a set.

```python
s1 = {1, 2, 3, 4, 5} 
print(sum(s1))
```

> Output
> 
> 15

## Membership operator in set

To check if an items is present in the set or not.

```python
s1 = {1, 2, 3, 4, 5} 
print(3 in s1)
print(6 in s1)
```

> Output
> 
> True  
> False