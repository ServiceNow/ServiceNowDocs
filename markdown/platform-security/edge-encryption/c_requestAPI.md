---
title: request
description: The request object is a global object available in Edge Encryption rule action and condition scripts.Returns the request as an iterable object of type JsonNode.Returns the request content as an iterable object of type XMLContent.Returns true if the given path exists in the XML DOM.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# request

The request object is a global object available in Edge Encryption rule action and condition scripts.

The request object is a JavaScript object that represents the client request coming in to the Edge Encryption proxy server. You must build your encryption rule to parse the request object, map request object values to fields in a table on the instance, and encrypt any sensitive data in the request object.

The request object includes the following attributes and data from the client request:

|Field|Description|
|-----|-----------|
|path|The path portion of the URL.|
|requestMethod|GET, POST, PUT, PATCH, DELETE.|
|contentType|The Content-Type header field.|
|urlParams|The parameters in the query string. This can also be evaluated to a String.|
|postParams|If this is a form post, this contains the post parameters.|

**Parent Topic:**[Encryption rule objects and APIs](api-overview.md)

## request - getAsJsonContent\(\)

Returns the request as an iterable object of type JsonNode.

This method is available only in an Edge Encryption rule if the request body is a valid JSON payload. If you are not sure what format the request body includes, check the contentType field on the request object.

Once the request is returned as a JsonNode object, you can use the [JSON APIs](json-overview.md) to iterate over the object and encrypt fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JsonNode|The request as an iterable JsonNode.|

## request - getAsXmlContent\(\)

Returns the request content as an iterable object of type XMLContent.

This method is available only in an Edge Encryption rule if the request body is a valid XML payload. If you are not sure what format the request body includes, check the contentType field on the request object.

Once the request is returned as an XMLContent object, you can use the [XML APIs](xml-overview.md) to iterate over the object and encrypt fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLContent|The request as an iterable object of type XMLContent.|

## request - XMLContains\(String path\)

Returns true if the given path exists in the XML DOM.

This method is available only if the request body is a valid XML payload. If you are not sure what format the request body includes, check the contentType field on the request object.

|Name|Type|Description|
|----|----|-----------|
|path|String|XPath statement you are searching for.|

|Type|Description|
|----|-----------|
|Boolean|Whether the given path exists in the XML DOM.|

