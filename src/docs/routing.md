# General information

Follow the [style guide](https://angular.io/docs/ts/latest/guide/router.html#!#routing-module), provide a const of type __'Routes'__ with an __unique__ name :

```js
const APP_ROUTES: Routes = [
    { path: 'about', component: AboutComponent },
    { path: '', component: HomeComponent}
];

...

RouterModule.forRoot(APP_ROUTES)
```

# Limitations

spread variables in routes definition are not yet supported

```js
const APP_ROUTES: Routes = [...ROUTES];
```
