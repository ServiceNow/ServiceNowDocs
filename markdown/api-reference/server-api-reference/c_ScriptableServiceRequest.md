---
title: RESTAPIRequest - Scoped, Global
description: The RESTAPIRequest API provides methods that allow you to access scripted REST API request details in scripts.The body of the request.Returns the value of a specific header from the web service request.Get the content types specified in the request Accept header.All headers from the request.The path parameters passed in the request URI.The query parameters from the web service request.The entire query added to the endpoint URI.The request URI, excluding domain information.The entire request URL.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTAPIRequest - Scoped, Global

The RESTAPIRequest API provides methods that allow you to access scripted REST API request details in scripts.

This API runs in the `sn_ws` namespace.

**Note:** You cannot instantiate objects of this type. Objects of this type are created automatically and are accessible only in scripted REST API resource scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTAPIRequest - body

The body of the request.

|Name|Type|Description|
|----|----|-----------|
|body|[RESTAPIRequestBody](../../ScriptableServiceRequestBody/concept/c_ScriptableServiceRequestBody.md#)|The body of the request. You can access data from the body object using the RESTAPIRequestBody API.|

```
var requestBody = request.body // Returns instance of RESTAPIRequestBody
```

## RESTAPIRequest - getHeader\(String header\)

Returns the value of a specific header from the web service request.

|Name|Type|Description|
|----|----|-----------|
|header|String|The name of the header, such as **accept** or **content-type**.|

|Type|Description|
|----|-----------|
|String|The value of the specified header.|

```
var acceptHeader = request.getHeader('accept');
```

## RESTAPIRequest - getSupportedResponseContentTypes\(\)

Get the content types specified in the request Accept header.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of string values where each string is a content type, such as application/json.|

## RESTAPIRequest - headers

All headers from the request.

|Name|Type|Description|
|----|----|-----------|
|headers|object|All headers from the request, and their values.|

```
var headers = request.headers; 
var acceptHeader = headers.Accept;
var myCustomHeader = headers.myCustom; 
var specialHeader = headers['special - header'];
```

## RESTAPIRequest - pathParams

The path parameters passed in the request URI.

|Name|Type|Description|
|----|----|-----------|
|pathParams|Object|The path parameters as a script object. Available path parameters depend on the web service configuration.|

In this example, the scripted REST API endpoint follows this format: `https://instance.service-now.com/api/now/myservice/{tableName}/{id}`. The request being processed uses this URL: `https://instance.service-now.com/api/now/myservice/myApp_table/1234`.

```
var pathParams = request.pathParams; 
var tableName = pathParams.tableName; //'myApp_table' 
var id = pathParams.id; //'1234'
```

## RESTAPIRequest - queryParams

The query parameters from the web service request.

|Name|Type|Description|
|----|----|-----------|
|queryParams|Array|The query parameters from the web service request.|

In this example, the request being processed uses this URL: `https://<instance_rest_endpoint>?active=false&name=now`. Note the **active** and **name** parameters.

```
var queryParams = request.queryParams; 
var isActiveQuery = queryParams.active; // [false] 
var nameQueryVal = queryParams.name; // ['now']
```

## RESTAPIRequest - queryString

The entire query added to the endpoint URI.

|Name|Type|Description|
|----|----|-----------|
|queryString|String|The entire query for the request.|

In this example, the request being processed uses this URL: `https://<instance_rest_endpoint>?active=false&name=now`. Note the query `active=false&name=now`.

```
var query = request.queryString; //"active=false&name=now"
```

## RESTAPIRequest - uri

The request URI, excluding domain information.

|Name|Type|Description|
|----|----|-----------|
|uri|String|The request URI, excluding domain information.|

In this example, the request being processed uses this URL: `https://instance.service-now.com/api/now/table/myTable?active=false&name=now`.

```
var query = request.uri; //"api/now/table/myTable"
```

## RESTAPIRequest - url

The entire request URL.

|Name|Type|Description|
|----|----|-----------|
|url|String|The entire request URL.|

In this example, the request being processed uses this URL: `https://instance.service-now.com/api/now/table/myTable?active=false&name=now`.

```
var query = request.url; //"https://instance.service-now.com/api/now/table/myTable?active=false&name=now"
```

