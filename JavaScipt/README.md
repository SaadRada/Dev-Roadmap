# JavaScript

![javascript](https://coursework.vschool.io/content/images/2016/03/javascript-logo-banner.jpg)

# What is javaScript?

javaScript is a high-level object-oriented multi-paradigm programming language Designed on 1995 by Brendan Eich used to :

- Create web applications
- Create dynamic SPA(signle page application) with React, angular or vue js
- Create backEnd applications with nodejs express js ...
- Create Mobile applications (React Native, ionic...)
- Create desktop applications (electron js)

# What we will Learn?

- [x] Introduction
- [x] Data Types And Variables
- [x] Numbers And Strings
- [x] Control Flow
- [x] Arrays
- [x] Loop
- Functions & Scope
- Higher Order Functions And Practice
- Objects
- Document Object Model [DOM]
- Browser Object Model [BOM]
- Destructuring
- More Methods And New Data Types
- Regular Expressions
- Object Oriented Programming
- Date, Time, Generators And Modules
- JSON
- Asynchronous JavaScript Programming

# Introduction

- ## Were to put the code
  ```
  <!DOCTYPE html>
  <html>
    <head>
      meta...
      link...
      <script src="path.js"> // bad
    </head>
    <body>
      <h1>Hello js</h1>
      <script src="path.js"> // good
    </body>
  </html>
  ```
- ## Comments
  ```
  // single line comment
  /*
    multiple
    line
    comment
  */
  ```
- ## Output to screen
  alert : popup that stop loading the rest of code
  log : output in the console
  document.write : write directly in the document page
  ```
  window.alert(1);
  console.log(1);
  document.write(1);
  ```
- ## Console Methods And WebAPI
  - log : console-log(1)
  - error : console.error("error");
  - table : console.table(["saad", "rada", 20])
- ## What Is ECMAScript ?

  - ECMAScript is a JavaScript standard meant to ensure the interoperability of web pages across different web browsers. It is standardized by Ecma International according to the document ECMA-262

  - ECMAScript 6, also known as ECMAScript 2015, is the latest version of the ECMAScript standard. ES6 is a significant update to the language, and the first update to the language since ES5 was standardized in 2009. Implementation of these features in major JavaScript engines is underway now.

- ## Data Type
  to get the data type of a variable we can use <strong>typeof()</strong>
  - String : "saad" OR 'saad'
  - Number : 10 OR 10.1
  - Array => object : [1, 2, 3, 4]
  - Object : {name: "saad", age: 20, contry: "morocco"}
  - Boolean : true false
  - undifined
  - null
- ## Variables

  in the first javascript is a loosely typed language

  - In programming we call a language loosely typed when you don't have to explicitly specify types of variables and objects. A strongly typed language on the contrary wants types specified.

  ```
  var name = value;
  var 1name // not working
  var _name // workinng
  var name with special caracteres not working
  ```

- ## Var vs Let Vs Const
  ![jjs scopr](https://cdn.hashnode.com/res/hashnode/image/upload/v1600864549731/CPpg9u2gi.png)
  - var
    - Redeclare - yes
    - Access Before Decalre - Undifined
    - Variable Scope Drama - Added to window
  - let
    - Redeclare - No
    - Access Before Decalre - Error
  - cont
    - is a constant value that can't change
    - Redeclare - No
    - Access Before Decalre - Error
- ## Escape Operator
  ```
  consol.log("saad 'rada'") => saad 'rada'
  consol.log('saad "rada"') => saad "rada"
  consol.log("saad "rada"") => ERROR
  consol.log('saad 'rada'') => ERROR
  consol.log('saad \'rada\'') => saad 'rada'
  consol.log('saad \n rada') => saad
  rada
  ```
- ## Concatinate and Template Literals

  ```
  var name = "saad";
  var lastName = "rada";

  alert(a +" "+ b);
  ```

  with backtick

  ```
  var name = "saad";
  var lastName = "rada";

  alert(`${a} ${b}`);
  ```

# Numbers

- Methods :

  - toString() : convert number to string

    ```
    (100).toString() // "100"
    100..toString() // "100"
    ```

  - Number() : convert string to number, return NAN if not a number

    ```
    Number("100") // 100
    ```

  - toFixed(n) : 12.44444.toFixed(2) : return 12.44 as a string
    ```
    12.444444.toFixed(2) // 12.44
    ```
  - parseInt() : convert string to number (int)
    ```
    parseInt("320.2") // 320
    parseInt("100 saad") // 100
    ```
  - parseFloat() : convert string to number (float)
    ```
    parseFloat("320.5") // 320.5
    parseInt("100.2 saad") // 100.2
    ```
  - Number.isInteger() : return true if integer
    ```
    Number.isInteger(2) // true
    Number.isInteger(2.3) // false
    ```
  - Number.isNan() : return true if not a number
    ```
    Number.isNan("saad") // true
    Number.isNan(12) // false
    ```

- Math Object :
  - Math.round() :
    ```
    Math.round(2.3) // 2
    Math.round(2.7) // 3
    ```
  - Math.ceil() :
    ```
    Math.ceil(12.1) // 13
    ```
  - Math.floor() :
    ```
    Math.floor(11.9) // 11
    ```
  - Math.min() & Math.max() :
    ```
    Math.min(1, 10, -2, 3, 0) // -2
    Math.max(20, 101, -5, 33) // 101
    ```
  - Math.random() :
    ```
    Math.random() // return random number between 0 and 1
    ```
  - Math.trunc() :
    ```
    Math.trunc(99.5) // 99 return the integer value
    ```

# Strings

- Methods :

  - length
    ```
    let name = "ahmad";
    console.log(name.length); // 5
    ```
  - access index
    ```
    let name = "saad";
    console.log(name[0]); // s
    ```
  - charAt()
    ```
    console.log(name.charAt(1)); // a
    ```
  - trim() : remove spaces
    ```
    let lastName = "    rada  ";
    console.log(lastName.trime()); // rada
    ```
  - toUpperCase()
    ```
    console.log(name.toUpperCase()); // SAAD
    ```
  - toLowerCase()
    ```
    let name = "SaaD";
    console.log(name.toLowerCase()); // saad
    ```
  - indexOf()
    ```
    let text = "Hello everyone im saad from morocco";
    console.log(text.indexOf("o")); // the first o - position 4
    ```
  - lastIndexOf()
    ```
    let text = "Hello everyone im saad from morocco";
    console.log(text.lastIndexOf("o")); // the last o - position 34
    ```
  - slice()
    ```
    let text = "lorem text value";
    console.log(text.slice(3)); // em text value
    console.log(text.slice(3, 8)); // em te
    console.log(text.slice(-4)); // value
    ```
  - repeat()
    ```
    let name = "saad";
    console.log(name.repeat(3)); // saadsaadsaad
    ```
  - split()
    ```
    let fullName = "Saad Rada";
    console.log(fullName.split()); // ["Saad Rada"]
    console.log(fullName.split(" ")); // ["Saad", "Rada"]
    console.log(fullName.split("")); // ["S", "a", "a", "d", "R", "a", "d", "a"]
    ```

  # Control Flow

  - #### Comparison Operators
    - == : Compare Value Only
    - === : Compare Value and Data Type
    - != : Not equales values
    - !== : Not equales Value and data type
    - > : greater than
    - > = : greater than or equale
    - < : less than
    - <= : less than or equale
  - #### Logical Operators
    - && : and
    - || : or
    - ! : not
  - #### if condition

    ```
    if(condition){
      do something
    }
    else {
      do something else
    }
    ```

  - #### Ternary Operator
    ```
    condition ? do something : do something else
    condition ? do something : another condition ? do another something : do something else
    ```
  - #### Nullish Coalescing Operator And Logical Or

    It is used to replace Null , Undifined and 0 with other values

    || : replace Null, Undifined and 0
    ?? : replace Null and Undifined

    ```
    let price

    console.log(`the price is ${price || 100}`); // price is undifined the outpout will be => the price is 100

    let user = null

    console.log(`Welcome ${user || "UNKNOWN user"}`);
    ```

  - #### Switch Statement

    ```
    let day = 1;

    switch(day) {
      case 0 : console.log("sunday"); break:
      case 1 : console.log("monday"); break;
      // multiple case
      case 2 :
      case 3 : console.log("multiple case")
      default : console.log("Unknown");
    }
    ```

# Arrays

- Create an array

  ```
  let pc = ["Macbook pro m1", "Asus ROG", "Hp EliteBook"];
  ```

- Access Arrays ELements

  ```
  console.log(pc[0]); // Macbook pro m1
  ```

- Nested Arrays

  ```
  console.log(pc[0][0]); // M
  ```

- Change Arrays Elements

  ```
  pc[0] = "Macbook pro 2019";
  console.log(pc);
  // Macbook pro 2019, Asus ROG, Hp EliteBook
  ```

- Check is Array

  ```
  Array.isArray(pc) // true
  ```

- Array length

  ```
  console.log(pc.length) // 3
  ```

- ### Array Methods

  #### Add And Remove Fron Array

  - ##### unshift : add in the first

    ```
    let array = [1, 2, 3];

    array.unshift(5);
    // [5, 1, 2, 3]
    ```

  - ##### push : add in the last

    ```
    let array = [1, 2, 3];

    array.push(4);
    // [1, 2, 3, 4]
    ```

  - ##### shift : remove the first case

    ```
    let array = [1, 2, 3];

    array.shift();
    // [2, 3]
    ```

  - ##### pop : remove the last case

    ```
    let array = [1, 2, 3];

    array.pop();
    // [1, 2]
    ```

  #### Array Searching

  - ##### indexOf and lastIndexOf (Return index)

    ```
    let names = ["Saad", "Moncef", "Abderahem", "Zoubair", "Saad"]

    console.log(names.indexOf("Saad")); // 0
    console.log(names.indexOf("Abderahem")); // 2
    console.log(names.lastIndexOf("Saad")); // 4
    console.log(names.indexOf("Amine")); // -1 Not Found
    ```

  - ##### includes (Return Boolean Value)

    ```
      let names = ["Saad", "Moncef", "Abderahem", "Zoubair"]

      console.log(names.includes("Saad")); // true
      console.log(names.indexOf("amine")); // false
    ```

  #### Array Basic Sorting

  - ##### Sort and R everse

    alphabetically sorting from 0 1 ... to a b c...

    ```
    let arr = [90, -10, 0, "saad", 500, "100"];

    console.log(arr.sort()); // [-10, 0, 100, 500, 90, "saad"]
    ```

    ```

    let arr = [90, -10, 0, "saad", 500, "100"];

    console.log(arr.reverse()); // ["100", 500, "saad", 0, -10, 90]

    ```

  #### Slice and Splice

  The slice() method returns selected elements in an array, as a new array.

  The slice() method selects from a given start, up to a (not inclusive) given end.

  The slice() method does not change the original array.

  ```
  let n = [1, 2, 3, 4]

  n.slice(1) // [2, 3, 4]
  n.slice(1, 4) // [2, 3]
  ```

  The splice() method adds and/or removes array elements.

  The splice() method overwrites the original array.

  ```
  let arr = [10, 5, 3]

  arr.splice(in position, remove, add)
  arr.splice(2, 0, 1,2) // [10, 5, 1, 2, 3]
  ```

  #### Concat and Join

  The concat() method creates a new array by merging (concatenating) existing arrays:

  ```

  let os = ["mac os", "linux", "windows"];
  let pc = ["MacBook Air", "Hp EliteBook", "Asus ROG"];

  let all = os.concat(pc); // ["mac os", "linux", "windows", "MacBook Air", "Hp EliteBook", "Asus ROG"]
  let allWithNew = os.concat(pc, "Dell", ["Android", "IOS"]); // ["mac os", "linux", "windows", "MacBook Air", "Hp EliteBook", "Asus ROG", "Dell", "Android", "IOS"]

  ```

  The join() method also joins all array elements into a string.

  It behaves just like toString(), but in addition you can specify the separator:

  ```

  let os = ["mac os", "linux", "windows"];

  os.join() // mac os, linux, windows
  os.join("") // mac oslinuxwindows
  os.join("|") // mac os|linux|windows

  ```

# Loops

- ### For loop

  ```
  for (start, end, increment) {
    // do something
  }

  for (let i = 0; i<10; i++) {
    consol.log(i); // 1 2 3 .... 9
  }
  ```

- ### Break, Continue, Label

  - Break : End the loop
  - Continue : Skip the curent index from loop
  - label : break specific loop

    ```
    mainLoop : for(let i = 0; i<10; i++){
      if(condition){
        continue; // skip
      }
      nestedLoop for(let j=0; j<5; j++){
        if(condition) {
          break; // break this loop
          break mainLoop; // break specific loop
        }
      }
    }
    ```

- ### While loop
  ```
  while (true) {
    // do this
  }
  ```
- ### Do While Loop
  ```
  do {
    // this
  }while(true)
  ```

# Function

- A function is simply a “chunk” of code that you can use over and over again, rather than writing it out multiple times
- Built in Functions : is a function that is already available in a programming language
- User Defined Functions : is a function that is created by the programmer
- Basic Function :

  ```
  function name() {
    do something
    return something;
  }

  // call function
  name()
  ```

- Function with parameters :

  ```
  function calc(num1, num2) {
    return num1 + num2;
  }

  calc(10,20); // 30
  ```

- Function parametrs default value :

  ```
  function sayHello(name = "Unknow") {
    return `Hello ${name}`;
  }

  sayHello("saad"); // Hello saad
  sayHello(); // Hello Unknown
  ```

- Function Rest parametrs

  ```
  function calc(...numbers) {
    let result = 0;

    for(let i=0; i<numbers.length; i++) {
      result += numbers[i];
    }

    return result;
  }

  calc(10, 20, 30); // 60
  calc(5, 10, 40, 20, 10) // 85
  ```

- Anonymous Function

  ```
  calc(1, 2) // Undifined Function

  let calc = function (num1, num2) {
    return num1 + num2;
  }

  calc(1, 2) // return 3
  ```

- Arrow Function

  ```
  let calc = function (num1, num2) {
    return num1 + num2
  }

  let calc = (num1, num2) => num1 + num2;

  // if the function has 1 parametre
  let sayHello = name => `Hello ${name}`;
  ```

# Higher Order Functions

Hugher Order Function is a function that accepts Functions as a parametrs

- ### Map

  ```
  let array = [1, 2, 3, 4, 5, 6];

  let addition = array.map(element, index, arr) {
    element // 1
    index // 0
    arr // [1, 2, 3, 4, 5, 6]
    this // 10
  }, 10);
  ```

- ### Filter

  ```
  let friends = ["Saad", "Ahmed", "Said", "Amine"];

  // if the return is true, return the curent element
  let filtredFriends = friends.filter((el) => el.startWith("A")) // Ahmed, Amine
  ```
