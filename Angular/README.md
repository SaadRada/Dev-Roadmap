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
<img src="https://camo.githubusercontent.com/ec556857dc74243cf84e12fa140fdc104c6b77de395bd1a00314457dc5cdb89d/68747470733a2f2f7777772e6e67646576656c6f702e746563682f77702d636f6e74656e742f75706c6f6164732f323031372f31322f466f6c6465722d5374727563747572652e706e67" alt="Structure" data-canonical-src="https://www.ngdevelop.tech/wp-content/uploads/2017/12/Folder-Structure.png" style="max-width: 50%; float:left;margin-right:5px">

- <strong>e2e</strong> : Contain Files For Testing
- <strong>Node_modules</strong> : Contain necessary Files To Angular Work
- <strong>src</strong> : Contain source files
- <strong>package.json</strong> : Contain All Project Dependencies
- <strong>angular.json</strong> : CLI configuration defaults for all projects in the workspace, including configuration options for build, serve, and test tools that the CLI uses,
- <strong>tslint.json</strong> : 
