---
title: Convert SNC Regex expressions to enhanced regex expressions
description: When you upgrade to Eureka Patch 5 or later releases, you should convert scripts that use the SNC.Regex API to use regular JavaScript expressions.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using regular expressions, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Convert SNC Regex expressions to enhanced regex expressions

When you upgrade to Eureka Patch 5 or later releases, you should convert scripts that use the SNC.Regex API to use regular JavaScript expressions.

## Procedure

1.  From the original expression, such as: `SNC.Regex("/expr/is");`, create a new regular expression object using the pattern with the slashes stripped.

    ```
    new RegExp('expr');
    ```

2.  Move the SNC.Regex flags to the start of the expression using Java’s inline flag special construct.

    ```
    new RegExp('(?is)expr');
    ```

3.  Add the *j* flag to the `RegExp` to tell the engine to treat the expression as a Java expression.

    **Note:** If you know that the script being converted does not use Java syntax, it is not necessary to use the *j* flag.

    ```
    new RegExp('(?is)expr', 'j');
    ```

4.  Add the *g* flag to handle multiple matches or a global replace.

    ```
    new RegExp('(?is)expr', 'jg');
    ```


## Example

Using SNC.Regex:

```
var r = new SNC.Regex('/world/');
var str = 'helloworld';
var replaced = r.replaceAll(str, 'there');
// replaced == 'hellothere'
```

Using a JavaScript regular expression:

```
var r = new RegExp('world', 'jg');
var str = 'helloworld';
var replaced = str.replace(r, 'there');
// replaced == 'hellothere'
```

**Parent Topic:**[Using regular expressions in server-side scripts](../concept/c_RegularExpressionsInScripts.md)

