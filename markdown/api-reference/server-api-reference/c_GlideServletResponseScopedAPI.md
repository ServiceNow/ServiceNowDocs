---
title: GlideServletResponse - Scoped
description: The GlideServletResponse API provides methods to use in processor scripts.Sends a temporary redirect to the client.Sets the MIME type of the responseSets a response header to the specified value.Sets the status code for the response.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideServletResponse- Scoped

The GlideServletResponse API provides methods to use in processor scripts.

ServiceNow processor scripts are equivalent to Java servlets. Processor scripts provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT, JSON, or HTML. Use the GlideServletResponse API in processor scripts to access the [HttpServletResponse](http://docs.oracle.com/javaee/1.4/api/javax/servlet/http/HttpServletResponse.html) object. The GlideServletResponse object provides a subset of the HttpServletResponse APIs. The methods are called using the global variable *g\_response*.

A useful global variable, *g\_target*, is available in processor scripts. It contains the table name extracted from the URL.

The URL to a processor has the format: `https://<instance name.servicenow.com>/<path endpoint>.do?<parameter endpoint>=<value>` where the path endpoint and parameter endpoint are defined on the processor form.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideServletResponse - sendRedirect\(String location\)

Sends a temporary redirect to the client.

|Name|Type|Description|
|----|----|-----------|
|location|String|The URL to receive the response.|

|Type|Description|
|----|-----------|
|void| |

## GlideServletResponse - setContentType\(String type\)

Sets the MIME type of the response

|Name|Type|Description|
|----|----|-----------|
|type|String|The MIME type.|

|Type|Description|
|----|-----------|
|void| |

```
g_response.setContentType('text/html;charset=UTF-8');
```

## GlideServletResponse - setHeader\(String key, String value\)

Sets a response header to the specified value.

|Name|Type|Description|
|----|----|-----------|
|key|String|Specifies the header.|
|value|String|The value to be assigned to the header. If the header exists, it is overwritten.|

|Type|Description|
|----|-----------|
|void| |

```
g_response.setHeader("host", "instance.service-now.com");
```

## GlideServletResponse - setStatus\(Number status\)

Sets the status code for the response.

|Name|Type|Description|
|----|----|-----------|
|status|Number|The status to be set.|

|Type|Description|
|----|-----------|
|void| |

```
// set the status to okay
g_response.setStatus(200);
```

