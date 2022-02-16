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
}
````

## Sass @import :
- Sass keeps the CSS code DRY (Don't Repeat Yourself). One way to write DRY code is to keep related code in separate files.

- You can create small files with CSS snippets to include in other Sass files. Examples of such files can be: reset file, variables, colors, fonts, font-sizes, etc.
- By default the Sass is compiling all .scss files so if we want to tell the the Sass to not compile a file (this file will bee imported) we need to use <strong>Sass Partials</strong>

Example : file _global.scss
````
@import 'global';
@use 'global';
````
