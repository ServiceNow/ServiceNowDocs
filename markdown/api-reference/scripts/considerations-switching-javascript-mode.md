---
title: Considerations for switching JavaScript modes
description: Switching the JavaScript mode for an application or script might change the behavior of existing scripts. Review some examples of behavior changes before switching JavaScript modes or to troubleshoot any issues that you experience after switching.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [JavaScript modes, JavaScript engine, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Considerations for switching JavaScript modes

Switching the JavaScript mode for an application or script might change the behavior of existing scripts. Review some examples of behavior changes before switching JavaScript modes or to troubleshoot any issues that you experience after switching.

For more information about each JavaScript mode, see [JavaScript modes](c_JS_modes.md) and [JavaScript engine feature support](../reference/javascript-engine-feature-support.md).

This table highlights how JavaScript behavior has evolved from the lenient and error-prone pre-ES5 environment, to the stricter and more predictable ES5, and lastly the more feature-rich environment of ES12 \(ECMAScript 2021\).

<table id="table_r4b_j4r_fcc"><thead><tr><th>

Feature

</th><th>

Compatibility Mode

</th><th>

ES5 Standards Mode

</th><th>

ECMAScript 2021 \(ES12\)

</th></tr></thead><tbody><tr><td>

Arguments object

</td><td>

The `arguments` object exists, but there's no `strict mode`, so modifications reflect on `arguments`. Prints: ```javascript
*** Script: [object Arguments]
*** Script: [object Arguments]
*** Script: [object Arguments]
*** Script: 123
```

</td><td>

In strict mode, the arguments object doesn’t reflect parameter modifications and throws an error. Prints: ```javascript
sn_es5: 123
sn_es5: undefined
sn_es5: [object Arguments]
sn_es5: 123
```

</td><td>

The same as ES5.

</td></tr><tr><td>

Boolean overrides

</td><td>

Primitive Booleans \(`true`, `false`\) can be overridden, causing unexpected behavior.

</td><td>

Primitive Booleans are more protected, though still can be overridden when assigned to variables.

</td><td>

The same as ES5, but strict mode helps prevent some assignments. The conditional expression should be written in this form: ```javascript
(cond_expr instanceof Boolean ? cond_expr.valueOf() : cond_expr).
```

</td></tr><tr><td>

Exception for syntax errors

</td><td>

Syntax errors throw exceptions at runtime. Error handling is inconsistent. Example: ```javascript
Javascript compiler exception: unterminated string literal (null.null.script; line 1) in:
var b = '
```

</td><td>

More consistent syntax error handling, especially in strict mode. Example: ```javascript
Evaluator: com.glide.script.RhinoEcmaError: unterminated string literal
   script : Line(1) column(9)
==>   1: var b = '
```

</td><td>

The same as ES5, but with more robust handling and clearer error messages in updated engines. Example: ```javascript
SyntaxError: Unterminated string constant at line 1

==>   1: var b = '
```

</td></tr><tr><td>

Increment and decrement

</td><td>

Allowed on variables but could behave unexpectedly with complex expressions. Prints: ```javascript
*** Script: c: 1
*** Script: gr.related_incidents: 1
*** Script: 2
*** Script: 3
```

</td><td>

Improved clarity, but still allowed on variables \(`var`, `let`, `const`\). Prints: ```javascript
sn_es5: c: 0
sn_es5: gr.related_incidents: 1
sn_es5: 1
sn_es5: 2
```

</td><td>

The same as ES5, with stricter rules in some contexts \(for example, `const`\).

</td></tr><tr><td>

Line continuations

</td><td>

Allowed with a backslash \(`\`\) but discouraged due to readability issues. In this example, all three functions are called. ```javascript
var expr = doFoo();  // do foo
           doBar();  // do bar 
           finish();   // all done
 eval(expr);

```

</td><td>

Same as Compatibility mode; no change in handling line continuations. In the previous example, ES5 only calls the first function and treats everything after the first comment including the newline as comment until the expression end.

</td><td>

The same as ES5, but template literals provide a more readable alternative.

</td></tr><tr><td>

Missing semicolons

</td><td>

Automatic semicolon insertion \(ASI\) often led to unexpected behavior.

</td><td>

Throws a syntax error when a semicolon is missing.

</td><td>

The same as ES5. Updated practices encourage explicit semicolons.

</td></tr><tr><td>

Non-existent functions

</td><td>

Calling a non-existent function throws a `ReferenceError`.

</td><td>

Throws a `TypeError` if a non-function is called.

</td><td>

Throws an EcmaError when a non-existent function is called or a property is referenced.

</td></tr><tr><td>

Non-existent properties

</td><td>

Accessing a non-existent property returns `undefined`; no error thrown.

</td><td>

Same as pre-ES5.

</td><td>

The same as Compatibility mode and ES5 Standards mode.

</td></tr><tr><td>

Numeric literals

</td><td>

Basic decimal and hexadecimal literals.

</td><td>

Introduced stricter parsing rules and better handling of numeric literals.

</td><td>

Added binary \(`0b`\), octal \(`0o`\), and BigInt literals \(`123n`\).

</td></tr><tr><td>

Reserved keyword as property

</td><td>

Using reserved keywords isn't possible.

</td><td>

Reserved keywords can be used as property names without error, for example, `obj.for`. Prints the object when returned.

</td><td>

The same as ES5.

</td></tr><tr><td>

Treat let and yield as keywords

</td><td>

`let` and `yield` aren’t keywords and can be used as identifiers only.

</td><td>

`let` is introduced as a keyword. `yield` is reserved in strict mode.

</td><td>

Both are keywords. Using them as identifiers throws syntax errors.

</td></tr></tbody>
</table>**Parent Topic:**[JavaScript modes](c_JS_modes.md)

