---
title: JSUtil - Global
description: The JSUtil script include provides shortcuts for common JavaScript routines.Checks if item is null or is undefined.Escape ampersands commonly used to define URL attributes.Escapes invalid XML characters such as "&lt; &gt; &amp;".Returns the value in a boolean GlideRecord field.Checks if item is not null and is not undefined.Checks to see if the specified object is a member of the specified class.Checks if the specified object is a Java class.Logs all the properties in the given object: name, type, and value.Checks if item is null, undefined, or evaluates to the empty string.Checks if an item is null, undefined, or evaluates to the empty string.Converts the specified object to a Boolean.Determines the type of the specified object.Restore ampersands from escaped text.Removes escape characters.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JSUtil- Global

The JSUtil script include provides shortcuts for common JavaScript routines.

This API is available in global server-side scripts, not scoped scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## JSUtil - doesNotHave\(Object item\)

Checks if item is null or is undefined.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The object to check|

|Type|Description|
|----|-----------|
|Boolean|True if the specified object is null or undefined.|

```
var x = "the quick brown fox";
var y = "";
var z;
 
gs.print("x = '" + x + "', JSUtil.doesNotHave(x) = " + JSUtil.doesNotHave(x));
gs.print("y = '" + y + "', JSUtil.doesNotHave(y) = " + JSUtil.doesNotHave(y));
gs.print("z = '" + z + "', JSUtil.doesNotHave(z) = " + JSUtil.doesNotHave(z))
```

Output:

```
x = 'the quick brown fox', JSUtil.doesNotHave(x) = false
y = '', JSUtil.doesNotHave(y) = false
z = 'undefined', JSUtil.doesNotHave(z) = true
```

## JSUtil - escapeAttr\(String text\)

Escape ampersands commonly used to define URL attributes.

|Name|Type|Description|
|----|----|-----------|
|text|String|The text|

|Type|Description|
|----|-----------|
|String|The text with ampersands properly escaped.|

```
var attr = "sysparm_query=active=true&sysparm_view=special";
 
gs.print(JSUtil.escapeAttr(attr));
```

Output: This is the returned text. If the text is displayed in the application, the page will render the escaped ampersand with a single ampersand.

```
sysparm_query=active=true&sysparm_view=special
```

## JSUtil - escapeText\(String text\)

Escapes invalid XML characters such as "&lt; &gt; &amp;".

|Name|Type|Description|
|----|----|-----------|
|text|String|The text|

|Type|Description|
|----|-----------|
|String|The text with escape characters added.|

```
var html = "<b>This is my title</b>";
 
gs.print(JSUtil.escapeText(html));
```

Output: This is the value returned. If the result is displayed in the application, the page renders the brackets back so it appears that it is not escaped.

```
<b>This is my title</b>
```

## JSUtil - getBooleanValue\(GlideRecord now\_GR, String field\)

Returns the value in a boolean GlideRecord field.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|A GlideRecord|
|field|String|The field from which to retrieve the boolean value.|

|Type|Description|
|----|-----------|
|Boolean|Returns the value in a boolean GlideRecord field, returns true if value of field is true, "true", 1, or "1".|

```
var inc = new GlideRecord("incident");
//get an active incident
inc.addActiveQuery();
inc.setLimit(1);
inc.query();
inc.next();
 
gs.print(JSUtil.getBooleanValue(inc, "active"));
```

Output: true

## JSUtil - has\(Object item\)

Checks if item is not null and is not undefined.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The Object to check|

|Type|Description|
|----|-----------|
|Boolean|True if the specified object is not null and is not undefined.|

```
var x = "the quick brown fox";
var y = "";
var z;
 
gs.print("x = '" + x + "', JSUtil.has(x) = " + JSUtil.has(x));
gs.print("y = '" + y + "', JSUtil.has(y) = " + JSUtil.has(y));
gs.print("z = '" + z + "', JSUtil.has(z) = " + JSUtil.has(z));
```

Output:

```
x = 'the quick brown fox', JSUtil.has(x) = true
y = '', JSUtil.has(y) = true
z = 'undefined', JSUtil.has(z) = false
```

## JSUtil - instance\_of\(Object item, String class\)

Checks to see if the specified object is a member of the specified class.

For JavaScript objects, this method behaves exactly like the JavaScript operator "instanceof", but also supports Java objects.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The object to check|
|class|String|The class to check|

|Type|Description|
|----|-----------|
|Boolean|True if the specified object is a member of the specified class.|

```
var a = ['a','b','c'];
var b = 10;
var c = new GlideRecord("incident");
 
gs.print("JSUtil.instance_of(a,'Array') = " + JSUtil.instance_of(a,Array));
gs.print("JSUtil.instance_of(a,'String') = " + JSUtil.instance_of(a,String));
 
gs.print("JSUtil.instance_of(b,'String') = " + JSUtil.instance_of(b,String));
 
gs.print("JSUtil.instance_of(c,'GlideRecord') = " + JSUtil.instance_of(c,GlideRecord));
```

Output:

```
JSUtil.instance_of(a,'Array') = true
JSUtil.instance_of(a,'String') = false
JSUtil.instance_of(b,'String') = false
JSUtil.instance_of(c,'GlideRecord') = true
```

## JSUtil - isJavaObject\(Object value\)

Checks if the specified object is a Java class.

|Name|Type|Description|
|----|----|-----------|
|value|Object|The object to check|

|Type|Description|
|----|-----------|
|Boolean|True if the specified object is an instance of a Java class.|

```
var tu = new TableUtils("incident");
var classes = tu.getHierarchy(); //Java ArrayList
var tables = ["task, incident"]; //JavaScript Array
 
gs.print("JSUtil.isJavaObject(classes) = " + JSUtil.isJavaObject(classes));
gs.print("JSUtil.isJavaObject(tables) = " + JSUtil.isJavaObject(tables));
```

Output:

```
JSUtil.isJavaObject(classes) = true
JSUtil.isJavaObject(tables) = false
```

## JSUtil - logObject\(Object obj, String name\)

Logs all the properties in the given object: name, type, and value.

Output is written to the console if you are running from a background script or have debug logging enables. The output is also written to the system log.

|Name|Type|Description|
|----|----|-----------|
|obj|Object|The object for which to enumerate properties|
|name|String|Optional name for the logged object|

|Type|Description|
|----|-----------|
|void| |

```
var arr = ["a","b","c"];
 
var inc = new GlideRecord("incident");
//get an active incident
inc.addActiveQuery();
inc.setLimit(1);
inc.query();
inc.next();
 
JSUtil.logObject(arr, "arr");
JSUtil.logObject(inc, "inc");
```

Output:

```
Log Object: arr
  Array of 3 elements
    [0]: string = a
    [1]: string = b
    [2]: string = c
Log Object: inc
  GlideRecord('incident') @ INC0000002
```

## JSUtil - nil\(Object item\)

Checks if item is null, undefined, or evaluates to the empty string.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The object to check|

|Type|Description|
|----|-----------|
|Boolean|True if the item is null, undefined, or evaluates to the empty string.|

```
var x = "the quick brown fox";
var y = "";
var z;
 
gs.print("x = '" + x + "', JSUtil.nil(x) = " + JSUtil.nil(x));
gs.print("y = '" + y + "', JSUtil.nil(y) = " + JSUtil.nil(y));
gs.print("z = '" + z + "', JSUtil.nil(z) = " + JSUtil.nil(z));
```

Output:

```
x = 'the quick brown fox', JSUtil.nil(x) = false
y = '', JSUtil.nil(y) = true
z = 'undefined', JSUtil.nil(z) = true
```

## JSUtil - notNil\(Object item\)

Checks if an item is null, undefined, or evaluates to the empty string.

**Note:** This method returns an error if the object provided isn’t declared.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The object to check.|

<table id="table_urk_f35_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the item exists and isn’t empty. An error returns if the object provided isn’t declared.Valid values:

-   true: The object provided has been declared and defined. If the object is a string, it isn’t empty.
-   false: The object provided is null, undefined, or evaluates to an empty string.

</td></tr></tbody>
</table>The following example shows results for a string variable, an empty string variable, and an undefined variable.

```
var x = "the quick brown fox";
var y = "";
var z;

gs.print("x = '" + x + "', JSUtil.notNil(x) = " + JSUtil.notNil(x));
gs.print("y = '" + y + "', JSUtil.notNil(y) = " + JSUtil.notNil(y));
gs.print("z = '" + z + "', JSUtil.notNil(z) = " + JSUtil.notNil(z));
```

Output:

```
x = 'the quick brown fox', JSUtil.notNil(x) = true
y = '', JSUtil.notNil(y) = false
z = 'undefined', JSUtil.notNil(z) = false
```

## JSUtil - toBoolean\(Object item\)

Converts the specified object to a Boolean.

|Name|Type|Description|
|----|----|-----------|
|item|Object|The object to convert|

|Type|Description|
|----|-----------|
|Boolean|If the specified object is a boolean, it is passed through. Non-zero numbers return true. Null or undefined return false. Strings return true only if exactly equal to 'true'.|

```
var zero = 0;
var one = 1;
var number = 12;
var trueBoolean = true;
var trueString = "true";
var otherString = "random text";
 
gs.print("JSUtil.toBoolean(zero) = " + JSUtil.toBoolean(zero));
gs.print("JSUtil.toBoolean(one) = " + JSUtil.toBoolean(one));
gs.print("JSUtil.toBoolean(number) = " + JSUtil.toBoolean(number));
gs.print("JSUtil.toBoolean(trueBoolean) = " + JSUtil.toBoolean(trueBoolean));
gs.print("JSUtil.toBoolean(trueString) = " + JSUtil.toBoolean(trueString));
gs.print("JSUtil.toBoolean(otherString) = " + JSUtil.toBoolean(otherString));
```

Output:

```
JSUtil.toBoolean(zero) = false
JSUtil.toBoolean(one) = true
JSUtil.toBoolean(number) = true
JSUtil.toBoolean(trueBoolean) = true
JSUtil.toBoolean(trueString) = true
JSUtil.toBoolean(otherString) = false
```

## JSUtil - type\_of\(Object value\)

Determines the type of the specified object.

|Name|Type|Description|
|----|----|-----------|
|value|Object|The object to check|

<table id="table_jc5_lj5_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The type of the specified object. -   'null' if the given value is null or undefined
-   'string' if the given value is a primitive string or a String wrapper instance
-   'number' if the given value is a primitive number or a Number wrapper instance
-   'boolean' if the given value is a primitive boolean or a Boolean wrapper instance
-   'function' if the given value is a function
-   'object' otherwise

</td></tr></tbody>
</table>```
var a = ["a","b","c"];
var b = 10;
var c = new GlideRecord("incident");
var d = true;
var e;
 
gs.print("JSUtil.type_of(a) = " + JSUtil.type_of(a));
gs.print("JSUtil.type_of(b) = " + JSUtil.type_of(b));
gs.print("JSUtil.type_of(c) = " + JSUtil.type_of(c));
gs.print("JSUtil.type_of= " + JSUtil.type_of(d));
gs.print("JSUtil.type_of(e) = " + JSUtil.type_of(e));
```

Output:

```
JSUtil.type_of(a) = object
JSUtil.type_of(b) = number
JSUtil.type_of(c) = object
JSUtil.type_of= boolean
JSUtil.type_of(e) = null
```

## JSUtil - unescapeAttr\(String text\)

Restore ampersands from escaped text.

|Name|Type|Description|
|----|----|-----------|
|text|String|The text|

|Type|Description|
|----|-----------|
|String|The text with escape characters removed.|

```
var attr = "sysparm_query=active=true&amp;sysparm_view=special";
 
gs.print(JSUtil.unescapeAttr(attr));
```

Output:

```
sysparm_query=active=true&sysparm_view=special
```

## JSUtil - unescapeText\(String text\)

Removes escape characters.

|Name|Type|Description|
|----|----|-----------|
|text|String|The text to process.|

|Type|Description|
|----|-----------|
|String|The the text without escape characters.|

```
var html = "&lt;b&gt;This is my title&lt;/b&gt;";
 
gs.print(JSUtil.unescapeText(html));
```

Output: This is the value returned. If the text is displayed in the application the page, it renders the html tags and displays the text in bold.

```
<b>This is my title</b>
```

