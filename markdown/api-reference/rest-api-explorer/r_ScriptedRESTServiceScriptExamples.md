---
title: Scripted REST API example - script samples
description: These examples demonstrate how to create various resource scripts for a scripted REST API.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Scripted REST API examples, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Scripted REST API example - script samples

These examples demonstrate how to create various resource scripts for a scripted REST API.

## Query parameters GET example

This example demonstrates how to get query parameter values from a request.

```
/**
 * GET - Sample Request API - Query Params
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var uri = request.uri;
    var url = request.url;
    var queryParams = request.queryParams;
    var customHeader = request.getHeader('X-Custom');

    return {
        "uri": uri,
        "url": url,
        "queryParams": queryParams,
        "customHeader": customHeader
    };

})(request, response);
```

## Path parameters GET example

This example demonstrates how to get path parameter values from a request.

```
/**
 * GET - Sample Request API - Path Params
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var uri = request.uri;
    var url = request.url;
    var path = request.pathParams;

    return {
        "uri": uri,
        "url": url,
        "path_params": path,
        "path.id": path.id
    };
})(request, response);

```

## Script include GET example

This example demonstrates how to use a script include to provide a response. By using a script include you can reuse common code and maintain readability in the REST service scripts.

```
/**
 * GET - Sample Request API - Script Include
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var responseObj = global.SampleDataUtil.getSampleJSON();
    return responseObj;
})(request, response);
```

## String POST example

This example demonstrates how to parse a POST message with a string body and send a response based on the request.

```
/**
 *  POST - Sample Request API - dataString
 *  sample usage:
 *  var requestBody = request.body;
 *  var requestString = requestBody.dataString;
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var requestBody = request.body;
    var requestString = requestBody.dataString;
    return {"requestString": requestString};
})(request, response);
```

## Binary POST example

This example demonstrates how to parse a POST message with a binary body and send a response based on the request.

```
/**
 * POST - Sample Request API - Body
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var body = request.body.data;
    //do any additional processing on the request body, such as inserting a new record.
    return {
        "body.id": body.id
    };
})(request, response);
```

## Not acceptable error example

This example demonstrates how to respond with a not acceptable error. Use this error type when the request Accept header value is not supported by the web service.

```
/**
 * Sample Not Acceptable Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    response.setError(new sn_ws_err.NotAcceptableError('sample error message'));
})(request, response);
```

## Bad request error example

This example demonstrates how to respond with a bad request error. Use this error type to indicate a mistake in the request syntax.

```
/**
 * Bad Request Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    response.setError(new sn_ws_err.BadRequestError('sample error message'));
})(request, response);
```

## Conflict error example

This example demonstrates how to respond with a conflict error. Use this error type in the event of multiple conflicting requests, such as multiple updates to the same record.

```
/**
 * Error Response: Conflict Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    response.setError(new sn_ws_err.ConflictError('sample error message'));
})(request, response);
```

## Not found error example

This example demonstrates how to respond with a not found error. Use this error type if the requested resource does not exist or is unavailable.

```
/**
 * Error Response: Not Found Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    response.setError(new sn_ws_err.NotFoundError('sample error message'));
})(request, response);
```

## Unsupported media type error example

This example demonstrates how to respond with an unsupported media type error. Use this error type to indicate that the Content-Type of the request is unsupported.

```
/**
 * Error Response: Unsupported Media Type Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    response.setError(new sn_ws_err.UnsupportedMediaTypeError('sample error message'));
})(request, response);
```

## Service error example

This example demonstrates how to respond with a generic service error. The ServiceError object allows you to define the status code, message, and error detail. Use a ServiceError if the predefined error types do not meet your needs.

```
/**
 * Error Response: Custom Error Sample
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var myError = new sn_ws_err.ServiceError();
    myError.setStatus(418);
    myError.setMessage("I am a Teapot");
    myError.setDetail("Here are the details about this error");
    response.setError(myError);
})(request, response);

```

## Scripted REST resource script example

This sample REST API resource script parses the **name** and **id** values from the request body and returns those values in the response.

```
/**
 * POST - Sample Request API - Body
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
var body = request.body.data,
id0,name0,id1,name1;
name0 = body[0].name; // 'user0'
id0 = body[0].id; // '1234'
name1 = body[1].name; // 'user1'
id1 = body[1].id; // '5678'

return {
"id": id0,
"name": name0,
"id1": id1,
"name1": name1
};
})(request, response);
```

## Requests

The API can accept both XML and JSON requests.

<table id="table_xkb_2vq_xs"><thead><tr><th>

JSON Request

</th><th>

XML Request

</th></tr></thead><tbody><tr><td>

```
POST /api/sn_demo_api/v1/example/body HTTP/1.1
Content-Type: application/json
Accept: application/json
Host: <instance>.service-now.com
Connection: close
Content-Length: 91

[   
  { "name": "user0",
    "id": 1234
  },
  {
    "name": "user1",
    "id": 5678
  }
]
```

</td><td>

```
POST /api/sn_demo_api/v1/example/body HTTP/1.1
Content-Type: application/xml
Accept: application/json
Host: <instance>.service-now.com
Connection: close
Content-Length: 152

<request><entry>
      <name>user0</name>
      <id>1234</id>
   </entry>
   <entry>
      <name>user1</name>
      <id>5678</id>
   </entry>
</request>
```

</td></tr></tbody>
</table>## Responses

Both requests specify application/json as the Accept header value. This causes either response to use JSON formatting, even if the request content type is XML.

```
HTTP/1.1 200 OK
Content-Type: application/json;charset=UTF-8
Transfer-Encoding: chunked
Date: Tue, 04 Aug 2015 15:20:44 GMT
Server: ServiceNow
Connection: close
Set-Cookie: BIGipServerpool_<Instance>=880838154.47166.0000; path=/

{"result":{"id":1234,"id1":5678,"name":"user0","name1":"user1"}}
```

**Parent Topic:**[Scripted REST API examples](../concept/c_ScriptedRESTAPIExamples.md)

