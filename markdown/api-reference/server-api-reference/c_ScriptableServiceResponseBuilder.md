---
title: RESTAPIResponse - Scoped, Global
description: The RESTAPIResponse API provides methods that allow you to build a RESTful response to a scripted REST API request.Returns the ResponseStreamWriter for this response, allowing you to write directly to the response stream.Sets the body content to send in the web service response.Assigns a value to the Content-Type header in the web service response.Configures the REST response to return an error.Assign a value to a REST service response header.Sets the headers for the web service response.Assigns a value to the Location header in the web service response.Sets the status code number for the web service response.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTAPIResponse - Scoped, Global

The RESTAPIResponse API provides methods that allow you to build a RESTful response to a scripted REST API request.

This API runs in the `sn_ws` namespace.

**Note:** You cannot instantiate objects of this type. Objects of this type are created automatically and are accessible only in scripted REST API resource scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTAPIResponse - getStreamWriter\(\)

Returns the ResponseStreamWriter for this response, allowing you to write directly to the response stream.

Set the content type and status code using the setHeaders and setStatus functions prior to calling the getStreamWriter function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|RESTAPIResponseStream - Scoped, Global|The ResponseStreamWriter for this response. You can use this object to write directly to the response stream.|

```
response.setContentType('application/json');
response.setStatus(200);
var writer = response.getStreamWriter();
```

## RESTAPIResponse - setBody\(Object body\)

Sets the body content to send in the web service response.

<table id="table_yzt_cmr_qr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

body

</td><td>

Object

</td><td>

The response body, as a JavaScript object.

 The body content is automatically serialized to JSON or XML depending on the value of the **Accept** header passed in the request.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var body = {};
body.name = "incident";
body.number = "1234";
body.caller = {"id": "user1"};
response.setBody(body);

```

```
var bodyArray = [];
var body = {};
body.name = "incident";
body.number = "1234";
body.caller = {"id":"user1"};
bodyArray.push(body);
response.setBody(bodyArray);
```

## RESTAPIResponse - setContentType\(String contentType\)

Assigns a value to the Content-Type header in the web service response.

You must set a response content type before writing the response. The content type is set automatically for string responses, based on the request Accept header value.

Setting an invalid content type causes the response to default to JSON. Failing to set a content type results in a status code 500 error when sending a binary response.

See the [W3 Content-Type header documentation](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.17) for more information about this header.

|Name|Type|Description|
|----|----|-----------|
|contentType|String|The content type of the response body, such as application/json.|

|Type|Description|
|----|-----------|
|void| |

```
response.setContentType('application/json');
```

## RESTAPIResponse - setError\(Object error\)

Configures the REST response to return an error.

<table id="table_apv_hb3_zs" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object

</td><td>

Error object. For more information about the types of error objects that can be used, see [Scripted REST API example - script samples](../../../../../integrate/custom-web-services/reference/r_ScriptedRESTServiceScriptExamples.md).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to return an error from within a scripted REST resource.

```
var queryParams = request.queryParams;
var userId = String(queryParams.user_id || '');
var fileId = String(queryParams.file_id || '');
if (!userId || !fileId){
  response.setError(new sn_ws_err.BadRequestError('Missing required parameters.'));
  return;
}
```

## RESTAPIResponse - setHeader\(String header, String value\)

Assign a value to a REST service response header.

|Name|Type|Description|
|----|----|-----------|
|header|String|The header you want to set.|
|value|String|The value to assign the specified header.|

|Type|Description|
|----|-----------|
|void| |

```
response.setHeader("Location","<URI>");
```

## RESTAPIResponse - setHeaders\(Object headers\)

Sets the headers for the web service response.

|Name|Type|Description|
|----|----|-----------|
|headers|Object|A JavaScript object listing each header and the value to assign that header.|

|Type|Description|
|----|-----------|
|void| |

```
var headers = {};
headers.X-Total-Count=100;
headers.Location='https://instance.service-now.com/<endpoint_to_resource>';
response.setHeaders(headers);
```

## RESTAPIResponse - setLocation\(String location\)

Assigns a value to the Location header in the web service response.

See the [W3 Location header documentation](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.30) for more information about this header.

|Name|Type|Description|
|----|----|-----------|
|None|String|An absolute URI to redirect the response recipient to.|

|Type|Description|
|----|-----------|
|void| |

## RESTAPIResponse - setStatus\(Number status\)

Sets the status code number for the web service response.

|Name|Type|Description|
|----|----|-----------|
|status|Number|The status code to send in the response, such as 200 to indicate success. Passing a non-numerical value, such as a string, causes the status code to default to 0.|

|Type|Description|
|----|-----------|
|void| |

```
response.setStatus(200);
```

