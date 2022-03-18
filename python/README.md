# Python :
## Introduction : 
- python is a high level general-purpose multi-platform Oriented   programming language
- Created on 1991 by Guido van Rossum
- python can use for :
  - web development (server-side)
  - Machine Learning
  - AI
  - software development
  - mathematics
  - system scripting
- File name extensions 
  - .py, .pyi, .pyc, .pyd, .pyo (prior to 3.5),[8] .pyw, .pyz (since 3.5)[9]
## Hello world
Python can be executed in a .py file or directly on command line
  ````
  print("Hello world");
  ````
## Comments
Ther's no way to create multi-line comments in python
in the example bellow it's just a string value
  ````
  # This is a python comment
  """
  This is a comment
  written in
  more than just one line
  """
  ````
## Variables
  - Declaration
    ````
    variableName = value
    x = 3
    name = "saad"
    ````
  - Casting (specify the data type of a variable)
    ````
    x = int(3)
    name = str("saad")
    ````
  - Get the data type of a variable
    ````
    x = 3
    name = "saad"
    print(type(x)) // int
    print(type(name)) // str
    ````
  - Case-Sensitive
    ````
    a = 4
    A = "Sally"
    #A will not overwrite a
    ````
  - Variable Names
    A variable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables:
      - Legal variable names:
        ````
        myvar = "John"
        my_var = "John"
        _my_var = "John"
        myVar = "John"
        MYVAR = "John"
        myvar2 = "John"
        ````
      - Illegal variable names:
        ````
        -myvar = "Jhon"
        2myvar = "John"
        my-var = "John"
        my var = "John"
        ````
  - Assign Multiple Values
    ````
    x, y, z = "Orange", "Banana", "Cherry"
    x = y = z = "Orange" // The same value for all variables
    ````
## Data Type
| Data type   | Example |
|----------|:-----------|
| int      |  integer : 3 |
| float |    3.1  |
| complex | 1j |
| str     | string : "saad" |
| list    | Tbale : [1, "saad", 2.5, 1j] |
| tuple   | ("apple", "banana", "cherry") |
| dict    | Object : {"name" : "John", "age" : 36} |
| bool    | True, False |
### Python Collections (Arrays)
-There are four collection data types in the Python programming language:
  - List is a collection which is ordered and changeable. Allows duplicate members.
  - Tuple is a collection which is ordered and unchangeable. Allows duplicate members.
  - Set is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.
  - Dictionary is a collection which is ordered** and changeable. No duplicate members.
## Strings

- ### Basics
  - x = 'saad'
  - get lenght : len(x)
  - index : x[0] // s
  - get type : type(x) // str
  - Check String : "sa" in x // check if sa in saad return true
  - Check if NOT : "sa" not in x // return false
- ### Slicing
  - Get the characters from position 2 to position 5 (not included):
    ````
    b = "Hello, World!"
    print(b[2:5])
    ````
  - ### Modify string
    - Upper Case : x.upper()
    - Lower Case : x.lower()
    - Remove Whitespace : x.strip()
    - Replace : x.replace("s", "q")
    - Split : x.split(",")
- ### Concatenate String
  ````
  a = "saad"
  b = "rada"
  c = a+b
  print(c) // saadrada
  ````
- ### Lists (Tables)
  - x = [1, "saad", true, 5.2]
  - get lenght : len(x)
  - index : x[0] // 1
  - get type : type(x) // <class = 'list'>
  - #### Acces list items :
    - get the last index : x[-1] // 5.2
    - get range : x[1:2] // saad true
    - check if item exist : 
      ````
      if 1 in x :
        print true
      ````
      
