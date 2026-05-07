---
title: General guidelines for scripting
description: Write efficient scripts using a JavaScript-like language. Follow these general guidelines for naming, variables, and table access.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# General guidelines for scripting

Write efficient scripts using a JavaScript-like language. Follow these general guidelines for naming, variables, and table access.

This guide will walk you through the general guidelines for writing efficient and reliable scripts in CPQ using a JavaScript-like language. Following these guidelines will help you create maintainable, readable, and well-performing code.

## Quick summary

-   Place declarations at the top
-   Comment thoughtfully
-   Indent brackets
-   Use descriptive variable names
-   Name variables consistently
-   Avoid "new"
-   Avoid loose equality \("=="\)
-   Use "const" before "let" and "let" over "var"
-   Minimize table lookups

## Place declarations at the top

Placing variable and function declarations at the top of your script improves readability and prevents unexpected variable hoisting issues.

```
1 // Declare and initiate at the beginning
2 let firstName = "";
3 let lastName = "";
4 let price = 0;
5 let discount = 0;
6 let fullPrice = 0,
7 const myArray = [];
8 const myMap= {};
```

## Comment thoughtfully

Use comments to explain complex logic, assumptions, or any non-obvious behavior in your code. Avoid redundant comments that merely repeat the code.

## Indent brackets

Properly indenting your code improves its visual structure and makes it easier to understand, especially when dealing with nested blocks.

```
1 // Good
2 if (condition) {
3 // ...
4 if (nestedCondition) {
5 // ...
6 }
7 }
8
9 // Bad
10 if (condition) {
11 // ...
12 if (nestedCondition) {
13 // ...
14 }
15 }
```

## Use descriptive variable names

Choose names that are meaningful and describe the purpose of the variable or function. This makes your code self- documenting and easier for others to understand.

```
1 //Good
2 let quoteId = cfgRequest.partner.quote.id.value;
3 let lineID = cfgRequest.partner.quote.lineId.value;
4 let currencyISO = cfgRequest.partner.quote.currencyIsoCode.value;
5 let priceBookID = cfgRequest.partner.quote.pricebookId.value;
6
7 if (quoteId != null) {
8 cfgRequest.quoteIDTest.set("value", quoteId);
9 }
10
11 if (lineID != null) {
12 cfgRequest.lineIDTest.set("value", lineID);
13 }
14
15 if (currencyISO != null) {
16 cfgRequest.currencyISOCodeTest.set("value", currencyISO);
17 }
18
19 if (priceBookID != null) {
20 cfgRequest.pricebookIDTest.set("value", priceBookID);
21 }
22
23 //Bad
24 let x1= cfgRequest.partner.quote.id.value;
25 let x2= cfgRequest.partner.quote.lineId.value;
26 let x3= cfgRequest.partner.quote.currencyIsoCode.value;
27 let x4= cfgRequest.partner.quote.pricebookId.value;
28
29 if (x1 != null) {
30 cfgRequest.quoteIDTest.set("value", x1);
31 }
32
33 if (x2 != null) {
34 cfgRequest.lineIDTest.set("value", x2);
35 }
36
37 if (x3 != null) {
38 cfgRequest.currencyISOCodeTest.set("value", x3);
39 }
40
41 if (x4 != null) {
42 cfgRequest.pricebookIDTest.set("value", x4);
43 }
```

## Name variables consistently

Consistent naming conventions enhance code readability and maintainability. Choose either camelCase or snake\_case and stick to it. Logik field variable names use camelCase, so most organizations stay with this convention for readability.

```
1 // camelCase
2 let firstName = "JohnDoe";
3
4 // snake_case
5 let last_name = "Smith";
```

## Avoid the "new" keyword

Using the `new` keyword can use more resources, lead to memory leaks, and cause unintended behaviors. Instead, use the literal notation for object creation if possible.

-   Use `" "` instead of `new String( )`
-   Use `( )` instead of `new Number( )`
-   Use `false` instead of `new Boolean( )`
-   Use `{ }` instead of `new Map( )`
-   Use `[ ]` instead of `new Array( )`

## Avoid loose equality \("=="\)

The loose equality operator can lead to unexpected type coercion. For accurate comparisons, use the strict equality operator \(`===`\).

```
1 // Good
2 if (count === 5) {
3 // ...
4 }
5
6 // Bad
7 if (count == "5") {
8 // ...
9 }
```

## Use "const" before "let" and "let" over "var"

Choose variable declaration based on scope and mutability requirements. Use `const` for variables that won't be reassigned and `let` for variables that will change. `var` is also acceptable but is a holdover from previous versions of JavaScript.

```
1 // Using const for unchanging values
2 const TAX_RATE = 0.15;
3
4 // Using let for mutable values
5 let itemCount = 5;
```

## Minimize table lookups

Excessive table queries can impact performance. Minimize queries by fetching necessary data once and storing it in variables.

To learn about general guideliines for using the `lookup` function, see [Minimizing table queries](table_queries.md).

**Related topics**  


[Create scripts](scripting.md)

[CPQ scripting language reference](cpq-logik-io-scripting-language-reference.md)

