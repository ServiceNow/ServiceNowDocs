---
title: JSON - Global
description: The JSON script include provides methods to create JSON objects from a string, and to turn JSON objects into strings.Creates an instance of the JSON class.Creates an object or primitive type from a JSON formatted string.Creates a string from a JSON object.Creates an object or primitive type from a JSON formatted string.Creates a string from a JSON object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JSON- Global

The JSON script include provides methods to create JSON objects from a string, and to turn JSON objects into strings.

This API has dynamic and static methods. You access the dynamic methods by creating a JSON object. To use the dynamic methods in a scoped application, add the global prefix when calling the constructor. You access the static methods by using the static JSON object.

The JavaScript ES5 native JSON object is used instead of the JSON static methods. If your script needs the old behavior, use the encode\(\) and decode\(\) methods.

This example creates a JSON object.

```
// obj is a JSON formatted object
var parser = new JSON(); // encode() and decode() are dynamic methods.
var str = parser.encode(obj);
```

The encode\(\) and decode\(\) methods are deprecated. Use the JavaScript JSON object instead.

This example creates a JSON object in a scoped script.

```
// obj is a JSON formatted object
var parser = new global.JSON();
var str = parser.encode(obj);

```

This example uses the static methods.

```
// obj is a JSON formatted object
var str =  JSON.stringify(obj);
// str is a string containing content to be turned into a JSON formatted object
var obj = JSON.parse(str);

```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## JSON - JSON\(\)

Creates an instance of the JSON class.

This class is deprecated. Use the JavaScript JSON object instead.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## JSON - decode\(String str\)

Creates an object or primitive type from a JSON formatted string.

**Note:** This class is deprecated. Use the JavaScript JSON object instead.

|Name|Type|Description|
|----|----|-----------|
|str|String|A JSON formatted string.|

|Type|Description|
|----|-----------|
|Object|An object created from the specified string.|

```
var str = '{"name":"George","lastname":"Washington"}';
var parser = new JSON();
var obj = parser.decode(str);
gs.info('The first name is '  + obj.name);
```

Output: The first name is George

To use in a scoped script.

```
var str = '{"name":"George","lastname":"Washington"}';
var parser = new global.JSON();
var obj = parser.decode(str);
gs.info('The first name is '  + obj.name);
```

Output: The first name is George

## JSON - encode\(Object jsonObject\)

Creates a string from a JSON object.

**Note:** This class is deprecated. Use the JavaScript JSON object instead.

|Name|Type|Description|
|----|----|-----------|
|jsonObject|Object|The JSON object to be turned into a string.|

|Type|Description|
|----|-----------|
|String|A JSON formatted string.|

```
var obj = {"name":"George","lastname":"Washington"};
var parser = new JSON();
var str = parser.encode(obj);
gs.info('The object '  + str);
```

Output: The object \{"lastname":"Washington","name":"George"\}

To use in a scoped script.

```
var obj = {"name":"George","lastname":"Washington"};
var parser = new global.JSON();
var str = parser.encode(obj);
gs.info('The object '  + str);
```

## JSON - parse\(String str\)

Creates an object or primitive type from a JSON formatted string.

The JavaScript ES5 native JSON object is used instead of the JSON static methods. If your script needs the old behavior, use the encode\(\) and decode\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|str|String|A JSON formatted string.|

|Type|Description|
|----|-----------|
|Object|An object created from the specified string.|

```
var str = '{"name":"George","lastname":"Washington"}';
var obj = JSON.parse(str);
gs.info('The first name is '  + obj.name);
```

Output: The first name is George

## JSON - stringify\(Object jsonObject\)

Creates a string from a JSON object.

The JSON.stringify\(\) method can only convert numbers, strings, and Java native objects to strings. It cannot convert user-defined objects to strings, unless those objects provide a toJSON\(\) method. The call to current.sys\_id\(\) returns a GlideElement object which does not have a toJSON\(\) method, so the return value for stringify is empty: "\{\}". The JavaScript ES5 native JSON object is used instead of the JSON static methods. If your script needs the old behavior, use the encode\(\) and decode\(\) methods.

JSON.stringify\(\) converts a value to JSON notation using the following guidelines:

-   If the value has a toJSON\(\) method, it is responsible for defining the data that is serialized.
-   Boolean, number, and string objects are converted to the corresponding primitive values during stringification; in accordance with the traditional conversion semantics.
-   If a function, undefined, or a symbol is encountered during conversion, it is either omitted \(when it is found in an object\) or censored to null \(when it is found in an array\). JSON.stringify\(\) also returns undefined when passing in "pure" values, such as `JSON.stringify(function(){})` or `JSON.stringify(undefined)`.
-   All symbol-keyed properties are ignored, even when using a *replacer\(\)* function.
-   Instances of Date implement the toJSON\(\) function by returning a string \(the same as date.toISOString\(\)\), thus they are treated as strings.
-   The numbers Infinity and NaN, as well as the value null, are all considered null.
-   For all other object instances, only their enumerable properties are serialized.

|Name|Type|Description|
|----|----|-----------|
|jsonObject|Object|JSON object to turn into a string.|

|Type|Description|
|----|-----------|
|String|JSON formatted string.|

```
var obj = {"name":"George","lastname":"Washington"};
var str =  JSON.stringify(obj);
gs.info('The object '  + str);

```

Output: The object \{"name":"George","lastname":"Washington"\}

It is also possible to define a replacer\(\) function and use that in the stringify\(\) call. This function leverages the GlideElement.toString\(\) method to provide a string representation of the GlideElement object.

```
function replacer(name, val) {
   // convert GlideElement to string
   if ( val && val.constructor === GlideElement ) {
       return val.toString();
   } else {
       return val; // return as is
   }
};

var s = global.JSON.stringify(json_obj, replacer);
gs.info("json="+s);

```

