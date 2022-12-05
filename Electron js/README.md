# Electron js

![electron](https://miro.medium.com/max/1400/1*pLdF3eiHQvT52YCnFtYiew.png)

## Introduction

Electron is a framework for building desktop applications using JavaScript, HTML, and CSS. By embedding Chromium and Node.js into its binary, Electron allows you to maintain one JavaScript codebase and create cross-platform apps that work on Windows, macOS, and Linux — no native development experience required.

## Create app

Electron apps follow the same general structure as other Node.js projects. Start by creating a folder and initializing an npm package.

```
mkdir my-electron-app && cd my-electron-app
npm init
```

```
{
  "name": "my-electron-app",
  "version": "1.0.0",
  "description": "Hello World!",
  "main": "main.js",
  "author": "Jane Doe",
  "license": "MIT"
}
```

```
npm install --save-dev electron
```

## Run App

the entry file by default is main.js

```
{
  "scripts": {
    "start": "electron ."
  }
}
```

```
npm run start
```
