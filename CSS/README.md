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

## CSS unitis
The default font size for web page is 16px
- px
- em => time - element
- rem => Root time - Root element
- vw => ViewPort Width
- vh => ViewPort Height
- calc() => calculate values - calc (100% / 4)

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
    ![css display](https://codewebdao.com/upload/users/1/css/2019/inline-block/css-display-block-vs-inline-block.png)

    
    The <strong>display</strong> property specifies if/how an element is displayed.

    - Block
        - The block elements Take by default full width
        - Add Line Break
        - Respect padding, margin, width, height

    - Inline
        - The Inline elements Take by default element width
        - Do not respect width, height
        - Respect margin, padding [ just left and right ]

    - Inline-Block
        - The Inline elements Take by default element width
        - Respect padding, margin, width, height
        - Mix between block and inline

    - display:none
        - Hide The element
        - do not take the place after hidden
    - visibility:hidden
        - Hide The element
        - Still take the place after hidden
- ### Overflow
    - Hidden => hide element, data or anything outside the parent element
    - Scroll => hide element, data or anything outside the parent element and add Scrolling to see the hidden Data
- ### Text
    - Text-aligne : center || left || right
    - Text-shadow : Left Top Blur Color
    - Direction : ltr (left to right) || rtl (right to left)
    - vertical-align : top || middle || bottom
    - text-decoration : none || underline ...
    - text-transform : capitalize || uppercase || lowercase ...
    - line-height : value px
    - letter-spacing : value px
    - word-spacing : value px
- ### Fonts
    - font-family : font-name
    - font-style : italic ....
    -
    - font-size : value px
    - font-weight : bold || 100 to 900 px
## Position
![Css position](https://miro.medium.com/max/1400/1*eQ1bD3AL6BXU6-dszAxd1g.png)
## Box-Shadow
![box shadow](https://miro.medium.com/max/2000/1*2ZUhePZinwXfe8V7DtX79A.png)
- Box-Shadow : H-Shadow | V-Shadow | Blur | Spread | Color | Inset
    ````
    div {
        box-shadow : 1px 3px black;
    }
    ````
## Transition
- Transition : Property | Duration | Delay | Timing Fucntion
    ````
    div {
        width : 400px;
        transition : all 2s 1s easy-in-out
    }

    div:hover {
        width : 500px
    }
    ````
## !important Declaration
- The !important rule in CSS is used to add more importance to a property/value than normal.

- In fact, if you use the !important rule, it will override ALL previous styling rules for that specific property on that element!

````
p {
    color : red !important;
}
````
## Css Variables
- The css variables is using to make design color changes for one place
    ````
    :root {
        --mainColor : black;
    }

    p {
        color : var(--mainColor);
    }

    div {
        background-color : var(--mainColor);
        --divWidth : 200px;
    }
    ````
- The root is define that the variable is a global variable.
- The divWidth variable is a local variable.
- Now if we want to change color black for all template design, we will change only the variable value.
## Flex Box
- Flex Direction 
    ![flex-direction](https://dev-to-uploads.s3.amazonaws.com/i/n2ggh6yy4sbgltrx2i40.png)
    ![flex-direction](https://dev-to-uploads.s3.amazonaws.com/i/6m9fg4n5a114q1va3b9p.png)
    ````
    parent-element {
        display-flex : flex;
        display-direction : row | row-reverse | column | column-reverse;
        display-wrap : mo-wrap | wrap | wrap-reverse
    }
- Flex Wrap
    ![flex-wrap](https://dev-to-uploads.s3.amazonaws.com/i/fux9qc05e6rtat192vlm.png)
- Flex Flow
    Flex Flow is a mixing Between Flex Direction And Wrap
    ````
    parent-element {
        display : flex;
        flex-flow : colum wrap;
    }
- Justify Content
    ![justify content](https://dev-to-uploads.s3.amazonaws.com/i/a5lhkhbhi7hxwjgyvl5x.png)
    ![justify content](https://dev-to-uploads.s3.amazonaws.com/i/1vyg5nf1w7plistni582.png)
- Align items
    ![align items](https://dev-to-uploads.s3.amazonaws.com/i/kt25wxicd7vm8ddtmq0l.png)
- Align Content
    ![align Content](https://dev-to-uploads.s3.amazonaws.com/i/nqvvc2rhf0vx3czy0rnr.png)
    ![align Content](https://dev-to-uploads.s3.amazonaws.com/i/zeet3705rsmz77v66x3c.png)
- Flex grow, shrink and Order
    - grow
        ![flex grow](https://miro.medium.com/max/1838/1*43faUXdI5KbcSb_LbXO-Ng.png)
    - shrink
        ![flex shrink](https://samanthaming.gumlet.io/flexbox30/23-flex-shrink.jpg.gz)
    - order
        ![flex order](https://i7x7p5b7.stackpathcdn.com/codrops/wp-content/uploads/2015/02/order-illustration.png)
- Flex basis
    - flex basis work as a width in row direction
    and as a height in a column direction : 
        ![flex basis](https://i.stack.imgur.com/cBN2s.png)

## Filter
    - The filter property is used to add some filters to images
    - blur() : Add Blur to image
    - grayscale() : change image mode to grayscale
    - brightness() : Adjusts the brightness of the image.
    - ...
## Grid
![Grid](https://miro.medium.com/max/2000/1*m2Q3kRG9yl5WyNIyoe15XA.png)

- ### unitis :
    - px
    - %
    - auto
    - Fraction
    - Repeat()
    - Mix Between All
- ### grid-template-columns :
    - The grid template columns is specific how much layouts are in the column
        ```
        .container {
            display : grid;
            grid-template-columns : 1fr 1fr 1fr;
        }
        ```
- ### grid-template-rows & Gap :
    - The grid template rows is specific how much layouts are in the row
        ```
        .container {
            display : grid;
            grid-template-rows : 1fr 2fr 1fr;
        }
        ```
    - Gap is specific the space bitween The grid elements
        ```
        .container {
            display : grid;
            grid-template-columns : repeat(3, 1fr);
            gap : 10px 20px;
        }
        ```
- ### Align-content & justify-content :
    - The Same as The Flex Box
