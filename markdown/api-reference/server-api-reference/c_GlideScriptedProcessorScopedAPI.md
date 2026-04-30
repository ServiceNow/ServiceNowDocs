---
title: GlideScriptedProcessor - Scoped
description: The GlideScriptedProcessor API provides a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT, JSON, or HTML. ServiceNow processors are equivalent to Java servlets.Redirects to the specified URL.Encodes an object as a JSON string and writes it to the current URL.Writes the specified string to the current URL.Writes the specified string to the current URL in the specified character-encoding.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideScriptedProcessor- Scoped

The GlideScriptedProcessor API provides a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT, JSON, or HTML. ServiceNow processors are equivalent to Java servlets.

Use this API in processor scripts to access the processor \(servlet\) capabilities. There are no constructors for the ScopedGlideScriptedProcessor APIs. The methods are called using the global variable *g\_processor*.

A useful global variable, *g\_target*, is available in processor scripts. It contains the table name extracted from the URL.

The URL to a processor has the format: `https://<instance name.servicenow.com>/<path endpoint>.do?<parameter endpoint>=<value>` where the path endpoint and parameter endpoint are defined on the processor form.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideScriptedProcessor - redirect\(String url\)

Redirects to the specified URL.

|Name|Type|Description|
|----|----|-----------|
|url|String|Destination URL|

|Type|Description|
|----|-----------|
|void| |

```
//Do whatever processing you need and redirect to the homepage
g_processor.redirect("/navpage.do")
```

## GlideScriptedProcessor - writeJSON\(Object o\)

Encodes an object as a JSON string and writes it to the current URL.

|Name|Type|Description|
|----|----|-----------|
|o|Object|The object to encode to a JSON string.|

|Type|Description|
|----|-----------|
|void| |

```
var map = {"key1":"value1","key2":"value2"};
g_processor.writeJSON(map);
```

## GlideScriptedProcessor - writeOutput\(String s\)

Writes the specified string to the current URL.

|Name|Type|Description|
|----|----|-----------|
|s|String|The string to write.|

|Type|Description|
|----|-----------|
|void| |

```
var name = g_request.getParameter("name");
g_processor.writeOutput("Hello " + name);
```

## GlideScriptedProcessor - writeOutput\(String contentType, String s\)

Writes the specified string to the current URL in the specified character-encoding.

|Name|Type|Description|
|----|----|-----------|
|contentType|String|Sets the content type of the response sent to the client, if the response has not been committed, and may include a character-encoding specification.|
|s|String|String to write.|

|Type|Description|
|----|-----------|
|void| |

```
var name = g_request.getParameter("name");
g_processor.writeOutput("text/plain", "Hello " + name);
```

