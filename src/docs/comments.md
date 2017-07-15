# General information

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

New lines are created inside a comment with a blank line between two lines.

```js
/**
 * First line
 *
 * Second line
 */
```

The example below will produce only one line in the outputed documentation.

```js
/**
 * First line
 * Second line
 */
```

# JSDoc tags

Currently Compodoc only support these JSDoc tags (due to [TypeScript compiler limitations](https://github.com/Microsoft/TypeScript/wiki/JSDoc-support-in-JavaScript)) :

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

__INDENTATION WARNING__ : TypeScript has an internal margin for new lines, if you want to keep a level of indentation, put a minimum of 13 space characters like in the next example.

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

# Components and directives example tags

Live demo examples tab can be added to components and directives documentation pages by the help of <example-url> tag.

```js
 /**
  * Example of usage:
  * <example-url>http://localhost/demo/mysample.component.html</example-url>
  * <example-url>/demo/mysample.component.html</example-url>
  */
```
