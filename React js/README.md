# React js

![React js](https://masterscoding.com/wp-content/uploads/2020/06/Banner-817x400-05-scaled.jpg)

## Introduction

- React js is a free and open-source front-end JavaScript library for building user interfaces based on UI components. It is maintained by Meta and a community of individual developers and companies.
- Created by Meta(Facebook) on 2013

## Hello World

- create react application
  ```
  npx create-react-app app-name
  npx create-react-app . // current folder
  ```
- npx is a package runner to create react js applications withot instaling create-react-app globaly in our computer
- run app
  ```
  npm start
  ```

## Folder Structure

The main files :

- **package.json** : contain the dependencies and the scripts require for the project
- **gitignore** : ignored files on pushing
- **README** : Markdown file contain the documentation
- **node-modules** : Contain all dependencies (library, framworks ...)
- **public** : the main accesible folder that contain the signle page html **index.html**
- **src** : the most important folder, contain all applications components and assets
- **index** : starter point render the app component
- **app js** : the main component rendred in index js file
- **app css** : the style of the app component
- **index.css** : the style of the body tag

## Components

Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML. Components come in two types

- Class components : requires you to extend from React.Component and create a render function which returns a React element
- Function components : a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX)

## Hooks

Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

- useState
- useEffects
- useRef
- ...

## JSX

- JSX stands for JavaScript XML.
- JSX allows us to write HTML in React.
- JSX makes it easier to write and add HTML in React.

- JS code :
  ```
  const App = () => {
  return React.createElement("div", null, "Hello world!");
  };
  ```
- JSX code :
  ```
  const App = () => {
    return <div>Hello world!</div>
  }
  ```

## Props

- Props is an object passed with attributes and values
- Props allow us to reuse the same component with diffirent content
- Props are arguments passed into React components.
- Props are passed to components via HTML attributes.
- React Props are like function arguments in JavaScript and attributes in HTML.

- App Component
  ```
  import Car from "path";
  const App = () => {
    return(
      <div>
        <Car name="Dacia"/>
          <p>This is children props</p>
        <Car/>
        <Car name="Renault"/>
        </>
      <div/>
    )
  }
  ```
- Car Component
  ```
  const Car (props) => {
    return (
      <h2>{props.name}<h2/>
      {props.children}
    )
  }
  ```
- **NOTICE** : in class component should be use **this** keyword before props
  ```
    class Car extends Component {
    render() {
      return (
        <h2>{props.name}<h2/>
        {this.props.children}
      )
    }
  }
  ```

## State

- React components has a built-in state object.
- The state object is where you store property values that belongs to the component.
- When the state object changes, the component re-renders.
- state
- in a class component we will use the **constructor**
- **constructor** is a magic method used to initialize an object's state in a class, it automatically called during the creation of an object
- **super()** It is used to call the constructor of its parent class. This is required when we need to access some variables of its parent class

  ```
  import React, { Component } from 'react'

  export class App extends Component {

    constructor() {
      super()
      this.state = {
        message: "Hello Saad"
      }
    }

    changeMessage() {
      this.setState ({
        message: "Thank you for subscribing"
      })
    }

    render() {
      return (
        <div>
          <h1>{this.state.message}</h1>
          <button onClick={() => {this.changeMessage()}}>Subscribe</button>
        </div>
      )
    }
  }

  export default App
  ```
