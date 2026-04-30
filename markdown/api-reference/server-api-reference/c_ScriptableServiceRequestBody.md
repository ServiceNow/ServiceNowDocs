---
title: RESTAPIRequestBody - Scoped, Global
description: The RESTAPIRequestBody API provides methods that allow you to access the body content of a scripted REST API request in scripts.The content of the request body.The content of the request body, as a stream.The content of the request body, as a String.Determines if there are additional entries in the request body.Retrieve one entry from the request body as a script object.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTAPIRequestBody - Scoped, Global

The RESTAPIRequestBody API provides methods that allow you to access the body content of a scripted REST API request in scripts.

The format of a RESTAPIRequestBody object may be JSON or XML, depending on the content-type header value from the request.

**Note:** You cannot instantiate objects of this type. Objects of this type are created automatically and are accessible only in scripted REST API resource scripts.

This API runs in the `sn_ws` namespace.

Single entry example-request-body in JSON format.

```
{
 "name": "user1",
 "id": 1234,
 "roles": [
  {
   "name": "admin"
  },
  {
   "name": "itil"
  }
 ]
}
```

Multiple entry example-request-body in JSON format.

```
[{
 "name": "user1",
 "id": 1234,
 "roles": [
  {
   "name": "admin"
  },
  {
   "name": "itil"
  }
 ]
},{
 "name": "user2",
 "id":9876,
 "roles": [
  {
   "name":"admin"
  }
 ]
}]
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTAPIRequestBody - data

The content of the request body.

**Note:** REST web services consume data, datastream, and dataString via stream. Because streams are only consumed once, only one can be called. For example, if calling both data and dataString, the second call will return empty.

|Name|Type|Description|
|----|----|-----------|
|data|Object or Array|The request content. This can be a single object or an array of objects depending on the request.|

```
var entry;
var id;
var requestBody = request.body;
var requestData = requestBody.data; //May be an array or a single object
if (requestData instanceof Array) { 
 entry = requestData[0].name; // 'user1'
 id = requestData[0].id; // '1234'
} else {
 entry = requestData.name; // 'user1'
 id = requestData.id; // '1234'
}
```

## RESTAPIRequestBody - dataStream

The content of the request body, as a stream.

**Note:** REST web services consume data, datastream, and dataString via stream. Because streams are only consumed once, only one can be called. For example, if calling both data and dataString, the second call will return empty.

|Name|Type|Description|
|----|----|-----------|
|dataStream|Object|The content of the request body. You can pass the stream to a separate API, such as to create an attachment from the request or forward the request to a different endpoint.|

```
var requestBody = request.body; 
var requestStream = requestBody.dataStream;
```

## RESTAPIRequestBody - dataString

The content of the request body, as a String.

**Note:** REST web services consume data, datastream, and dataString via stream. Because streams are only consumed once, only one can be called. For example, if calling both data and dataString, the second call will return empty.

|Name|Type|Description|
|----|----|-----------|
|dataString|String|The content of the request body.|

```
var requestBody = request.body; 
var requestString = requestBody.dataString;
```

## RESTAPIRequestBody - hasNext\(\)

Determines if there are additional entries in the request body.

Use this method with the nextEntry\(\) method to iterate over multiple request body entries.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_a5m_my1_sr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

boolean

</td><td>

Flag indicating whether there are additional entries in the request body.Possible values:

-   true: Additional entries are available. As nextEntry\(\) is called, hasNext\(\) continues to be true until the last matching record is loaded.
-   false: No additional entries.

</td></tr></tbody>
</table>```
var requestBody = request.body;
requestBody.hasNext(); // returns true if the request contains a single entry or multiple entries
requestBody. nextEntry(); // returns next available entry

//calling second time
requestBody.hasNext(); // returns false if the request contains a single entry, or true if the request contains multiple entries
```

## RESTAPIRequestBody - nextEntry\(\)

Retrieve one entry from the request body as a script object.

Use this method with the hasNext\(\) method to iterate over multiple request body entries.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A single entry from the request body.|

```
var requestBody = request.body;
var requestEntry = requestBody.nextEntry(); // returns available entry if there is only one entry, or the first entry if there are multiple.
var name = requestEntry.name; // 'user1'

// Calling second time
requestEntry = requestBody.nextEntry(); // returns undefined if there is only one entry, or the second entry if there are multiple.
```

This example demonstrates using hasNext\(\) with nextEntry\(\).

```
var requestBody = request.body;
while(requestBody.hasNext()){
var entry = requestBody.nextEntry();
}
```

