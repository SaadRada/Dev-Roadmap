# Angular
![Angular](https://www.studide.in/wp-content/uploads/2021/09/angular-banner-1024x297.png)
- Angular is a javascript Or typescript Framework
- open source
- presented on 2009 by Google
- Allowing to Create SPA(single page application)

## What is SPA?
- SPA is stand for single page application
- An SPA (Single-page application) is a web app implementation that loads only a single web document, and then updates the body content of that single document via JavaScript APIs such as XMLHttpRequest and Fetch when different content is to be shown
![SPA](https://www.t2.sa/sites/default/files/inline-images/figure1.jpg)
- application has only one page for hHTML(index.html) contain all components
- the SPA page content is changed dynamicly with user interactivity

## Angular architecture MVVM
- MVVM is stand for Model View View Model
- Module : Data
- View : user interface
- View Module : is the Mediator between the View and the module
## Angular Component Architecture
- HTML for the views
- Css for styling
- TypeScript For Data Banding and Calculation Api ...
- Browser Can't understand TypeScript For that TypeScript is compile to be a javaScript code
## Install a Project
- Download Node js Last Version (npm)
- Download Angular CLI(Command Line Interface)
- Cli use for testing and compilation
  ```
  npm install -g @angular/cli / Last Version
  npm install -g @angular/cli@version
  ng version // check angular cli version
  ```
## Create a project
```
ng new projectName // Create new project
cd projectName // go to project
ng serve --open // open the project
```
## Angular Project Structure

<img src="https://www.ngdevelop.tech/wp-content/uploads/2017/12/Folder-Structure.png" align="right">

- <strong>e2e</strong> : Contain Files For Testing
- <strong>Node_modules</strong> : Contain necessary Files To Angular Work
- <strong>src</strong> : Contain source files
- <strong>package.json</strong> : Contain All Project Dependencies
- <strong>angular.json</strong> : CLI configuration defaults for all projects in the workspace, including configuration options for build, serve, and test tools that the CLI uses,
- <strong>tslint.json</strong> : 
