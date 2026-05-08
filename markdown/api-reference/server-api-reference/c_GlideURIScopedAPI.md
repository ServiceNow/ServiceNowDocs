---
title: GlideURI - Scoped
description: The GlideURI API provides methods to handle URI parameters in a scoped application.Instantiates a GlideURI object.Returns the value of the specified parameter.Returns the file name portion of the URI.Sets the specified parameter to the specified value.Reconstructs the URI string and performs the proper URL encoding by converting non-valid characters to their URL code. For example, converting &amp; to '%26'.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideURI- Scoped

The GlideURI API provides methods to handle URI parameters in a scoped application.

**Note:** Do not use the GlideURI API in scripts that are executed during export or in background jobs.

For more information on using URIs:

-   Navigate by URL
-   Navigation stack

See also: [GlideURI - Global](../../GlideURIGlobal/concept/GlideURIGlobalAPI.md#) .

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideURI - GlideURI\(\)

Instantiates a GlideURI object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## Scoped GlideURI - get\(String name\)

Returns the value of the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name.|

|Type|Description|
|----|-----------|
|String|The value for the specified parameter.|

```
var gURI = new GlideURI();
gURI.set('sysparm_query', 'priority=2^active=true' );
var fileString = gURI.get('sysparm_query');
gs.info(fileString);
```

Output:

```
priority=2^active=true
```

## Scoped GlideURI - getFileFromPath\(\)

Returns the file name portion of the URI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The file name portion of the URI.|

```
var gURI = new GlideURI();
 
var fileString = gURI.getFileFromPath();
gs.info(fileString);
```

## Scoped GlideURI - set\(String name, String value\)

Sets the specified parameter to the specified value.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name.|
|value|String|The value.|

|Type|Description|
|----|-----------|
|None| |

```
var gURI = new GlideURI();
gURI.set('sysparm_query', 'priority=2^active=true' );
var fileString = gURI.get('sysparm_query');
gs.info(fileString);
```

Output:

```
priority=2^active=true
```

## Scoped GlideURI - toString\(String path\)

Reconstructs the URI string and performs the proper URL encoding by converting non-valid characters to their URL code. For example, converting &amp; to '%26'.

Parameters set with the set\(\) method are encoded with the URI as well.

|Name|Type|Description|
|----|----|-----------|
|path|String|The base portion of the system URL to which the URI is appended.|

|Type|Description|
|----|-----------|
|String|The URL.|

```
var gURI = new GlideURI();
fileString = gURI.toString('https://<your instance>.service-now.com/navpage.do');
```

