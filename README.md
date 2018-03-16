# Angular5firebasecrud folder stucture
https://drive.google.com/open?id=1Vk2IdOW3WfD4ft7_1WRQn_hqUNvKitKV

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).



## start (Angular% firebase Crud)

## create project
ng new angular5firebasecrud

## Configure firebase project with your gmail account.
https://console.firebase.google.com

click on Add project 
enter project name 
continue
add firebase to your web app
copy apikey etc. (all congiguration) paste in environment.ts file


## firebase package installing
npm install firebase@4.6.1 angularfire2@5.0.0-rc.3  --save

## import following package in app.module.ts
import { AngularFireModule } from 'angularfire2';
import { AngularFireDatabaseModule } from 'angularfire2/database';
import { environment } from '../environments/environment';

 imports: [
    BrowserModule,
    AngularFireModule.initializeApp(environment.firebaseConfig),
    AngularFireDatabaseModule  
  ],

  ## generate component
  ng g c employees

  ## child component
  ng g c employee
  ng g c employee-list

  ## create shared folder under employees
  ng g s employee
  ng g class employee --type=model

  type code in employee.model.ts


## import following package in employee.service.ts
import { AngularFireDatabase, AngularFireList } from 'angularfire2/database';
import {Employee } from './employee.model';
