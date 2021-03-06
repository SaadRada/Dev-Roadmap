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

- Introduction
- Data Types And Variables
- Numbers And Strings
- Control Flow
- Arrays
- Loop
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
