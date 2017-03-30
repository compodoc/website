## General information

Compodoc use Typescript AST parser and it's internal APIs, so the comments have to be JSDoc comments :

```js
/**
 * Supported comment
 */
```

These ones are not supported :

```js
/*
 * unsupported comment
 */

/*
  unsupported comment
 */

// unsupported comment
```

## JSDoc tags

Currently Compodoc only support these JSDoc tags :

- ```@returns```

- ```@param <param name>```

```js
/**
 * @param {string} target  The target to process see {@link Todo}
 *
 * @example
 * This is a good example
 * processTarget('yo')
 *
 * @returns      The processed target number
 */
function processTarget(target:string):number;
```

- ```@link``` : you can use these three syntax like JSDoc:

```js
//for an internal reference

{@link Todo}
[Todo]{@link Todo}
{@link Todo|TodoClass}

//for an external link

[Google]{@link http://www.google.com}
{@link http://www.apple.com|Apple}
{@link https://github.com GitHub}
```

- ```@example``` : for giving an example on directives, components and pipes decorators, use @example or markdown :

```js
/**
 * Shows all events on a given day. Example usage:
 *
 * `` `
 * &lt;mwl-calendar-day-view
 *  [viewDate]="viewDate"
 *  [events]="events"&gt;
 * &lt;/mwl-calendar-day-view&gt;
 * `` `
 */

 /**
  * Shows all events on a given day. Example usage:
  *
  * @example
  * <mwl-calendar-day-view
  *  [viewDate]="viewDate"
  *  [events]="events">;
  * </mwl-calendar-day-view>
  */
```
