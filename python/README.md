# Python
![python](https://geekflare.com/wp-content/uploads/2020/06/python-hosting-1200x385.jpg)

## Introduction

Python is a popular programming language. It was created by Guido van Rossum, and released in 1991.
It is used for:

- web development (server-side),
- software development,
- mathematics,
- system scripting.

## Python Syntax
Python syntax can be executed by writing directly in the Command Line:
````
>>> print("Hello, World!")
Hello, World!
````
Or by creating a python file on the server, using the .py file extension, and running it in the Command Line:
````
C:\Users\Your Name>python myfile.py
````
## Comments
- Comments can be used to explain Python code.
- Comments can be used to make the code more readable.
- Comments can be used to prevent execution when testing code.

Comments starts with a #, and Python will ignore them:
````
#This is a comment
print("Hello, World!")
````
## Variables
- ### Names
    Variables are containers for storing data values.

    Python has no command for declaring a variable.
    A variable is created the moment you first assign a value to it.
    ````
    x = 5
    y = "John"
    print(x)
    print(y)
    ````
- ### Casting
    If you want to specify the data type of a variable, this can be done with casting.
    ````
    x = str(3)    # x will be '3'
    y = int(3)    # y will be 3
    z = float(3)  # z will be 3.0
    ````
- ### Get the Type
    You can get the data type of a variable with the <strong>type()</strong> function.
    ````
    x = 5
    y = "John"
    print(type(x))
    print(type(y))
    ````
- ### Many Values to Multiple Variables
    Python allows you to assign values to multiple variables in one line:
    ````
    x, y, z = "Orange", "Banana", "Cherry"
    print(x)
    print(y)
    print(z)
    => Orange Banana Cherry
    ````
- ### One Value to Multiple Variables
    And you can assign the same value to multiple variables in one line:
    ````
    x = y = z = "Orange"
    print(x)
    print(y)
    print(z)
    => Orange Orange Orange
    ````
- ### Global Variables
    Create a variable outside of a function, and use it inside the function

    ````
    x = "awesome"

    def myfunc():
    print("Python is " + x)

    myfunc()
    => awesome
    ````
- ### The global Keyword
    If you use the <strong>global</strong> keyword, the variable belongs to the global scope:
    ````
    def myfunc():
    global x
    x = "fantastic"

    myfunc()

    print("Python is " + x)
    => Python is fantastic
    ````
## Data Types
| Data type   | Name    | Example         |
| ----------- | ------- | --------------- |
| Text        | str     |  "Hello Python" |
| integer     | int     | 12              |
| float       | float   | 10.5            |
| Table       | list    | ["apple", "banana", "cherry"] |
| tuple       | tuple   | ("apple", "banana", "cherry") |
| objet       | dict    | 










