#### Built from 
`https://www.jqwidgets.com/angular-components-documentation/documentation/angular-cli/angular-cli.htm`

## Build Angular basic:
```
ng new myapp
cd newapp 
ng serve
```
## Add JQWidgets:
```
npm install jqwidgets-scripts --save
ng serve
```
#### app.module.ts
```
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { AppComponent } from './app.component';
import { jqxBarGaugeComponent } from 'jqwidgets-scripts/jqwidgets-ts/angular_jqxbargauge';
@NgModule({
  declarations: [
    AppComponent, jqxBarGaugeComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
#### app.component.ts
```
import { Component } from '@angular/core';
 
@Component({
    selector: 'app-root',
    templateUrl: './app.component.html',
    styleUrls: ['./app.component.css']
})
 
export class AppComponent {
    values: number[] = [102, 115, 130, 137];
}
```
#### app.component.html
```
<jqxBarGauge 
    [width]="600" [height]="600" [max]="150" 
    [colorScheme]="'scheme02'" [values]="values">
</jqxBarGauge>
```
#### add to tsconfig.json
```
  	"include": [
	  "src/**/*"
	],
	"files": [
	  "node_modules/jqwidgets-scripts/jqwidgets-ts/angular_jqxbargauge.ts"
	]
```

`ng serve`

# JqwidgetsAngularCliApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.0.2.

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
