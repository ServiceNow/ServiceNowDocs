---
title: Jelly escaping types
description: You use different methods when escaping characters in JavaScript and HTML. JavaScript uses the backslash character, and HTML uses the ampersand character.You can handle character escaping in Jelly files. XML escaping behavior can be modified only by users with the security\_admin role.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Jelly tags, Creating custom UI Pages and UI macros, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Jelly escaping types

You use different methods when escaping characters in JavaScript and HTML. JavaScript uses the backslash character, and HTML uses the ampersand character.

**Note:** This functionality requires a knowledge of JavaScript, HTML, and Apache Jelly \(a Java and XML based scripting and processing engine for turning XML into executable code\).

There are two different types of escaping that is required when generating output from Jelly:

-   JavaScript
-   HTML

The escaping for each of these consists of the following types.

<table id="simpletable_j3d_w44_mq"><thead><tr><th>

Type

</th><th>

From

</th><th>

To

</th></tr></thead><tbody><tr><td>

JavaScript

</td><td>

' \(single quote\)

</td><td>

\\'

</td></tr><tr><td>

 

</td><td>

" \(double quote\)

</td><td>

\\"

</td></tr><tr><td>

 

</td><td>

CR \(carriage return\)

</td><td>

\(blank\)

</td></tr><tr><td>

 

</td><td>

NL \(newline\)

</td><td>

\\n \('\\' followed by 'n'\)

</td></tr><tr><td>

HTML

</td><td>

&amp; \(ampersand\)

</td><td>

&amp;amp;

</td></tr><tr><td>

 

</td><td>

&lt; \(less than\)

</td><td>

&amp;lt;

</td></tr><tr><td>

 

</td><td>

&gt; \(greater than\)

</td><td>

&amp;gt;

</td></tr></tbody>
</table>You can also escape HTML using the getHTMLValue\(\) function which will enforce all line breaks and escape the characters mentioned above. It can be used as follows:

```
${test.getHTMLValue()} 
```

**Parent Topic:**[Jelly tags](../../general-scripting/reference/r_JellyTags.md)

## Add escaping to a Jelly replacement

You can handle character escaping in Jelly files. XML escaping behavior can be modified only by users with the security\_admin role.

### About this task

**Note:** This functionality requires a knowledge of JavaScript, HTML, and Apache Jelly \(a Java and XML based scripting and processing engine for turning XML into executable code\).

### Procedure

1.  Add a prefix to the `${expression}` or `$[expression]` indicating the escaping to be performed.

    ```
    ${JS:expression}
    ${HTML:expression}
    ```

    The prefix tells the system to take the result of the expression and escape it before outputting. The escaping may be combined by specifying a comma-separated list of prefixes:

    ```
    ${JS,HTML:expression} 
    ```


