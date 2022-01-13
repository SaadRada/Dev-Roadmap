# CSS3
![css](https://fullstack-dev.netlify.app/desc-images/css3.jpeg)

## What is CSS?

- CSS is stands for cascading style sheets
- CSS describes how HTML elements are to be displayed on screen

## CSS syntax
````
selector {
    property : value;
}
````
![css sytnax](https://www.w3schools.com/css/img_selector.gif)

## CSS selectors

1. Nature select

    ````
    div {
        background-color : red;
    }
    ````
2. class,id select

    ````
    .className {
        background-color : red;
    }
    #idName {
        color : white;
    }
    ````
3. attribute select

    ````
    input[pleacholder] {
        background-color : red;
    }
    ````
4. Combinators select

    1. descendant selector (space)
        ````
        all p element inside a div
        div p {
            background-color : red;
        }
        ````
    2. child selector (>)
        ````
        all direct shildren
        nav > li {
            padding : 5px;
        }
        ````
    3. adjacent sibling selector (+)
        ````
        all h1 directly after a div
        div + h1 {
            color : crimson;
        }
        ````
    4. General Sibling Selector (~)
        ````
        all brothers p after a div
        div ~ p {
            color : crimson;
        }
        ````
5.CSS Pseudo-elements & classes
- 1.elements
    - after
    - before
    - first-line
    - first-letter
    - Maker
    - selection
        ````
        selector::pseudo-element {
        property: value;
        }
        ````
- 2.classes
        ![all css pseudo classes](http://ways2web.weebly.com/uploads/5/4/4/8/54485903/3112201_orig.png)

## CSS simple styling
- ### color
    ````
    p {
        color : red;
    }
    ````
- ### backgrounds
    - background-color
    - background-image
    - background-position
    - background-size
    - background-repeat
    - background-attachement
    - background : (mix between all before values)
    ````
    main {
        background-color : red;
        background-image : url("path/file.ext");
        background-size : cover;
        background-repeat : no-repeat;
        background-attachement : fixed;
        background : url("..") color image repeat position;
    }
    ````
- ### border
    ````
    border : type size color;
    div {
        border : solid 1px black;
    }
    ````
- margin & padding
  - padding : inside space
  - margin  : outside space
  ````
  p {
    padding : 10px;
    margin  : 5px;
  }
  ````
- ### height & width
  ````
  body {
      width  : 100%;
      height : 100vh;
  }
  ````
- ### Box model
![box model](https://www.lilengine.co/sites/default/files/inline-images/Screen%20Shot%202019-04-14%20at%2023.59.07.png)
- ### Display
    The <strong>display</strong> property specifies if/how an element is displayed.

    - Block
        - The block elements Take by default full width
        - Add Line Break
        - Respect padding, margin, width, height
            <div style="border:1px solid green;padding:5px;margin:5px">Block element</div><div style="border:1px solid green;padding:5px;margin:5px">Block element</div>
    - Inline
        - The Inline elements Take by default element width
        - Do not respect width, height
        - Respect margin, padding [ just left and right ]
        <span style="border:1px solid green;display:inline;margin:5px;padding:5px">Inline element</span> <span style="border:1px solid green;display:inline;margin:5px;padding:5px">Inline element</span>
    - Inline-Block
        - The Inline elements Take by default element width
        - Respect padding, margin, width, height
        - Mix between block and inline
        <span style="border:1px solid green;display:inline-block;margin:5px;padding:5px">Inline element</span> <span style="border:1px solid green;display:inline-block;margin:5px;padding:5px">Inline element</span>
    - display:none
        - Hide The element
        - do not take the place after hidden
    - visibility:hidden
        - Hide The element
        - Still take the place after hidden
- ### Overflow
    - Hidden => hide element, data or anything outside the parent element
    - Scroll => hide element, data or anything outside the parent element and add Scrolling to see the hidden Data


