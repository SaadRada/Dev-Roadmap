# HTML5

## What is HTML?
 - HTML stands for Hyper Text Markup Language
 - HTML is the standard markup language for creating web pages

## HTML syntax
````
<!DOCTYPE html>
<html>
    <head>
        .....
    </head>
    <body>
        .....
    </body>
</html>
````
 - <strong>!DOCTYPE html</strong> declaration defines that this document is an HTML5 document
 - <strong>html</strong> element is the root element of an HTML page
 - <strong>head</strong> not vissible for user contain
 - <strong>body</strong> element is the vissible page for user

 ## Links pages
 the link element is using to link the html page with other pages 
 like css page or JavaScript page

 Exemple
 ````
 <link rel="stylesheet" href="link.css">
 <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
 <script src="link.js"></script>
 ````



 ## HTML headings
 HTML heading is using to create titles or subtitles

 Exemple
````
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
````
<h1> Heading1 </h1>
<h2> Heading2 </h2>
<h3> Heading3 </h3>
<h4> Heading4 </h4>
<h5> Heading5 </h5>
<h6> Heading6 </h6>

# Paragraphe
A paragraph always starts on a new line, and is usually a block of text.

Exemple
````
<p>lorem ipsum text</p>
````

## HTML links
The html <strong>a</strong> tag defines a hyperlink

Exemple
````
 <a href="link.extension">Text</a>
````

## HTML images
Images can improve the design and the appearance of a web page.

Exemple
````
<img src="link.png" alt="text if image not found">
````
 
 ## HTML tables
 HTML tables arrange data into rows and columns.

Exemple
````
<table>
    <th>
        <td>name</td> <td>age</td>
    </th>
    <tr>
        <td>name</td> <td>age</td>
    </tr>
</table>
````

## HTML lists
HTML lists  group a set of related items in lists.
- <strong>ul</strong> unorder list
- <strong>ol</strong> order list

Exemple
````
<ul>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
<ul>
````
- item 1
- item 2
- item 3

Exemple
````
<ol>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
<ol>
````
1. item1
2. item2
3. item3

## HTML forms
An HTML form is used to collect user input. The user input is most often sent to a server for processing.

Exemple
````
<form action="link.php" method="POST OR GET">
    <label for="email">email</label>
    <input type="email" name="enail" id="email">
    <label for="pass">password</label>
    <input type="password" name="pass" id="pass">
    <input type="submit" value="login">
</form>
````
#### input types 
- <strong>text</strong> to input a sample text
- <strong>email</strong> to input a email format
- <strong>password</strong> to input a hidding text format
- <strong>date</strong> to input a date format
- <strong>tel</strong> to input a phone format
- <strong>number</strong> to input a number format
- <strong>checkbox</strong> to check values
- <strong>checkbox</strong> to choise values
- <strong>file</strong> to upload a file
- ...

## HTML media

<strong>HTML video</strong>

````
<video width="" height="" controls autoplay muted>
    <src ="video.mp4">
    <src ="video.avi">
</video>
````

<strong>HTML audio</strong>

````
<audio width="" height="" controls autoplay muted>
    <src ="audio.mp3">
    <src ="audio.ogg">
</audio>
````
## HTML Semantic Elements
![html semantic](https://www.w3schools.com/html/img_sem_elements.gif)
````
<article>
<aside>
<details>
<figcaption>
<figure>
<footer>
<header>
<main>
<mark>
<nav>
<section>
<summary>
<time>
````
