---
title: j2js - Global
description: The j2js script include enables you to convert Java objects to JavaScript objects.Converts a Java object from system code to a JavaScript object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# j2js- Global

The j2js script include enables you to convert Java objects to JavaScript objects.

If the given value is a Java object that can be converted to an equivalent JavaScript object, that conversion is performed and the result is returned. Otherwise the original Java object is returned.

The j2js class is available to server-side scripts.

The specific conversion performed in the order they are checked.

-   Java String -&gt; JavaScript string
-   Java Boolean -&gt; JavaScript boolean
-   Java Integer -&gt; JavaScript number
-   Java Long -&gt; JavaScript number
-   Java Double -&gt; JavaScript number
-   Java Byte -&gt; JavaScript number
-   Java Float -&gt; JavaScript number
-   Java Short -&gt; JavaScript number
-   Java Character -&gt; JavaScript number
-   Java Array -&gt; JavaScript Array with order preserved
-   Java List -&gt; JavaScript Array with order preserved
-   Java Map -&gt; JavaScript Object with the key/value pairs translated into property/value pairs
-   Java Set -&gt; JavaScript Array in arbitrary order

Conversions are performed recursively on the elements of arrays, lists, or collections. For example, given a Java ArrayList of ArrayLists of strings, this will return a JavaScript Array of Arrays of strings.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## j2js - j2js\(Object javaObject\)

Converts a Java object from system code to a JavaScript object.

|Name|Type|Description|
|----|----|-----------|
|javaObject|Object|A Java object from system code such as a Packages call.|

|Type|Description|
|----|-----------|
|Object|A JavaScript object if the parameter can be converted, otherwise it returns the Java object.|

```
var tu = new TableUtils("cmdb_ci_win_server");
var classes = tu.getHierarchy();
//getHierarchy returns a Java ArrayList, which is not exactly like a JavaScript Array
//for example you cannot get length
gs.print("classes = " + classes);
gs.print("classes.length = " + classes.length);
 
//convert to a JavaScript Array
gs.include("j2js");
var jsClasses = j2js(classes);
gs.print("jsClasses = " + jsClasses);
gs.print("jsClasses.length = " + jsClasses.length);
```

Output:

```
classes = [cmdb_ci_win_server, cmdb_ci_server, cmdb_ci_computer, cmdb_ci_hardware, cmdb_ci]
classes.length = undefined
jsClasses = cmdb_ci_win_server,cmdb_ci_server,cmdb_ci_computer,cmdb_ci_hardware,cmdb_ci
jsClasses.length = 5
```

