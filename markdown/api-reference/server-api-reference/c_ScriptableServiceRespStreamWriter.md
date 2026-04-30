---
title: RESTAPIResponseStream - Scoped, Global
description: The RESTAPIResponseStream API provides methods that allow you to write directly to the scripted REST API response stream.Write an input stream to the response stream.Write string data to the response stream.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTAPIResponseStream - Scoped, Global

The RESTAPIResponseStream API provides methods that allow you to write directly to the scripted REST API response stream.

Use RESTAPIResponseStream methods to build web service APIs in the [Scripted REST API](../../../../../integrate/custom-web-services/concept/c_CustomWebServices.md) feature.

This API runs in the `sn_ws` namespace.

**Note:** You cannot instantiate objects of this type. Objects of this type are created automatically and are accessible only in scripted REST API resource scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTAPIResponseStream - writeStream\(Object stream\)

Write an input stream to the response stream.

You must set the content type and status code before calling the writeStream\(\) method or the response will fail. You cannot modify these values after calling the writeStream\(\) method.

**Note:**

It is the responsibility of the script author to obtain the stream from a third-party service.

|Name|Type|Description|
|----|----|-----------|
|stream|Object|An attachment or a response stream from a third-party service.|

|Type|Description|
|----|-----------|
|void| |

The following example is for scoped applications:

```
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {

    response.setContentType('application/json');
    response.setStatus(200);

    var gsa = new GlideSysAttachment();
    var attachmentStream = new gsa.getContentStream(<sys_id of attachment>); 
    var writer = response.getStreamWriter();
    writer.writeStream(attachmentStream);

})(request, response);
```

The following example is for global applications:

```
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {

    response.setContentType('application/json');
    response.setStatus(200);

    var attachmentStream = new GlideSysAttachmentInputStream(<sys_id of attachment>);
    var writer = response.getStreamWriter();
    writer.writeStream(attachmentStream);

})(request, response);
```

## RESTAPIResponseStream - writeString\(String data\)

Write string data to the response stream.

You must set the content type and status code before calling the writeString\(\) method or the response will fail. You cannot modify these values after calling the writeString\(\) method.

|Name|Type|Description|
|----|----|-----------|
|data|String|The string to add to the response data.|

|Type|Description|
|----|-----------|
|void| |

```
response.setContentType('application/json');
response.setStatus(200);
var writer = response.getStreamWriter();
var body ={
  name:user1,
  id: 1234,
  roles: [
    {
      name: admin
    },
    {
      name: itil
    }
  ]
}
writer.writeString("{'name':'user','id':'1234'}");
writer.writeString(JSON.stringify(body));
```

