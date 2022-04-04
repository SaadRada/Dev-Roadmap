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
- <strong>package.json</strong> : Contain All Project Dependencies
- <strong>angular.json</strong> : CLI configuration defaults for all projects in the workspace, including configuration options for build, serve, and test tools that the CLI uses,
- <strong>tslint.json</strong> : TSlint check Typescript code for readability, maintainability, and functionality errors.
- (:warning: TSLint has been deprecated as of 2019)
- <strong> tsconfig.json </strong> : contain Typescript configuration
- <strong>src</strong> : Contain source files
  - <strong> assets </strong> : Contains image and other asset files to be copied as-is when you build your application
  - <strong> index.html </strong> : The Main page visible to the user that contain the compomemts
  - <strong> styles.css </strong> : The global css file Vissible to all components
  - <strong> app </strong> : Contains the component files in which your application logic and data are defined. has 6 files
   - <strong> app.module.ts </strong> : Defines the root module, named AppModule, that tells Angular how to assemble the application. Initially declares only the AppComponent. As you add more components to the app, they must be declared here.
   - <strong> app.component.ts </strong> : ?
   - <strong> app.component.spec.ts </strong> : Defines a unit test for the root AppComponent.
   - <strong> app.component.html </strong> : Defines the HTML template associated with the root AppComponent.
   - <strong> app.component.css </strong> : Defines the base CSS stylesheet for the root AppComponent.
   - <strong> app-routing.module.ts </strong> : The composant routing file