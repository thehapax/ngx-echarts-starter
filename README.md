Numerous changes must be made to fork in order to get sample working in Angular 9.07. 
-  See reference guide: https://www.freakyjolly.com/angular-e-charts-using-ngx-echarts-tutorial/
-  "enableIvy": false, in tsconfig.json
-  app.module.ts : imports NgxEchartsModule only, do not include  forRoot
- in package.json, dependencies: 

```
    "rxjs": "~6.5.4",
    "tslib": "^1.10.0",
```

- if using "@angular/core": "~9.1.7", need to downgrade in package.json or charts will be 'null'

```
dependencies:
    "echarts": "^4.2.1",
    "ngx-echarts": "^4.2.2",
```


==========

# Ngx-Echarts Starter Project

A starter project for [ngx-echarts](https://github.com/xieziyu/ngx-echarts)

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.8.

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
