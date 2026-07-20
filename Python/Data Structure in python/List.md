List are used to store a collection of items (values or data) of multiple data types.

Items can be of different data types (integer, float, string, etc)

```python
lt= [1, "Ashwin", 10.5]
print(lt)
print(type(lt))
```

> Output
> 
> ==[1, 'Ashwin', 10.5]==  
> ==<class 'list'>==

List items are not stored in continuous memory locations.

# Accessing list items (using index)

- List items can be accessed by index starting from 0.

  

![[/image 53.png|image 53.png]]

```python
lt = [1, "Ashwin", 10.5]
print(lt[0])
print(lt[1])
print(lt[2])
```

> Output
> 
> 1  
> Ashwin  
> 10.5
> 
>   

negative indexing is also supported where lt[-1] refers to the last item, lt[-2] refers the second last item and so on.

# Modifying list item

- python list are mutable, which means list items can be changed after creating them.

## **Appending items**

```python
l = [1, 2, 3, 4]
print(l)
l.append(5)
print(l)
```

> Output  
> [1, 2, 3, 4]  
> [1, 2, 3, 4, 5]

## **Inserting Items** (Insert item at specific location)

- Inserting an item to the specified index and shifting all the items at right side of new items towards right.

```python
l = [1, 2, 3, 4]
print(l)
l.insert(2, 10)
print(l)
```

> Output
> 
> [1, 2, 3, 4]  
> [1, 2, 10, 3, 4]

## **Change item at specific index**

- To change the item at a specific index in the list

```python
l = [1, 2, 3, 4]
print(l)
l[2] = 0
print(l)
```

> Output
> 
> [1, 2, 3, 4]  
> [1, 2, 0, 4]

# **Removing Items**

## Remove an item using remove() function

```python
l = [1, 2, 3, 4, 5, 6]
print(l)
l.remove(3)
print(l)
```

> Output
> 
> [1, 2, 3, 4, 5, 6]  
> [1, 2, 4, 5, 6]

## Remove an item by index (using pop() function)

```python
l = [1, 2, 3, 4, 5, 6]
print(l)
l.pop(1)
print(l)
```

> Output
> 
> [1, 2, 3, 4, 5, 6]  
> [1, 3, 4, 5, 6]

## using del keyword

```jsx
l = [1, 2, 3, 4, 5, 6]
print(l)
del l[4]
print(l)
```

> Output
> 
> [1, 2, 3, 4, 5, 6]  
> [1, 2, 3, 4, 6]

# Membership operator

## Checking for an item in a list

- Checking is an item is present in the list or not.

- “in” operator is called the membership operator.

```python
l = [1, 2, 3, 4]
print(1 in l)
print(6 in l)
```

> Output
> 
> True  
> False

## Checking if an items is not in a list

```jsx
l = [1, 2, 3, 4]
print(1 not in l)
print(6 not in l)
```

> Output
> 
> False  
> True

# General list functions

## **Counting Items**

- Counting the number of times an item appears in a list

```python
l = [1, 1, 3, 4, 5, 6]
print(l.count(1))
```

> Output  
> 2

## **Find Index of an Item**

- It gives the index where the item was found first.

```python
l = [1, 1, 3, 4, 5, 6]
print(l.index(1))
print(l.index(5))
```

> Output
> 
> 0  
> 4

## Find the Max, Min, Sum functions

```jsx
l = [1, 2, 3, 4, 5, 6]
print(max(l))
print(min(l))
print(sum(l))
```

> Output
> 
> 6  
> 1  
> 21

## Sort a list

```python
lt = [3,5,2,6,1,4]
print(f"Before: {lt}")
lt.sort()
print(f"After sorting: {lt}")
```

> Output
> 
> Before: [3, 5, 2, 6, 1, 4]  
> After reversing: [1, 2, 3, 4, 5, 6]

## **Reverse a List**

```python
lt = [1, 2, 3, 4, 5, 6]
print(f"Before: {lt}")
lt.reverse()
print(f"After reversing: {lt}")
```

> Output  
> [1, 2, 3, 4, 5, 6]

# Slicing

List slicing is used to select specific elements from a list.

![[/image 53.png|image 53.png]]

  

## start and end

- start is the index we want to begin from.

- Index to end the slice.

```python
lt = [1, 2, 3, 4, 5, 6]
\#here i want to select only the elements at the index ranging from 0 to 3(exculsive)
print(lt[0:3])
```

> Output  
> [1, 2, 3]

  

![[/image 1 12.png|image 1 12.png]]

## step

- Specify the interval between the elements.

```python
lt = [1, 2, 3, 4, 5, 6]
print(lt[0:5:2])
```

> Output  
> [1, 3, 5]

  

# Traversing a list

## Using indexing

```python
lt = [1, 2, 3, 4, 5, 6]
for i in range(len(lt)):
    print(lt[i])
```

> Output
> 
> 1  
> 2  
> 3  
> 4  
> 5  
> 6
> 
>   

## Using membership operator

```python
lt = [1, 2, 3, 4, 5, 6]
for i in lt:
    print(i)
```

> Output
> 
> 1  
> 2  
> 3  
> 4  
> 5  
> 6