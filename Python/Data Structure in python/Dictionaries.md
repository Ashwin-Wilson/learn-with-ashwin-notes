- A **dictionary** is a collection of **key-value pairs**.

- Keys are **unique** and **immutable** (string, number, tuple).

- Values can be of any data type.

- Defined using **curly braces** `**{}**`.

```python
d = {
    "name":"ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
print(type(d))
```

> Output
> 
> {'name': 'ashwin', 'age': 20, 'company': 'Valaxia'}  
> <class 'dict'>

# **Characteristics** 

## Key-Value Pairs

The data is stored in a =={ key : value }== format

## Unique Keys

Keys must be unique

## Duplicate Values

Keys must be unique while values can be repeated

# Creating Dictionary

```python
d = {
    "name":"ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
```

> Output
> 
> {'name': 'ashwin', 'age': 20, 'company': 'Valaxia'}

# Accessing Items

## Using key and [ ]

This method will raise an error if the key doesn’t exist.

Without Error

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d['name'])
```

> Output
> 
> Ashwin

Error raised when the key doesn’t exist

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d["place"])
```

> Output
> 
> ==Traceback (most recent call last):==  
> ==File "C:\Users\VICTUS\Desktop\Online tutorials\Python tutorial\code\[temp.py](http://temp.py/)", line 6, in <module>==  
> ==print(d["place"])==  
> ==~^^^^^^^^^==  
> ==KeyError: 'place'==

## Using get()

This will not raise any error if the key doesn’t exist, instead it will return None.

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d.get("company"))
print(d.get("place"))
```

> Output
> 
> Valaxia  
> None

get() can also be used to return a default value if the key doesn’t exist

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d.get("company"))
print(d.get("place","Kerala"))
```

> Output
> 
> Valaxia  
> Kerala

# Adding Items

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
d['place'] = 'kerala'
print(d)
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia'}  
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia', 'place': 'kerala'}

# Updating items

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
d["name"] = "Ashwin Wilson"
print(d)
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia'}  
> {'name': 'Ashwin Wilson', 'age': 20, 'company': 'Valaxia'}

# Removing Items

## Using pop()

Removes the key-value pair and returns the value.

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
val = d.pop("age")
print(val)
print(d)
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia'}  
> 20  
> {'name': 'Ashwin', 'company': 'Valaxia'}

## Using popitem()

Remove and returns the last inserted key-value pair as a tuple.

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
val = d.popitem()
print(val)
print(d)
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia'}  
> ('company', 'Valaxia')  
> {'name': 'Ashwin', 'age': 20}

## Using del

Just deletes the key-value pair, doesn’t returns anything

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d)
del d["age"]
print(d)
```

> Output
> 
> {'name': 'Ashwin', 'age': 20, 'company': 'Valaxia'}  
> {'name': 'Ashwin', 'company': 'Valaxia'}

# General dict functions

## items()

This will return a view object of the dictionary.

It behaves like a list of tuples (key, value)

- This can be used to iterate over key value pairs.
    
    > Output
    > 
    > ```python
    > d = {
    >     "name":"Ashwin",
    >     "age":20,
    >     "company":"Valaxia"
    > }
    > for key, value in d.items():
    >     print(f"Key: {key}, Value: {value}")
    > ```
    > 
    > Key: name, Value: Ashwin  
    > Key: age, Value: 20  
    > Key: company, Value: Valaxia
    

Whenever the dictionary is updated the view object also get updated.

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
l = d.items()
print(l)
d['place'] = 'Kerala'
print(l)
```

> Output
> 
> dict_items([('name', 'Ashwin'), ('age', 20), ('company', 'Valaxia')])  
> dict_items([('name', 'Ashwin'), ('age', 20), ('company', 'Valaxia'), ('place', 'Kerala')])

## key()

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d.keys())
```

> Output
> 
> dict_keys(['name', 'age', 'company'])

## values()

To get the dictionary values only.

```python
d = {
    "name":"Ashwin",
    "age":20,
    "company":"Valaxia"
}
print(d.values())
```

> Output
> 
> dict_values(['Ashwin', 20, 'Valaxia'])

## setdefault()

Used to get the values using it’s key and set default values if the key does not exist.

```python
d = {
    "name":"Ashwin",
    "age":20
}
print(d.setdefault("name"))
d.setdefault("place", "Kerala")
print(d)
```

> Output
> 
> Ashwin  
> {'name': 'Ashwin', 'age': 20, 'place': 'Kerala'}