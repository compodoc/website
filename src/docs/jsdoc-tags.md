# JSDoc tags

Currently Compodoc only support these JSDoc tags (due to [TypeScript compiler limitations](https://github.com/Microsoft/TypeScript/wiki/JSDoc-support-in-JavaScript)) :

-   `@returns {Type} Description`

```js
/**
 * @param {string} target  The target to process
 * @returns The processed target number
 */
function processTarget(target:string):number;
```

-   `@ignore`, `@internal`

These tags indicate that a symbol in your code should never appear in the documentation.

`@ignore` works inside a class, component or injectable, but also for the entire component.

```js
/**
 * @ignore
 */
@Component({
    selector: 'app-root',
    templateUrl: './app.component.html',
    styleUrls: ['./app.component.css'],
})
export class AppComponent {}
```

```js
/**
 * Footer component
 */
@Component({
    selector: 'the-footer',
    templateUrl: './footer.component.html',
    styleUrls: ['./footer.component.css'],
})
export class FooterComponent {
    /**
     * @ignore
     */
    ignoredProperty: string;

    /**
     * @ignore
     */
    @Input() ignoredInput: string;

    /**
     * @ignore
     */
    @Output() ignoredOutput;

    /**
     * @ignore
     */
    ignoredFunction() {}
}
```

-   `@param {Type} Name Description`

```js
/**
 * @example
 * This is a good example
 * processTarget('yo')
 *
 * @param {string} target  The target to process see {@link Todo}
 * @returns The processed target number
 */
function processTarget(target:string):number;
```

-   `@link` : you can use these three syntax like JSDoc:

```js
//for an internal reference

{@link Todo}
[Todo]{@link Todo}
{@link Todo|TodoClass}

Anchors are supported : [Todo]{@link Todo#myproperty}

//for an external link

[Google]{@link http://www.google.com}
{@link http://www.apple.com|Apple}
{@link https://github.com GitHub}
```

-   `@example` : for giving an example on directives, components and pipes decorators, use @example or markdown :

**INDENTATION WARNING** : TypeScript has an internal margin for new lines, if you want to keep a level of indentation, put a minimum of 13 space characters like in the next example.

```js
/**
 * Shows all events on a given day. Example usage:
 *
 * `` `
 * &lt;mwl-calendar-day-view
 *             [viewDate]="viewDate"
 *             [events]="events"&gt;
 * &lt;/mwl-calendar-day-view&gt;
 * `` `
 */

/**
 * Shows all events on a given day. Example usage:
 *
 * @example
 * <mwl-calendar-day-view
 *             [viewDate]="viewDate"
 *             [events]="events">
 * </mwl-calendar-day-view>
 */
```
