# Sass
![sass](https://www.webski.com.au/app/uploads/2015/11/what-is-sass.jpg)

## Introduction :
- Sass is stand for Syntacticaly Awesome Style Sheets
- Sass is a CSS pre-processor.
- Sass reduces repetition of CSS and therefore saves time.
- With Sass we can use Extend, variables, functions, loop and if condition
- Sass was designed by Hampton Catlin and developed by Natalie Weizenbaum in 2006

## Variables :
Variables are a way to store information that you can re-use later.

Sass Variable Syntax :
````
$variableName : value;
````
Example : 
````
$mainColor : red;
$containerWidth : 100%;
$font : 'Tahome', sans-serif;
$fontSize : 18px;
---- usage ----
div {
  color : $mainColor;
}
````
## Nesting : 
Sass lets you nest CSS selectors in the same way as HTML.

Example :
````
nav {
  ul {
    list-style : none;
  }
  li {
    display : inline-block;
  }
  a {
    text-decoration : none; 
  }
  &:hover {
    background-color : red; // = nav:hover
  }
}
````
& is stand for parent element
## Sass @import :
- Sass keeps the CSS code DRY (Don't Repeat Yourself). One way to write DRY code is to keep related code in separate files.

- You can create small files with CSS snippets to include in other Sass files. Examples of such files can be: reset file, variables, colors, fonts, font-sizes, etc.
- By default the Sass is compiling all .scss files so if we want to tell the the Sass to not compile a file (this file will bee imported) we need to use <strong>Sass Partials</strong>

Example : file _global.scss
````
@import 'global';
@use 'global';
````
## Extend : 
The <strong>@extend</strong> is using to not repeat css static values
Example : 
````
.container {
  width : 100%;
  background-color : #345EA6;
  text-align-center;
}
````
We can extend the container css values to another element
````
.home {
  @extend .container;
  display : grid;
  .....
}
````
## Placeholder
The placeholder is the same way to use extend 
but the extended element is note a class
is a placeholder element (faracha)

Example :
````
%allPagesStyle {
  width : 100%;
  padding : 20px;
  margin : 10px 0;
}
````
use it in another element :
````
.services {
  @extend %allPagesStyle;
  display : flex;
  ...
}
````

## Control Flow - If And Else :
````
.box {
  @if ($theme == 'light'){
    background-color : white;
    color : black;
  }
  @else {
    background-color : black;
    color : white;
  }
}
````
we can also use if else in one property
````
.box {
  width : 100%;
  background-color : if($theme == 'dark', black, white);
}