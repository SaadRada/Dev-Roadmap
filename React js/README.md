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
