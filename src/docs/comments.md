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