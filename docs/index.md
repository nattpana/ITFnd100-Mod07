# ITFnd100-Mod07_Assignment_07
*Natta Panapornsirikun, 05,31,23*

## Introduction
Learning Python on week 07

## Topic 1 : Research Exception Handling in Python
There are at least two distinguishable kinds of errors: syntax errors and exceptions.

### 1) Syntax Errors :
Program displays a little ‘arrow’ pointing at the earliest point in the line where the error was detected. The error is caused by (or at least detected at) the token preceding the arrow.

### 2) Exception Errors:
Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. Errors detected during execution are called exceptions and are not unconditionally fatal: you will soon learn how to handle them in Python programs. Most exceptions are not handled by programs.
Python's exception handling allows you to catch and handle errors that occur during the execution of your code. The basic syntax for exception handling is the try-except block.
These exceptions are predefined in the Python language and are categorized into different types based on their nature and the kind of errors they represent. Here are some common types of exceptions in Python:
    ZeroDivisionError: Raised when division or modulo operation is performed with zero as the divisor.
    TypeError: Raised when an operation or function is applied to an object of an inappropriate type.
    ValueError: Raised when a function receives an argument of the correct type but an invalid value.
    IndexError: Raised when an index is out of range for a sequence (such as a list or a string).
    KeyError: Raised when a dictionary key is not found.
    FileNotFoundError: Raised when an attempt is made to open a file that does not exist.
    ImportError: Raised when a module or package cannot be imported.
    NameError: Raised when a local or global name is not found.
    OverflowError and UnderflowError: Raised when a calculation exceeds the maximum or minimum representable value.
    IOError: Raised when an input/output operation fails.
Ref: Type of Erroers: https://docs.python.org/3/tutorial/errors.html   
     How to build in Exception: https://docs.python.org/3/library/exceptions.html
     Type of Exceptions: https://realpython.com/python-exceptions/
     Type of Exceptions: :https://www.geeksforgeeks.org/python-exception-handling/#
     
## Topic 2: Research Pickling in Python
In Python, we work with high-level data structures such as lists, tuples, and sets. However, when we want to store these objects in memory, they need to be converted into a sequence of bytes that the computer can understand. This process is called serialization. The next time we want to access the same data structure, this sequence of bytes must be converted back into the high-level object in a process known as deserialization.

We can use formats such as JSON, XML, HDF5, and Pickle for serialization. In this tutorial, we will learn about the Python Pickle library for serialization. We will cover its uses and understand when you should choose Pickle over other serialization formats. 

Finally, we will learn how to use Pickle Python library to serialize lists, dictionaries, Pandas data frames, machine learning models, and more.
Object serialization may be the solution you’re looking for.

It is the process of storing a data structure in memory so that you can load or transmit it when required without losing its current state.

Here is a simple diagram explaining how serialization works:
Python offers three different modules in the standard library that allow you to serialize and deserialize objects:
    The marshal module
    The json module
    The pickle module
    
The marshal module is the oldest of the three listed above. It exists mainly to read and write the compiled bytecode of Python modules, or the .pyc files you get when the interpreter imports a Python module. So, even though you can use marshal to serialize some of your objects, it’s not recommended.
- Don’t use the marshal module. It’s used mainly by the interpreter, and the official documentation warns that the Python maintainers may modify the format in backward-incompatible ways.

The json module is the newest of the three. It allows you to work with standard JSON files. JSON is a very convenient and widely used format for data exchange.
- The json module and XML are good choices if you need interoperability with different languages or a human-readable format.
 
The pickle module implements binary protocols for serializing and de-serializing a Python object structure. Pickling is a process in Python that allows you to serialize objects into a byte stream and store them in a file or transfer them over a network. This serialized byte stream can later be deserialized to reconstruct the original object. Pickling is useful for tasks such as saving and loading data structures, caching objects, or transferring objects between different Python programs.
- The Python pickle module is a better choice for all the remaining use cases. If you don’t need a human-readable format or a standard interoperable format, or if you need to serialize custom objects, then go with pickle.

Inside the Python Pickle Module
The Python pickle module basically consists of four methods:

    pickle.dump(obj, file, protocol=None, *, fix_imports=True, buffer_callback=None)
    pickle.dumps(obj, protocol=None, *, fix_imports=True, buffer_callback=None)
    pickle.load(file, *, fix_imports=True, encoding="ASCII", errors="strict", buffers=None)
    pickle.loads(bytes_object, *, fix_imports=True, encoding="ASCII", errors="strict", buffers=None)

The first two methods are used during the pickling process, and the other two are used during unpickling. The only difference between dump() and dumps() is that the first creates a file containing the serialization result, whereas the second returns a string.

To differentiate dumps() from dump(), it’s helpful to remember that the s at the end of the function name stands for string. The same concept also applies to load() and loads(): The first one reads a file to start the unpickling process, and the second one operates on a string.

Ref: What is pickle:https://docs.python.org/3/library/pickle.html
     Types of Modules: https://realpython.com/python-pickle-module/
     Python tutorial:  https://www.tutorialspoint.com/python-pickling
     Introduction to Pickle in Python:  https://www.datacamp.com/tutorial/pickle-python-tutorial
     What is Pickle in Python: https://favtutor.com/blogs/pickle-python
     
## Summary
Exception handling and pickling are key concepts in Python. Exception handling allows you to catch and handle errors during program execution, improving robustness and user experience. 
    Pickling involves serializing objects into byte streams for storage or transmission. It enables saving and loading data structures and facilitates object transfer between Python programs. Understanding exception handling and pickling enhances error management and data persistence in Python programming.

