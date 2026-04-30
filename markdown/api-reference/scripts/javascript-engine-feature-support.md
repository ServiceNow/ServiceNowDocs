---
title: JavaScript engine feature support
description: Compare ECMAScript features between the ECMAScript 2021 \(ES12\) and ES5 Standards JavaScript modes in Zurich. Both modes support a subset of ECMAScript features.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 30
breadcrumb: [JavaScript engine, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# JavaScript engine feature support

Compare ECMAScript features between the ECMAScript 2021 \(ES12\) and ES5 Standards JavaScript modes in Zurich. Both modes support a subset of ECMAScript features.

For more information about these features, see the ECMAScript language specifications \(ECMA-262\) on the [Ecma International](https://www.ecma-international.org/) website.

## Support definitions

-   **Supported**

    The feature has been tested and validated.

-   **Not Supported**

    The feature has not been validated in the current release.

-   **Disallowed**

    The feature does not align with the ServiceNow AI Platform programming model or poses a security or performance risk. Disallowed features result in an error.


## ECMAScript 2022 \(ES13\) features

**Important:** Prior to deploying code to production, you should test scripts using supported ECMAScript 2022 \(ES13\) features thoroughly due to the newly added and partial support of features across this ECMAScript version.

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|public instance class fields|Supported|Not Supported|
|private instance class fields basic support|Not Supported|Not Supported|
|private instance class fields initializers|Not Supported|Not Supported|
|optional private instance class fields access|Not Supported|Not Supported|
|optional deep private instance class fields access|Not Supported|Not Supported|
|computed instance class fields|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|public static class fields|Supported|Not Supported|
|static class fields use \[\[Define\]\]|Supported|Not Supported|
|private static class fields|Supported|Not Supported|
|computed static class fields|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|private instance methods|Not Supported|Not Supported|
|private static methods|Supported|Not Supported|
|private accessor properties|Not Supported|Not Supported|
|private static accessor properties|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.prototype.at\(\)|Supported|Not Supported|
|String.prototype.at\(\)|Supported|Not Supported|
|%TypedArray%.prototype.at\(\)|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Basic functionality|Supported|Not Supported|
|ToObject called before ToPropertyKey|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Error has cause|Supported|Not Supported|
|Error.prototype lacks cause|Supported|Not Supported|
|EvalError has cause|Supported|Not Supported|
|EvalError.prototype lacks cause|Supported|Not Supported|
|RangeError has cause|Supported|Not Supported|
|RangeError.prototype lacks cause|Supported|Not Supported|
|ReferenceError has cause|Supported|Not Supported|
|ReferenceError.prototype lacks cause|Supported|Not Supported|
|SyntaxError has cause|Supported|Not Supported|
|SyntaxError.prototype lacks cause|Supported|Not Supported|
|TypeError has cause|Supported|Not Supported|
|TypeError.prototype lacks cause|Supported|Not Supported|
|URIError has cause|Supported|Not Supported|
|URIError.prototype lacks cause|Supported|Not Supported|
|AggregateError has cause|Supported|Not Supported|
|AggregateError.prototype lacks cause|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|constructor supports it|Not Supported|Not Supported|
|shows up in flags|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Ergonomic brand checks for private fields|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Class static initialization blocks|Supported|Not Supported|

## ECMAScript 2021 \(ES12\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|fulfillment|Supported|Disallowed|
|AggregateError|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|WeakRef minimal support|Disallowed|Disallowed|
|FinalizationRegistry minimal support|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|\|\|= basic support|Supported|Not Supported|
|\|\|= short-circuiting behavior|Supported|Not Supported|
|\|\|= setter not unnecessarily invoked|Supported|Not Supported|
|&amp;&amp;= basic support|Supported|Not Supported|
|&amp;&amp;= short-circuiting behavior|Supported|Not Supported|
|&amp;&amp;= setter not unnecessarily invoked|Supported|Not Supported|
|??= basic support|Supported|Not Supported|
|??= short-circuiting behavior|Supported|Not Supported|
|??= setter not unnecessarily invoked|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|numeric separators|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|String.prototype.replaceAll|Supported|Supported|

## ECMAScript 2020 \(ES11\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|throws on non-global regex|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|constructor|Supported|Not Supported|
|BigInt.asUintN|Supported|Not Supported|
|BigInt.asIntN|Supported|Not Supported|
|BigInt64Array|Not Supported|Not Supported|
|BigUint64Array|Not Supported|Not Supported|
|DataView.prototype.getBigInt64|Not Supported|Not Supported|
|DataView.prototype.getBigUint64|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|"globalThis" global property is global object|Supported|Disallowed|
|"globalThis" global property has correct property descriptor|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|optional property access|Supported|Not Supported|
|optional bracket access|Supported|Not Supported|
|optional method call|Supported|Not Supported|
|optional function call|Supported|Not Supported|
|spread parameters after optional chaining|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Promise.allSettled|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|nullish coalescing operator \(??\)|Supported|Not Supported|

## ECMAScript 2019 \(ES10\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic|Supported|Not Supported|
|empty description|Supported|Not Supported|
|undefined description|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|String.prototype.trimLeft|Supported|Supported|
|String.prototype.trimRight|Supported|Supported|
|String.prototype.trimStart|Supported|Not Supported|
|String.prototype.trimEnd|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.prototype.flat|Supported|Not Supported|
|Array.prototype.flatMap|Supported|Not Supported|
|flat and flatMap in Array.prototype\[@@unscopables\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.fromEntries|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic|Supported|Disallowed|
|await|Disallowed|Disallowed|
|yield|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|functions created with the Function constructor|Disallowed|Disallowed|
|arrows|Disallowed|Disallowed|
|\[native code\]|Disallowed|Disallowed|
|class expression with implicit constructor|Disallowed|Disallowed|
|class expression with explicit constructor|Disallowed|Disallowed|
|unicode escape sequences in identifiers|Disallowed|Disallowed|
|methods and computed property names|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Line separator can appear in string literals|Disallowed|Disallowed|
|Paragraph separator can appear in string literals|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Well-formed JSON.stringify|Disallowed|Disallowed|

## ECMAScript 2018 \(ES9\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|object rest properties|Supported|Not Supported|
|object spread properties|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic support|Supported|Disallowed|
|don't change resolution value|Supported|Disallowed|
|change rejection value|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|async generators|Disallowed|Disallowed|
|for-await-of loops|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|s \(dotAll\) flag for regular expressions|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|RegExp named capture groups|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|RegExp Lookbehind Assertions|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|RegExp Unicode Property Escapes|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|template literal revision|Disallowed|Disallowed|

## ECMAScript 2017 \(ES8\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.values|Supported|Not Supported|
|Object.entries|Supported|Not Supported|
|Object.getOwnPropertyDescriptors|Supported|Not Supported|
|Object.getOwnPropertyDescriptors doesn't provide undefined descriptors|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|String.prototype.padStart|Supported|Not Supported|
|String.prototype.padEnd|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|in parameter lists|Supported|Not Supported|
|in argument lists|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|return|Supported|Disallowed|
|throw|Supported|Disallowed|
|no line break between async and function|Supported|Disallowed|
|no "prototype" property|Disallowed|Disallowed|
|await|Supported|Disallowed|
|await, rejection|Supported|Disallowed|
|must await a value|Disallowed|Disallowed|
|can await non-Promise values|Supported|Disallowed|
|cannot await in parameters|Disallowed|Disallowed|
|async methods, object literals|Supported|Disallowed|
|async methods, classes|Disallowed|Disallowed|
|async arrow functions in methods, classes|Supported|Disallowed|
|async arrow functions|Supported|Disallowed|
|correct prototype chain|Disallowed|Disallowed|
|async function prototype, Symbol.toStringTag|Disallowed|Disallowed|
|async function constructor|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|SharedArrayBuffer|Disallowed|Disallowed|
|SharedArrayBuffer\[Symbol.species\]|Disallowed|Disallowed|
|SharedArrayBuffer.prototype.byteLength|Disallowed|Disallowed|
|SharedArrayBuffer.prototype.slice|Disallowed|Disallowed|
|SharedArrayBuffer.prototype\[Symbol.toStringTag\]|Disallowed|Disallowed|
|Atomics.add|Disallowed|Disallowed|
|Atomics.and|Disallowed|Disallowed|
|Atomics.compareExchange|Disallowed|Disallowed|
|Atomics.exchange|Disallowed|Disallowed|
|Atomics.wait|Disallowed|Disallowed|
|Atomics.wake|Disallowed|Disallowed|
|Atomics.isLockFree|Disallowed|Disallowed|
|Atomics.load|Disallowed|Disallowed|
|Atomics.or|Disallowed|Disallowed|
|Atomics.store|Disallowed|Disallowed|
|Atomics.sub|Disallowed|Disallowed|
|Atomics.xor|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|\_\_defineGetter\_\_|Supported|Disallowed|
|\_\_defineGetter\_\_, symbols|Supported|Disallowed|
|\_\_defineGetter\_\_, ToObject\(this\)|Disallowed|Disallowed|
|\_\_defineSetter\_\_|Supported|Disallowed|
|\_\_defineSetter\_\_, symbols|Supported|Disallowed|
|\_\_defineSetter\_\_, ToObject\(this\)|Disallowed|Disallowed|
|\_\_lookupGetter\_\_|Supported|Disallowed|
|\_\_lookupGetter\_\_, prototype chain|Supported|Disallowed|
|\_\_lookupGetter\_\_, symbols|Supported|Disallowed|
|\_\_lookupGetter\_\_, ToObject\(this\)|Disallowed|Disallowed|
|\_\_lookupGetter\_\_, data properties can shadow accessors|Disallowed|Disallowed|
|\_\_lookupSetter\_\_|Supported|Disallowed|
|\_\_lookupSetter\_\_, prototype chain|Supported|Disallowed|
|\_\_lookupSetter\_\_, symbols|Supported|Disallowed|
|\_\_lookupSetter\_\_, ToObject\(this\)|Disallowed|Disallowed|
|\_\_lookupSetter\_\_, data properties can shadow accessors|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|\_\_defineGetter\_\_|Supported|Disallowed|
|\_\_defineSetter\_\_|Supported|Disallowed|
|\_\_lookupGetter\_\_|Supported|Disallowed|
|\_\_lookupSetter\_\_|Supported|Disallowed|

## ECMAScript 2016 \(ES7\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic support|Supported|Not Supported|
|assignment|Supported|Not Supported|
|early syntax error for unary negation without parentheses|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.prototype.includes|Supported|Not Supported|
|Array.prototype.includes is generic|Not Supported|Not Supported|
|%TypedArray%.prototype.includes|Supported|Disallowed|

## ECMAScript 2015 \(ES6\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|direct recursion|Disallowed|Disallowed|
|mutual recursion|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|explicit undefined defers to the default|Supported|Not Supported|
|defaults can refer to previous parameters|Supported|Not Supported|
|arguments object interaction|Supported|Not Supported|
|temporal dead zone|Disallowed|Disallowed|
|separate scope|Supported|Not Supported|
|new Function\(\) support|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|function 'length' property|Supported|Not Supported|
|arguments object interaction|Not Supported|Not Supported|
|can't be used in setters|Disallowed|Disallowed|
|new Function\(\) support|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|with arrays, in function calls|Supported|Not Supported|
|with arrays, in array literals|Supported|Not Supported|
|with sparse arrays, in function calls|Supported|Not Supported|
|with sparse arrays, in array literals|Supported|Not Supported|
|with strings, in function calls|Supported|Not Supported|
|with strings, in array literals|Supported|Not Supported|
|with astral plane strings, in function calls|Supported|Not Supported|
|with astral plane strings, in array literals|Supported|Not Supported|
|with generator instances, in calls|Disallowed|Disallowed|
|with generator instances, in arrays|Disallowed|Disallowed|
|with generic iterables, in calls|Supported|Not Supported|
|with generic iterables, in arrays|Supported|Not Supported|
|with instances of iterables, in calls|Supported|Not Supported|
|with instances of iterables, in arrays|Supported|Not Supported|
|spreading non-iterables is a runtime error|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|computed properties|Supported|Not Supported|
|shorthand properties|Supported|Not Supported|
|shorthand methods|Supported|Not Supported|
|string-keyed shorthand methods|Supported|Not Supported|
|computed shorthand methods|Supported|Not Supported|
|computed accessors|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|with arrays|Supported|Not Supported|
|with sparse arrays|Supported|Not Supported|
|with strings|Supported|Not Supported|
|with astral plane strings|Supported|Not Supported|
|with generator instances|Disallowed|Disallowed|
|with generic iterables|Supported|Not Supported|
|with instances of generic iterables|Supported|Not Supported|
|iterator closing, break|Supported|Not Supported|
|iterator closing, throw|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|octal literals|Supported|Not Supported|
|binary literals|Supported|Not Supported|
|octal supported by Number\(\)|Not Supported|Not Supported|
|binary supported by Number\(\)|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|toString conversion|Supported|Not Supported|
|tagged template literals|Supported|Not Supported|
|passed array is frozen|Supported|Not Supported|
|line break normalization|Disallowed|Disallowed|
|TemplateStrings call site caching|Supported|Not Supported|
|TemplateStrings permanent caching|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|"y" flag|Supported|Not Supported|
|"y" flag, lastIndex|Supported|Not Supported|
|"u" flag|Supported|Not Supported|
|"u" flag, non-BMP Unicode characters|Supported|Not Supported|
|"u" flag, Unicode code point escapes|Supported|Not Supported|
|"u" flag, case folding|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|with arrays|Supported|Not Supported|
|with sparse arrays|Supported|Not Supported|
|with strings|Supported|Not Supported|
|with astral plane strings|Supported|Not Supported|
|with generator instances|Disallowed|Disallowed|
|with generic iterables|Supported|Not Supported|
|with instances of generic iterables|Supported|Not Supported|
|iterator closing|Supported|Not Supported|
|trailing commas in iterable patterns|Supported|Not Supported|
|with objects|Supported|Not Supported|
|object destructuring with primitives|Supported|Not Supported|
|trailing commas in object patterns|Supported|Not Supported|
|throws on null and undefined|Supported|Not Supported|
|computed properties|Supported|Not Supported|
|multiples in a single var statement|Supported|Not Supported|
|nested|Supported|Not Supported|
|in for-in loop heads|Supported|Not Supported|
|in for-of loop heads|Supported|Not Supported|
|in catch heads|Supported|Not Supported|
|rest|Supported|Not Supported|
|defaults|Supported|Not Supported|
|defaults, let temporal dead zone|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|with arrays|Supported|Not Supported|
|with sparse arrays|Supported|Not Supported|
|with strings|Supported|Not Supported|
|with astral plane strings|Supported|Not Supported|
|with generator instances|Disallowed|Disallowed|
|with generic iterables|Supported|Not Supported|
|with instances of generic iterables|Supported|Not Supported|
|iterator closing|Supported|Not Supported|
|iterable destructuring expression|Supported|Not Supported|
|chained iterable destructuring|Supported|Not Supported|
|trailing commas in iterable patterns|Supported|Not Supported|
|with objects|Supported|Not Supported|
|object destructuring with primitives|Supported|Not Supported|
|trailing commas in object patterns|Supported|Not Supported|
|object destructuring expression|Supported|Not Supported|
|parenthesized left-hand-side is a syntax error|Disallowed|Disallowed|
|chained object destructuring|Supported|Not Supported|
|throws on null and undefined|Supported|Not Supported|
|computed properties|Supported|Not Supported|
|nested|Supported|Not Supported|
|rest|Supported|Not Supported|
|nested rest|Supported|Not Supported|
|empty patterns|Supported|Not Supported|
|defaults|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|with arrays|Supported|Not Supported|
|with sparse arrays|Supported|Not Supported|
|with strings|Supported|Not Supported|
|with astral plane strings|Supported|Not Supported|
|with generator instances|Disallowed|Disallowed|
|with generic iterables|Supported|Not Supported|
|with instances of generic iterables|Supported|Not Supported|
|iterator closing|Supported|Not Supported|
|trailing commas in iterable patterns|Supported|Not Supported|
|with objects|Supported|Not Supported|
|object destructuring with primitives|Supported|Not Supported|
|trailing commas in object patterns|Supported|Not Supported|
|throws on null and undefined|Supported|Not Supported|
|computed properties|Supported|Not Supported|
|nested|Supported|Not Supported|
|'arguments' interaction|Supported|Not Supported|
|new Function\(\) support|Disallowed|Disallowed|
|in parameters, function 'length' property|Supported|Not Supported|
|rest|Supported|Not Supported|
|empty patterns|Supported|Not Supported|
|defaults|Supported|Not Supported|
|defaults, separate scope|Supported|Not Supported|
|defaults, new Function\(\) support|Disallowed|Disallowed|
|aliased defaults, arrow function|Supported|Not Supported|
|shorthand defaults, arrow function|Supported|Not Supported|
|duplicate identifier|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|in strings|Supported|Not Supported|
|in identifiers|Not Supported|Not Supported|
|in property key definitions|Not Supported|Not Supported|
|in property key accesses|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|in constructors|Not Supported|Not Supported|
|assignment is an early error|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic support|Supported|Supported|
|is block-scoped|Supported|Not Supported|
|scope shadow resolution|Supported|Not Supported|
|cannot be in statements|Disallowed|Disallowed|
|redefining a const is an error|Disallowed|Disallowed|
|for loop statement scope|Supported|Not Supported|
|for-in loop iteration scope|Supported|Not Supported|
|for-of loop iteration scope|Supported|Not Supported|
|temporal dead zone|Not Supported|Not Supported|
|basic support \(strict mode\)|Supported|Supported|
|is block-scoped \(strict mode\)|Supported|Not Supported|
|scope shadow resolution \(strict mode\)|Supported|Not Supported|
|cannot be in statements \(strict mode\)|Disallowed|Disallowed|
|redefining a const \(strict mode\)|Disallowed|Disallowed|
|for loop statement scope \(strict mode\)|Supported|Not Supported|
|for-in loop iteration scope \(strict mode\)|Supported|Not Supported|
|for-of loop iteration scope \(strict mode\)|Supported|Not Supported|
|temporal dead zone \(strict mode\)|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic support|Supported|Not Supported|
|is block-scoped|Supported|Not Supported|
|scope shadow resolution|Supported|Not Supported|
|cannot be in statements|Disallowed|Disallowed|
|for loop statement scope|Supported|Not Supported|
|temporal dead zone|Not Supported|Not Supported|
|for/for-in loop iteration scope|Supported|Not Supported|
|for-in loop binding shadowing parameter|Disallowed|Disallowed|
|basic support \(strict mode\)|Supported|Not Supported|
|is block-scoped \(strict mode\)|Supported|Not Supported|
|scope shadow resolution \(strict mode\)|Supported|Not Supported|
|cannot be in statements \(strict mode\)|Disallowed|Disallowed|
|for loop statement scope \(strict mode\)|Supported|Not Supported|
|temporal dead zone \(strict mode\)|Not Supported|Not Supported|
|for/for-in loop iteration scope \(strict mode\)|Supported|Not Supported|
|for-in loop binding shadowing parameter \(strict mode\)|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|block-level function declaration|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|0 parameters|Supported|Not Supported|
|1 parameter, no brackets|Supported|Not Supported|
|multiple parameters|Supported|Not Supported|
|lexical "this" binding|Supported|Not Supported|
|"this" unchanged by call or apply|Supported|Not Supported|
|can't be bound, can be curried|Supported|Not Supported|
|lexical "arguments" binding|Supported|Not Supported|
|no line break between parameters and `=>`|Disallowed|Disallowed|
|correct precedence|Disallowed|Disallowed|
|no "prototype" property|Not Supported|Not Supported|
|lexical "super" binding in constructors|Supported|Not Supported|
|lexical "super" binding in methods|Supported|Not Supported|
|lexical "new.target" binding|Not Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|class statement|Supported|Not Supported|
|is block-scoped|Supported|Not Supported|
|class expression|Supported|Not Supported|
|anonymous class|Supported|Not Supported|
|constructor|Supported|Not Supported|
|prototype methods|Supported|Not Supported|
|string-keyed methods|Supported|Not Supported|
|computed prototype methods|Supported|Not Supported|
|optional semicolons|Supported|Not Supported|
|static methods|Supported|Not Supported|
|computed static methods|Supported|Not Supported|
|accessor properties|Supported|Not Supported|
|computed accessor properties|Supported|Not Supported|
|static accessor properties|Supported|Not Supported|
|computed static accessor properties|Supported|Not Supported|
|class name is lexically scoped|Supported|Not Supported|
|computed names, temporal dead zone|Not Supported|Not Supported|
|methods aren't enumerable|Supported|Not Supported|
|implicit strict mode|Not Supported|Not Supported|
|constructor requires new|Supported|Not Supported|
|extends|Supported|Not Supported|
|extends expressions|Supported|Not Supported|
|extends null|Supported|Not Supported|
|new.target|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|statement in constructors|Supported|Not Supported|
|expression in constructors|Supported|Not Supported|
|in methods, property access|Supported|Not Supported|
|in methods, method calls|Supported|Not Supported|
|method calls use correct "this" binding|Supported|Not Supported|
|constructor calls use correct "new.target" binding|Supported|Not Supported|
|is statically bound|Supported|Not Supported|
|super\(\) invokes the correct constructor|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Disallowed|
|generator function expressions|Supported|Disallowed|
|correct "this" binding|Supported|Disallowed|
|can't use "this" with new|Supported|Disallowed|
|sending|Supported|Disallowed|
|%GeneratorPrototype%|Disallowed|Disallowed|
|%GeneratorPrototype% prototype chain|Disallowed|Disallowed|
|%GeneratorPrototype%.constructor|Disallowed|Disallowed|
|%GeneratorPrototype%.throw|Disallowed|Disallowed|
|%GeneratorPrototype%.return|Disallowed|Disallowed|
|yield operator precedence|Disallowed|Disallowed|
|yield \*, arrays|Supported|Disallowed|
|yield \*, sparse arrays|Supported|Disallowed|
|yield \*, strings|Supported|Disallowed|
|yield \*, astral plane strings|Supported|Disallowed|
|yield \*, generator instances|Supported|Disallowed|
|yield \*, generic iterables|Supported|Disallowed|
|yield \*, instances of iterables|Supported|Disallowed|
|yield \* on non-iterables is a runtime error|Supported|Disallowed|
|yield \*, iterator closing|Supported|Disallowed|
|yield \*, iterator closing via throw\(\)|Supported|Disallowed|
|shorthand generator methods|Supported|Disallowed|
|string-keyed shorthand generator methods|Supported|Disallowed|
|computed shorthand generators|Supported|Disallowed|
|shorthand generator methods, classes|Supported|Disallowed|
|computed shorthand generators, classes|Supported|Disallowed|
|shorthand generators can't be constructors|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Int8Array|Supported|Disallowed|
|Uint8Array|Supported|Disallowed|
|Uint8ClampedArray|Supported|Disallowed|
|Int16Array|Supported|Disallowed|
|Uint16Array|Supported|Disallowed|
|Int32Array|Supported|Disallowed|
|Uint32Array|Supported|Disallowed|
|Float32Array|Supported|Disallowed|
|Float64Array|Supported|Disallowed|
|DataView \(Int8\)|Supported|Disallowed|
|DataView \(Uint8\)|Supported|Disallowed|
|DataView \(Int16\)|Supported|Disallowed|
|DataView \(Uint16\)|Supported|Disallowed|
|DataView \(Int32\)|Supported|Disallowed|
|DataView \(Uint32\)|Supported|Disallowed|
|DataView \(Float32\)|Supported|Disallowed|
|DataView \(Float64\)|Supported|Disallowed|
|ArrayBuffer\[Symbol.species\]|Supported|Disallowed|
|constructors require new|Supported|Disallowed|
|constructors accept generic iterables|Supported|Disallowed|
|correct prototype chains|Disallowed|Disallowed|
|%TypedArray%.from|Supported|Disallowed|
|%TypedArray%.of|Supported|Disallowed|
|%TypedArray%.prototype.subarray|Supported|Disallowed|
|%TypedArray%.prototype.join|Supported|Disallowed|
|%TypedArray%.prototype.indexOf|Supported|Disallowed|
|%TypedArray%.prototype.lastIndexOf|Supported|Disallowed|
|%TypedArray%.prototype.slice|Supported|Disallowed|
|%TypedArray%.prototype.every|Supported|Disallowed|
|%TypedArray%.prototype.filter|Supported|Disallowed|
|%TypedArray%.prototype.forEach|Supported|Disallowed|
|%TypedArray%.prototype.map|Supported|Disallowed|
|%TypedArray%.prototype.reduce|Supported|Disallowed|
|%TypedArray%.prototype.reduceRight|Supported|Disallowed|
|%TypedArray%.prototype.reverse|Supported|Disallowed|
|%TypedArray%.prototype.some|Supported|Disallowed|
|%TypedArray%.prototype.sort|Supported|Disallowed|
|%TypedArray%.prototype.copyWithin|Supported|Disallowed|
|%TypedArray%.prototype.find|Supported|Disallowed|
|%TypedArray%.prototype.findIndex|Supported|Disallowed|
|%TypedArray%.prototype.fill|Supported|Disallowed|
|%TypedArray%.prototype.keys|Supported|Disallowed|
|%TypedArray%.prototype.values|Supported|Disallowed|
|%TypedArray%.prototype.entries|Supported|Disallowed|
|%TypedArray%.prototype\[Symbol.iterator\]|Supported|Disallowed|
|%TypedArray%\[Symbol.species\]|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|constructor arguments|Supported|Not Supported|
|constructor requires new|Supported|Not Supported|
|constructor accepts null|Supported|Not Supported|
|constructor invokes set|Supported|Not Supported|
|iterator closing|Supported|Not Supported|
|Map.prototype.set returns this|Supported|Not Supported|
|-0 key converts to +0|Supported|Not Supported|
|Map.prototype.size|Supported|Not Supported|
|Map.prototype.delete|Supported|Not Supported|
|Map.prototype.clear|Supported|Not Supported|
|Map.prototype.forEach|Supported|Not Supported|
|Map.prototype.keys|Supported|Not Supported|
|Map.prototype.values|Supported|Not Supported|
|Map.prototype.entries|Supported|Not Supported|
|Map.prototype\[Symbol.iterator\]|Supported|Not Supported|
|Map.prototype isn't an instance|Supported|Not Supported|
|Map iterator prototype chain|Supported|Not Supported|
|Map\[Symbol.species\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|constructor arguments|Supported|Not Supported|
|constructor requires new|Supported|Not Supported|
|constructor accepts null|Supported|Not Supported|
|constructor invokes add|Supported|Not Supported|
|iterator closing|Supported|Not Supported|
|Set.prototype.add returns this|Supported|Not Supported|
|-0 key converts to +0|Supported|Not Supported|
|Set.prototype.size|Supported|Not Supported|
|Set.prototype.delete|Supported|Not Supported|
|Set.prototype.clear|Supported|Not Supported|
|Set.prototype.forEach|Supported|Not Supported|
|Set.prototype.keys|Supported|Not Supported|
|Set.prototype.values|Supported|Not Supported|
|Set.prototype.entries|Supported|Not Supported|
|Set.prototype\[Symbol.iterator\]|Supported|Not Supported|
|Set.prototype isn't an instance|Supported|Not Supported|
|Set iterator prototype chain|Supported|Not Supported|
|Set\[Symbol.species\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Disallowed|
|constructor arguments|Supported|Disallowed|
|constructor requires new|Supported|Disallowed|
|constructor accepts null|Supported|Disallowed|
|constructor invokes set|Supported|Disallowed|
|frozen objects as keys|Supported|Disallowed|
|iterator closing|Supported|Disallowed|
|WeakMap.prototype.set returns this|Supported|Disallowed|
|WeakMap.prototype.delete|Supported|Disallowed|
|no WeakMap.prototype.clear method|Supported|Disallowed|
|.has, .get and .delete methods accept primitives|Disallowed|Disallowed|
|WeakMap.prototype isn't an instance|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Disallowed|
|constructor arguments|Supported|Disallowed|
|constructor requires new|Supported|Disallowed|
|constructor accepts null|Supported|Disallowed|
|constructor invokes add|Supported|Disallowed|
|iterator closing|Supported|Disallowed|
|WeakSet.prototype.add returns this|Supported|Disallowed|
|WeakSet.prototype.delete|Supported|Disallowed|
|no WeakSet.prototype.clear method|Supported|Disallowed|
|.has and .delete methods accept primitives|Disallowed|Disallowed|
|WeakSet.prototype isn't an instance|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|constructor requires new|Supported|Disallowed|
|no "prototype" property|Supported|Disallowed|
|"get" handler|Supported|Disallowed|
|"get" handler, instances of proxies|Supported|Disallowed|
|"get" handler invariants|Supported|Disallowed|
|"set" handler|Supported|Disallowed|
|"set" handler, instances of proxies|Supported|Disallowed|
|"set" handler invariants|Supported|Disallowed|
|"has" handler|Supported|Disallowed|
|"has" handler, instances of proxies|Supported|Disallowed|
|"has" handler invariants|Supported|Disallowed|
|"deleteProperty" handler|Supported|Disallowed|
|"deleteProperty" handler invariant|Supported|Disallowed|
|"getOwnPropertyDescriptor" handler|Supported|Disallowed|
|"getOwnPropertyDescriptor" handler invariants|Supported|Disallowed|
|"defineProperty" handler|Supported|Disallowed|
|"defineProperty" handler invariants|Supported|Disallowed|
|"getPrototypeOf" handler|Supported|Disallowed|
|"getPrototypeOf" handler invariant|Supported|Disallowed|
|"setPrototypeOf" handler|Supported|Disallowed|
|"setPrototypeOf" handler invariant|Supported|Disallowed|
|"isExtensible" handler|Supported|Disallowed|
|"isExtensible" handler invariant|Supported|Disallowed|
|"preventExtensions" handler|Supported|Disallowed|
|"preventExtensions" handler invariant|Supported|Disallowed|
|"ownKeys" handler|Supported|Disallowed|
|"ownKeys" handler invariant|Supported|Disallowed|
|"apply" handler|Supported|Disallowed|
|"apply" handler invariant|Supported|Disallowed|
|"construct" handler|Supported|Disallowed|
|"construct" handler invariants|Supported|Disallowed|
|Proxy.revocable|Supported|Disallowed|
|Array.isArray support|Supported|Disallowed|
|JSON.stringify support|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Reflect.get|Disallowed|Disallowed|
|Reflect.set|Disallowed|Disallowed|
|Reflect.has|Disallowed|Disallowed|
|Reflect.deleteProperty|Disallowed|Disallowed|
|Reflect.getOwnPropertyDescriptor|Disallowed|Disallowed|
|Reflect.defineProperty|Disallowed|Disallowed|
|Reflect.getPrototypeOf|Disallowed|Disallowed|
|Reflect.setPrototypeOf|Disallowed|Disallowed|
|Reflect.isExtensible|Disallowed|Disallowed|
|Reflect.preventExtensions|Disallowed|Disallowed|
|Reflect.ownKeys, string keys|Disallowed|Disallowed|
|Reflect.ownKeys, symbol keys|Disallowed|Disallowed|
|Reflect.apply|Disallowed|Disallowed|
|Reflect.construct|Disallowed|Disallowed|
|Reflect.construct sets new.target meta-property|Disallowed|Disallowed|
|Reflect.construct creates instances from third argument|Disallowed|Disallowed|
|Reflect.construct, Array subclassing|Disallowed|Disallowed|
|Reflect.construct, RegExp subclassing|Disallowed|Disallowed|
|Reflect.construct, Function subclassing|Disallowed|Disallowed|
|Reflect.construct, Promise subclassing|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Disallowed|
|constructor requires new|Supported|Disallowed|
|Promise.prototype isn't an instance|Supported|Disallowed|
|Promise.all|Supported|Disallowed|
|Promise.all, generic iterables|Supported|Disallowed|
|Promise.race|Supported|Disallowed|
|Promise.race, generic iterables|Supported|Disallowed|
|Promise\[Symbol.species\]|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Not Supported|
|typeof support|Supported|Not Supported|
|symbol keys are hidden to pre-ES6 code|Supported|Not Supported|
|Object.defineProperty support|Supported|Not Supported|
|symbols inherit from Symbol.prototype|Supported|Not Supported|
|cannot coerce to string or number|Supported|Not Supported|
|can convert with String\(\)|Supported|Not Supported|
|new Symbol\(\) throws|Supported|Not Supported|
|Object\(symbol\)|Not Supported|Not Supported|
|JSON.stringify ignores symbol primitives|Supported|Not Supported|
|JSON.stringify ignores symbol objects|Not Supported|Not Supported|
|global symbol registry|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Symbol.hasInstance|Supported|Disallowed|
|Symbol.isConcatSpreadable|Supported|Disallowed|
|Symbol.iterator, existence|Supported|Disallowed|
|Symbol.iterator, arguments object|Supported|Disallowed|
|Symbol.species, existence|Supported|Disallowed|
|Symbol.species, Array.prototype.concat|Disallowed|Disallowed|
|Symbol.species, Array.prototype.filter|Disallowed|Disallowed|
|Symbol.species, Array.prototype.map|Disallowed|Disallowed|
|Symbol.species, Array.prototype.slice|Disallowed|Disallowed|
|Symbol.species, Array.prototype.splice|Disallowed|Disallowed|
|Symbol.species, RegExp.prototype\[Symbol.split\]|Disallowed|Disallowed|
|Symbol.species, Promise.prototype.then|Disallowed|Disallowed|
|Symbol.replace|Supported|Disallowed|
|Symbol.search|Supported|Disallowed|
|Symbol.split|Supported|Disallowed|
|Symbol.match|Supported|Disallowed|
|Symbol.match, RegExp constructor|Disallowed|Disallowed|
|Symbol.match, String.prototype.startsWith|Disallowed|Disallowed|
|Symbol.match, String.prototype.endsWith|Disallowed|Disallowed|
|Symbol.match, String.prototype.includes|Disallowed|Disallowed|
|Symbol.toPrimitive|Supported|Disallowed|
|Symbol.toStringTag|Supported|Disallowed|
|Symbol.toStringTag affects existing built-ins|Supported|Disallowed|
|Symbol.toStringTag, new built-ins|Supported|Disallowed|
|Symbol.toStringTag, misc. built-ins|Supported|Disallowed|
|Symbol.unscopables|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.assign|Supported|Not Supported|
|Object.is|Supported|Not Supported|
|Object.getOwnPropertySymbols|Supported|Not Supported|
|Object.setPrototypeOf|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|function statements|Supported|Supported|
|function expressions|Supported|Supported|
|new Function|Not Supported|Not Supported|
|bound functions|Not Supported|Not Supported|
|variables \(function\)|Supported|Not Supported|
|object methods \(function\)|Supported|Not Supported|
|accessor properties|Not Supported|Not Supported|
|shorthand methods|Supported|Not Supported|
|shorthand methods \(no lexical binding\)|Supported|Not Supported|
|symbol-keyed methods|Not Supported|Not Supported|
|class statements|Supported|Not Supported|
|class expressions|Supported|Not Supported|
|variables \(class\)|Supported|Not Supported|
|object methods \(class\)|Not Supported|Not Supported|
|class prototype methods|Supported|Not Supported|
|class static methods|Supported|Not Supported|
|isn't writable, is configurable|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|String.raw|Supported|Not Supported|
|String.fromCodePoint|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|String.prototype.codePointAt|Supported|Supported|
|String.prototype.normalize|Supported|Supported|
|String.prototype.repeat|Supported|Supported|
|String.prototype.startsWith|Supported|Supported|
|String.prototype.startsWith throws on RegExp|Not Supported|Not Supported|
|String.prototype.endsWith|Supported|Supported|
|String.prototype.endsWith throws on RegExp|Not Supported|Not Supported|
|String.prototype.includes|Supported|Supported|
|String.prototype\[Symbol.iterator\]|Supported|Not Supported|
|String iterator prototype chain|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|RegExp.prototype.flags|Supported|Not Supported|
|RegExp.prototype\[Symbol.match\]|Supported|Not Supported|
|RegExp.prototype\[Symbol.replace\]|Supported|Not Supported|
|RegExp.prototype\[Symbol.split\]|Supported|Not Supported|
|RegExp.prototype\[Symbol.search\]|Supported|Not Supported|
|RegExp\[Symbol.species\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.from, array-like objects|Supported|Not Supported|
|Array.from, generator instances|Supported|Disallowed|
|Array.from, generic iterables|Supported|Not Supported|
|Array.from, instances of generic iterables|Supported|Not Supported|
|Array.from map function, array-like objects|Supported|Not Supported|
|Array.from map function, generator instances|Supported|Disallowed|
|Array.from map function, generic iterables|Supported|Not Supported|
|Array.from map function, instances of iterables|Supported|Not Supported|
|Array.from, iterator closing|Supported|Not Supported|
|Array.of|Supported|Not Supported|
|Array\[Symbol.species\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.prototype.copyWithin|Supported|Not Supported|
|Array.prototype.find|Supported|Not Supported|
|Array.prototype.findIndex|Supported|Not Supported|
|Array.prototype.fill|Supported|Not Supported|
|Array.prototype.keys|Supported|Not Supported|
|Array.prototype.values|Supported|Not Supported|
|Array.prototype.entries|Supported|Not Supported|
|Array.prototype\[Symbol.iterator\]|Supported|Not Supported|
|Array iterator prototype chain|Supported|Not Supported|
|Array.prototype\[Symbol.unscopables\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Number.isFinite|Supported|Not Supported|
|Number.isInteger|Supported|Not Supported|
|Number.isSafeInteger|Supported|Not Supported|
|Number.isNaN|Supported|Not Supported|
|Number.parseFloat|Supported|Disallowed|
|Number.parseInt|Supported|Disallowed|
|Number.EPSILON|Supported|Not Supported|
|Number.MIN\_SAFE\_INTEGER|Supported|Not Supported|
|Number.MAX\_SAFE\_INTEGER|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Math.clz32|Supported|Not Supported|
|Math.imul|Supported|Not Supported|
|Math.sign|Supported|Not Supported|
|Math.log10|Supported|Not Supported|
|Math.log2|Supported|Not Supported|
|Math.log1p|Supported|Not Supported|
|Math.expm1|Supported|Not Supported|
|Math.cosh|Supported|Not Supported|
|Math.sinh|Supported|Not Supported|
|Math.tanh|Supported|Not Supported|
|Math.acosh|Supported|Not Supported|
|Math.asinh|Supported|Not Supported|
|Math.atanh|Supported|Not Supported|
|Math.trunc|Supported|Not Supported|
|Math.fround|Supported|Not Supported|
|Math.cbrt|Supported|Not Supported|
|Math.hypot|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Date.prototype\[Symbol.toPrimitive\]|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|length property \(accessing\)|Disallowed|Disallowed|
|length property \(setting\)|Disallowed|Disallowed|
|correct prototype chain|Disallowed|Disallowed|
|Array.isArray support|Supported|Disallowed|
|Array.prototype.concat|Supported|Disallowed|
|Array.prototype.filter|Supported|Disallowed|
|Array.prototype.map|Supported|Disallowed|
|Array.prototype.slice|Supported|Disallowed|
|Array.prototype.splice|Supported|Disallowed|
|Array.from|Supported|Disallowed|
|Array.of|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Disallowed|Disallowed|
|correct prototype chain|Disallowed|Disallowed|
|RegExp.prototype.exec|Disallowed|Disallowed|
|RegExp.prototype.test|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|can be called|Disallowed|Disallowed|
|correct prototype chain|Disallowed|Disallowed|
|can be used with "new"|Disallowed|Disallowed|
|Function.prototype.call|Disallowed|Disallowed|
|Function.prototype.apply|Disallowed|Disallowed|
|Function.prototype.bind|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Disallowed|Disallowed|
|correct prototype chain|Disallowed|Disallowed|
|Promise.all|Disallowed|Disallowed|
|Promise.race|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Boolean is subclassable|Disallowed|Disallowed|
|Number is subclassable|Disallowed|Disallowed|
|String is subclassable|Disallowed|Disallowed|
|Error is subclassable|Disallowed|Disallowed|
|Map is subclassable|Disallowed|Disallowed|
|Set is subclassable|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functions|Disallowed|Disallowed|
|generator functions|Disallowed|Disallowed|
|arrow functions|Disallowed|Disallowed|
|classes|Disallowed|Disallowed|
|subclasses|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|ToPrimitive|Supported|Disallowed|
|CreateListFromArrayLike|Supported|Disallowed|
|instanceof operator|Supported|Disallowed|
|HasBinding|Supported|Disallowed|
|CreateDynamicFunction|Supported|Disallowed|
|ClassDefinitionEvaluation|Supported|Disallowed|
|IteratorComplete, IteratorValue|Supported|Disallowed|
|ToPropertyDescriptor|Supported|Disallowed|
|Object.assign|Supported|Disallowed|
|Object.defineProperties|Supported|Disallowed|
|Function.prototype.bind|Supported|Disallowed|
|Error.prototype.toString|Supported|Disallowed|
|String.raw|Supported|Disallowed|
|RegExp constructor|Supported|Disallowed|
|RegExp.prototype.flags|Supported|Disallowed|
|RegExp.prototype.test|Supported|Disallowed|
|RegExp.prototype.toString|Supported|Disallowed|
|RegExp.prototype\[Symbol.match\]|Supported|Disallowed|
|RegExp.prototype\[Symbol.replace\]|Supported|Disallowed|
|RegExp.prototype\[Symbol.search\]|Supported|Disallowed|
|RegExp.prototype\[Symbol.split\]|Supported|Disallowed|
|Array.from|Supported|Disallowed|
|Array.prototype.concat|Supported|Disallowed|
|Array.prototype iteration methods|Supported|Disallowed|
|Array.prototype.pop|Supported|Disallowed|
|Array.prototype.reverse|Supported|Disallowed|
|Array.prototype.shift|Supported|Disallowed|
|Array.prototype.splice|Supported|Disallowed|
|Array.prototype.toString|Supported|Disallowed|
|JSON.stringify|Supported|Disallowed|
|Promise resolve functions|Supported|Disallowed|
|String.prototype.match|Supported|Disallowed|
|String.prototype.replace|Supported|Disallowed|
|String.prototype.search|Supported|Disallowed|
|String.prototype.split|Supported|Disallowed|
|Date.prototype.toJSON|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.assign|Supported|Disallowed|
|Array.from|Supported|Disallowed|
|Array.of|Supported|Disallowed|
|Array.prototype.copyWithin|Supported|Disallowed|
|Array.prototype.fill|Supported|Disallowed|
|Array.prototype.pop|Supported|Disallowed|
|Array.prototype.push|Supported|Disallowed|
|Array.prototype.reverse|Supported|Disallowed|
|Array.prototype.shift|Supported|Disallowed|
|Array.prototype.splice|Supported|Disallowed|
|Array.prototype.unshift|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|\[\[Set\]\]|Supported|Disallowed|
|SetIntegrityLevel|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.prototype.copyWithin|Supported|Disallowed|
|Array.prototype.pop|Supported|Disallowed|
|Array.prototype.reverse|Supported|Disallowed|
|Array.prototype.shift|Supported|Disallowed|
|Array.prototype.splice|Supported|Disallowed|
|Array.prototype.unshift|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|\[\[Set\]\]|Supported|Disallowed|
|Object.assign|Supported|Disallowed|
|Object.prototype.hasOwnProperty|Supported|Disallowed|
|Function.prototype.bind|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|SetIntegrityLevel|Supported|Disallowed|
|TestIntegrityLevel|Supported|Disallowed|
|SerializeJSONObject|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.getPrototypeOf|Disallowed|Disallowed|
|Object.getOwnPropertyDescriptor|Disallowed|Disallowed|
|Object.getOwnPropertyNames|Disallowed|Disallowed|
|Object.seal|Disallowed|Disallowed|
|Object.freeze|Disallowed|Disallowed|
|Object.preventExtensions|Disallowed|Disallowed|
|Object.isSealed|Disallowed|Disallowed|
|Object.isFrozen|Disallowed|Disallowed|
|Object.isExtensible|Disallowed|Disallowed|
|Object.keys|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.keys|Supported|Disallowed|
|Object.getOwnPropertyNames|Supported|Disallowed|
|Object.assign|Disallowed|Disallowed|
|JSON.stringify|Disallowed|Disallowed|
|JSON.parse|Disallowed|Disallowed|
|Reflect.ownKeys, string key order|Disallowed|Disallowed|
|Reflect.ownKeys, symbol key order|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|var â¸¯;|Disallowed|Disallowed|
|var ð ‹€;|Disallowed|Disallowed|
|no escaped reserved words as identifiers|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|hoisted block-level function declaration|Supported|Disallowed|
|labeled function statements|Disallowed|Disallowed|
|function statements in if-statement clauses|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic support|Supported|Disallowed|
|multiple \_\_proto\_\_ is an error|Disallowed|Disallowed|
|not a computed property|Disallowed|Disallowed|
|not a shorthand property|Disallowed|Disallowed|
|not a shorthand method|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|get prototype|Disallowed|Disallowed|
|set prototype|Disallowed|Disallowed|
|absent from Object.create\(null\)|Disallowed|Disallowed|
|present in hasOwnProperty\(\)|Disallowed|Disallowed|
|correct property descriptor|Disallowed|Disallowed|
|present in Object.getOwnPropertyNames\(\)|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|existence|Supported|Disallowed|
|tags' names are lowercase|Supported|Disallowed|
|quotes in arguments are escaped|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|basic functionality|Supported|Disallowed|
|returns this|Supported|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|hyphens in character sets|Disallowed|Disallowed|
|invalid character escapes|Disallowed|Disallowed|
|invalid control-character escapes|Disallowed|Disallowed|
|invalid Unicode escapes|Disallowed|Disallowed|
|invalid hexadecimal escapes|Disallowed|Disallowed|
|incomplete patterns and quantifiers|Disallowed|Disallowed|
|octal escape sequences|Disallowed|Disallowed|
|invalid backreferences become octal escapes|Disallowed|Disallowed|

## ECMAScript 2009 \(ES5\) features

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Getter accessors|Supported|Supported|
|Setter accessors|Supported|Supported|
|Trailing commas in object literals|Supported|Supported|
|Trailing commas in array literals|Supported|Supported|
|Reserved words as property names|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Object.create|Supported|Supported|
|Object.defineProperty|Supported|Supported|
|Object.defineProperties|Supported|Supported|
|Object.getPrototypeOf|Supported|Supported|
|Object.keys|Supported|Supported|
|Object.seal|Supported|Supported|
|Object.freeze|Supported|Supported|
|Object.preventExtensions|Supported|Supported|
|Object.isSealed|Supported|Supported|
|Object.isFrozen|Supported|Supported|
|Object.isExtensible|Supported|Supported|
|Object.getOwnPropertyDescriptor|Supported|Supported|
|Object.getOwnPropertyNames|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Array.isArray|Supported|Supported|
|Array.prototype.indexOf|Supported|Supported|
|Array.prototype.lastIndexOf|Supported|Supported|
|Array.prototype.every|Supported|Supported|
|Array.prototype.some|Supported|Supported|
|Array.prototype.forEach|Supported|Supported|
|Array.prototype.map|Supported|Supported|
|Array.prototype.filter|Supported|Supported|
|Array.prototype.reduce|Supported|Supported|
|Array.prototype.reduceRight|Supported|Supported|
|Array.prototype.sort: compareFn must be function or undefined|Supported|Not Supported|
|Array.prototype.sort: compareFn may be explicit undefined|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Property access on strings|Supported|Supported|
|String.prototype.split|Supported|Not Supported|
|String.prototype.trim|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Date.prototype.toISOString|Supported|Supported|
|Date.now|Supported|Supported|
|Date.prototype.toJSON|Supported|Not Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|undefined|Supported|Supported|
|NaN|Supported|Supported|
|Infinity|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Number.prototype.toExponential rounds properly|Supported|Supported|
|Number.prototype.toExponential throws on Â±Infinity fractionDigits|Supported|Supported|
|Number.prototype.toExponential does not throw on edge cases|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|reserved words|Disallowed|Disallowed|
|"this" is undefined in functions|Disallowed|Disallowed|
|"this" is not coerced to object in primitive methods|Disallowed|Disallowed|
|"this" is not coerced to object in primitive accessors|Disallowed|Disallowed|
|legacy octal is a SyntaxError|Supported|Disallowed|
|assignment to unresolvable identifiers is a ReferenceError|Supported|Disallowed|
|assignment to eval or arguments is a SyntaxError|Supported|Disallowed|
|assignment to non-writable properties is a TypeError|Supported|Disallowed|
|eval or arguments bindings is a SyntaxError|Disallowed|Disallowed|
|arguments.caller removed or is a TypeError|Supported|Disallowed|
|arguments.callee is a TypeError|Supported|Disallowed|
|\(function\(\)\{\}\).caller and \(function\(\)\{\}\).arguments is a TypeError|Supported|Disallowed|
|arguments is unmapped|Disallowed|Disallowed|
|eval\(\) can't create bindings|Disallowed|Disallowed|
|deleting bindings is a SyntaxError|Disallowed|Disallowed|
|deleting non-configurable properties is a TypeError|Disallowed|Disallowed|
|"with" is a SyntaxError|Supported|Disallowed|
|repeated parameter names is a SyntaxError|Supported|Disallowed|
|function expressions with matching name and argument are valid|Disallowed|Disallowed|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|Function.prototype.bind|Supported|Supported|

|Feature|ECMAScript 2021 \(ES12\) mode|ES5 Standards mode|
|-------|-----------------------------|------------------|
|JSON|Supported|Supported|

**Parent Topic:**[JavaScript engine on the platform](../concept/c_JS_engine_upgrade.md)

