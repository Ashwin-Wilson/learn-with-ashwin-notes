# Introduction to Python
Python is created by Guido van Rossum.

It is popular for its simplicity and versatility. (Its syntax is user-friendly).

### Application of Python

- **Machine Learning, Deep Learning, Artificial Intelligence**

- **Web Applications**

- **Game Development**

- **Desktop Applications**

## Execution of Python program

- .py is the file extension for python

![[/image 46.png|image 46.png]]

Python uses a two-step process to execute programs, involving both compilation and interpretation:

- **Compilation to Bytecode:**
    
    - The source code is first compiled into an intermediate format called **bytecode**.
    
    - The resulting bytecode files have a `.pyc` extension.
    
    - This step is performed by the Python compiler.
    
    - This byte code can be implemented in any machine with a Python Virtual Machine(PVM) Installed
    

- **Interpretation of Bytecode:**
    
    - The bytecode is executed line by line by the **interpreter**.
    
    - The interpreter translates the bytecode into machine-specific instructions, enabling execution on your computer.
    
    - The PVM interprets and executes the bytecode.
    

## Some Important features of Python

**Portability**

Python is platform-independent, which means it can run on multiple operating systems like Windows, Linux, and macOS. Python programs are first compiled into an intermediate bytecode, which is then executed by the Python interpreter, ensuring consistency across platforms.

**Dynamically Typed**

Python is a dynamically typed language, meaning the type of a variable is determined at runtime. While this adds flexibility, it can also make Python slower compared to statically typed languages.

**Garbage Collection**

Python includes built-in garbage collection, which automatically manages memory by deallocating unused objects. This feature simplifies the programmer's job and helps prevent memory leaks.

## First Python Program

Create a python program filename.py

print “Hello world”

```python
print("Hello world")
```

> To run the program in terminal : python filename.py