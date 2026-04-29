---
title: JSON - Scoped
description: The JSON script include provides scoped methods to create JSON objects from a string, and to turn JSON objects into strings.Creates an object or primitive type from a JSON formatted string.Creates a string from a JSON object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JSON- Scoped

The JSON script include provides scoped methods to create JSON objects from a string, and to turn JSON objects into strings.

For scoped applications, the JSON API uses static methods that call the JavaScript ES5 native JSON object.

**Note:** Use the global keyword with JSON method calls in scoped scripts, for example, `global.JSON.stringify()`. Not using the global keyword could result in an error message, such as `ScopedRhinoObjectWrapper: not a wrappable type: com.glide.script.FieldGlideDescriptor`.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped JSON - parse\(String str\)

Creates an object or primitive type from a JSON formatted string.

|Name|Type|Description|
|----|----|-----------|
|str|String|JSON formatted string.|

|Type|Description|
|----|-----------|
|Object|Object created from the specified string.|

```
var str = '{"name":"George","lastname":"Washington"}';
var obj = global.JSON.parse(str);
gs.info('The first name is ' + obj.name);
```

Output:

```
The first name is George
```

## Scoped JSON - stringify\(Object jsonObject\)

Creates a string from a JSON object.

|Name|Type|Description|
|----|----|-----------|
|jsonObject|Object|JSON object to turn into a string.|

|Type|Description|
|----|-----------|
|String|JSON-formatted string.|

```
var obj = {"name":"George","lastname":"Washington"};
var str =  global.JSON.stringify(obj);
gs.info('The object ' + str);
```

Output:

```
The object {"name":"George","lastname":"Washington"}
```

