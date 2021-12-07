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


