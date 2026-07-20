A tuple is an ordered, immutable (unchangeable) collection in Python.

Defined using **round brackets** `**()**`.

Can store multiple data types.

```python
tp = (10, 20, "Ashwin")
print(tp)
print(type(tp))
```

> Output
> 
> (10, 20, 'Ashwin')  
> <class 'tuple'>

# Characteristics

## Ordered

Tuple always maintains the order of items.

```python
tp = (10, 20, "Ashwin")
```

Here the order of the items will be always the same

## Indexed

Tuple items can be accessed using index, similar to lists.

![[/image 58.png|image 58.png]]

```python
tp = (10, 20, "Ashwin")
\#using positive index
print(tp[2])
\#using negative index
print(tp[-1])
```

> Output
> 
> Ashwin  
> Ashwin
> 
>   

## Immutable

Tuple cannot be modified after it is created.

```python
tp = (10, 20, "Ashwin")
tp[0] = 1
```

This will return an error.

## Faster and Memory-efficient

They are faster and memory-efficient when compared to list.

# Creating tuples

Tuples can be created with or without parentheses.

```python
# with paranthesis
tp1 = (10, 20, "Ashwin")

# without paranthesis
tp2 = 10, 20, "Ashwin"
```

To create a single-item tuple, a comma must follow the item.

```python
tp = (4,)
```

# General Tuple Functions

## Length

Returns the number items in the tuple

```python
tp = (10, 20, "Ashwin")
print(len(tp))
```

> Output
> 
> 3

## Count

Returns the number of times a specified item appears in the tuple.

```python
tp = (10, 20, 10, 30, 40, 50)
print(tp.count(10))
```

> Output
> 
> 2

## Index

Returns the index of the first occurrence of a specified item.

```python
tp = (20, 10, 10, 30, 40, 50)
print(tp.index(10))
```

> Output
> 
> 1

# Slicing Tuples

It is similar to the slicing in list.

```python
tp = (10, 20, 10, 30, 40, 50)
print(tp[1:4])
```

> Output
> 
> (20, 10, 30)

# Tuple Packing & Unpacking

- **Packing**: Putting multiple values together into a single tuple.

- **Unpacking**: Extracting tuple elements into individual variables. The number of variables must match the number of elements in the tuple.

```python
tp = ("Ashwin", 20, "Developer")
name, age, job = tp
print(name)
print(age)
print(job)
```

> Output
> 
> Ashwin  
> 20  
> Developer

# Nested Tuples

- A nested tuple is a tuple that contains other tuples as its elements.

- Useful for storing structured data (like matrices, records, coordinates).

- Access elements using multiple indices.

![[/image 1 13.png|image 1 13.png]]

```python
t = (1, (2, 3), (4, 5))

print(t[1])     # Access inner tuple
print(t[2][1])  # Access element from nested tuple
```

> Output
> 
> (2, 3)  
> 5