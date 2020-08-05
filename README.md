## Notes from 3 AUG 2020 

It appears that the starter does not work immediately out of the box. 
From reviewing the open issues on ngx-echarts it appears many unresolved issues. 

Here are my notes to get the starter working:

Numerous changes must be made to fork in order to get sample working in Angular 9.07. 

-  No angular 10 version available yet. 
-  "enableIvy": false, in tsconfig.json (https://github.com/xieziyu/ngx-echarts/issues/217#issue-542377145)
-  app.module.ts : imports NgxEchartsModule only, do not include forRoot (https://github.com/xieziyu/ngx-echarts/issues/241#issuecomment-651244001)
- in package.json, add dependencies: 

```
    "rxjs": "~6.5.4",
    "tslib": "^1.10.0",
```

- if using "@angular/core": "~9.1.7", for now, ngx-echarts: 5.0.0 is broken, need to downgrade in package.json or charts will be 'null', hopefully the developers will fix it soon. (https://github.com/xieziyu/ngx-echarts/issues/241#issuecomment-648116169)


```
dependencies:
    "echarts": "^4.2.1",
    "ngx-echarts": "^4.2.2",
```

- This repository deployed with production build on https://ngx-echarts-starter-a0adf4.netlify.app/

On `ng build --prod` we have a few warnings: 

```
WARNING in $Homedir/ngx-echarts-starter/node_modules/echarts/index.js depends on 'zrender/lib/vml/vml'. CommonJS or AMD dependencies can cause optimization bailouts.
For more info see: https://angular.io/guide/build#configuring-commonjs-dependencies

WARNING in $Homedir/ngx-echarts-starter/node_modules/echarts/index.js depends on 'zrender/lib/svg/svg'. CommonJS or AMD dependencies can cause optimization bailouts.
For more info see: https://angular.io/guide/build#configuring-commonjs-dependencies
```


Original Readme is below
=========================

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


-  Also see reference guide: https://www.freakyjolly.com/angular-e-charts-using-ngx-echarts-tutorial/
