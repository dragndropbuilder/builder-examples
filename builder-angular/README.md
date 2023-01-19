## Quickstart

1. Install 
```
npm i @videostation/reportbuilder
```
2. Add new `schemas: []` property with `CUSTOM_ELEMENTS_SCHEMA` value to `@NgModule` decorator of your `AppModule`

Example of module implementation...
```typescript
import { CUSTOM_ELEMENTS_SCHEMA, NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  bootstrap: [AppComponent],
  schemas: [CUSTOM_ELEMENTS_SCHEMA]
})
export class AppModule { }
```
Example of component implementation...
```typescript
import { Component } from '@angular/core';
import '@videostation/reportbuilder/elements';

@Component({
  selector: 'app-root',
  template: '<vs-form-builder style="width: 100%;"></vs-form-builder>',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  title = 'VideoStation :: Builder';
}
```

## Development

To get started:

```bash
$ npm install
```

To see the demo app, run:

```bash
$ npm start
```