Follow the style guide, provide a const of type 'Routes' and with an unique name :

```js
const APP_ROUTES: Routes = [
    { path: 'about', component: AboutComponent },
    { path: '', component: HomeComponent}
];

...

RouterModule.forRoot(APP_ROUTES)
```
