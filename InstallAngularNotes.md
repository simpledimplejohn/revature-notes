To install Angular 

Install Typescript
`npm install -g typescript`



Install the command line interface
`npm install -g @angular/cli`
To Create a Project
`ng new complete-api-ui --skip-git`
  * yes to routing
  * select css for styles

// if you did not get routing you can add it 


Create a app component: ??
  `mkdir components` in src/app
  `cd components`
  `ng g c app`

Install bootstrap:
`ng add @ng-bootstrap/ng-bootstrap`

Run Live Server
  `ng serve -o`
  quit control - c

Module is a container for an app

When downloading without NodeModules or refreshing run
`npm install` or `npm i`

Build is 
`ng build`

Make models in app
  * user.ts made manually

CLI
`ng generate component` these are abreviated
* make a service `ng g s name` //creates a serivce
* make a componenent `ng g c name`

ADDING BOOTSTRAP
* Run this from the root directory (or whereever....)
* `npm install bootstrap --save`
* Put this in global styles.css
* `@import "~bootstrap/dist/css/bootstrap.css"`
* Also there is Ng bootstrap
* `ng add @ng-bootstrap/ng-bootstrap`
* Don't forget to import it too

ROUTTING A PAGE
* in app-routing.modules.st declare the path in the routs array
  `const routes: Routes = [ {path: '', component: MainComponent} ]`
* in the app.component.html all routs run through
  `<router-outlet></router-outlet>`
* to link to a route use the:
  <class="someclass" routerLink="/">

Making A Model 
* nothing special, make a model folder, moodel file.ts

Make A Service
* `ng g s user` for a user service