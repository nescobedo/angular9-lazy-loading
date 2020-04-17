# Angular 9 LazyLoading Modules the Ivy way

I've been creating a lot of angular repos lately and was setting up lazy loading for a new app.  Should have been less then an hour to setup the modules and components I wanted but I kept getting errors when setting up child routes.  

In the end I forgot to consider that I was using the latest and greatest (Ivy) and that loadChildren process has changed.   

**Angular 8:**  
  loadChildren: '../app/orders/orders.module#OrdersModule',

**Angular 9:**  
 loadChildren: () => import('./orders/orders.module').then(m => m.OrdersModule)

  
    
    

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
