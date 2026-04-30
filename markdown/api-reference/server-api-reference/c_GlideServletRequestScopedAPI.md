---
title: GlideServletRequest - Scoped
description: The GlideServletRequest API provides methods to use in processor scripts.Returns the MIME type of the body of the request.Returns the header value.Returns a comma-separated list of header names.Returns the header values.Returns the value of the parameter contained in the request URL.Returns a list of URL parameters that were used in the request URI.Returns the query string from the request.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideServletRequest- Scoped

The GlideServletRequest API provides methods to use in processor scripts.

ServiceNow processor scripts are equivalent to Java servlets. Processor scripts provide a customizable URL endpoint that can execute arbitrary server-side JavaScript code and produce output such as TEXT, JSON, or HTML. Use the GlideServletRequest API in processor scripts to access the [HttpServletRequest](http://docs.oracle.com/javaee/1.4/api/javax/servlet/http/HttpServletRequest.html) object. The GlideServletRequest object provides a subset of the HttpServletRequest APIs. The methods are called using the global variable *g\_request*.

A useful global variable, *g\_target*, is available in processor scripts. It contains the table name extracted from the URL.

The URL to a processor has the format: `https://<instance name.servicenow.com>/<path endpoint>.do?<parameter endpoint>=<value>` where the path endpoint and parameter endpoint are defined on the processor form.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideServletRequest - getContentType\(\)

Returns the MIME type of the body of the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The content type, returns null if the content type is not known.|

```
var contentType = g_request.getContentType();
```

## GlideServletRequest - getHeader\(String name\)

Returns the header value.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the header to be retrieved.|

|Type|Description|
|----|-----------|
|String|The header.|

```
var headerValue = g_request.getHeader("host");
```

Output:

```
demonightlyus.service-now.com
```

## GlideServletRequest - getHeaderNames\(\)

Returns a comma-separated list of header names.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of header names as a string.|

```
var headerList = g_request.getHeaderNames();
```

Output:

```
host,connection,cache-control,authorization,accept,user-agent,accept-encoding,accept-language,
cookie,x-forwarded-proto,x-forwarded-host,x-forwarded-for
```

## GlideServletRequest - getHeaders\(String name\)

Returns the header values.

|Name|Type|Description|
|----|----|-----------|
|name|String|Names of the headers to be retrieved.|

|Type|Description|
|----|-----------|
|Array|An array of header values as a string.|

```
var headerValue = g_request.getHeaders("host");
```

Output:

```
demonightlyus.service-now.com
```

## GlideServletRequest - getParameter\(String name\)

Returns the value of the parameter contained in the request URL.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the parameter to be retrieved. This can be the parameter endpoint from the processor form.|

|Type|Description|
|----|-----------|
|Object|The parameter value. Returns null if the parameter is not found.|

```
var name = g_request.getParameter("x_snc_custom_x_snc_name");
```

## GlideServletRequest - getParameterNames\(\)

Returns a list of URL parameters that were used in the request URI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of parameter names as a string.|

```
var paramList = g_request.getParameterNames();
```

## GlideServletRequest - getQueryString\(\)

Returns the query string from the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The query string.|

This example uses the request URL: `https://instance.service-now.com/x_custom_app_customApp.do?x_custom_app_name=George&bell=rung`.

```
var queryString = g_request.getQueryString();
g_processor.writeOutput("The query string is: " + queryString);
```

Output:

```
The query string is: x_custom_app_name=George&bell=rung
```

