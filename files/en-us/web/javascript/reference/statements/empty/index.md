---
title: empty
slug: Web/JavaScript/Reference/Statements/Empty
tags:
- JavaScript
- Language feature
- Statement
browser-compat: javascript.statements.empty
---
{{jsSidebar("Statements")}}

An **empty statement** is used to provide no statement, although the JavaScript
syntax would expect one.

{{EmbedInteractiveExample("pages/js/statement-empty.html")}}

## Syntax

```js
;
```

## Description

The empty statement is a semicolon (`;`) indicating that no statement will be
executed, even if JavaScript syntax requires one.

The opposite behavior, where you want multiple statements, but JavaScript only
allows a single one, is possible using
a[ block statement](/en-US/docs/Web/JavaScript/Reference/Statements/block),
which combines several statements into a single one.

## Examples

### Empty loop body

The empty statement is sometimes used with loop statements. See the following
example with an empty loop body:

```js
let arr = [1, 2, 3];

// Assign all array values to 0
for (let i = 0; i < arr.length; arr[i++] = 0) /* empty statement */ ;

console.log(arr);
// [0, 0, 0]
```

### Unintentional usage

It is a good idea to comment *intentional* use of the empty statement, as it is
not really obvious to distinguish from a normal semicolon.

In the following example, the usage is probably not intentional:

```js example-bad
if (condition);       // Caution, this "if" does nothing!
   killTheUniverse()  // So this always gets executed!!!
```

In the next example, an
{{jsxref("Statements/if...else", "if...else")}} statement
without curly braces (`{}`) is used.

If `three` is `true`, nothing will happen, `four` does not matter, and also the
`launchRocket()` function in the `else` case will not be executed.

```js example-bad
if (one)
  doOne();
else if (two)
  doTwo();
else if (three)
  ; // nothing here
else if (four)
  doFour();
else
  launchRocket();
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

*   {{jsxref("Statements/block", "Block statement")}}