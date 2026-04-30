---
title: Scripted REST API example - streaming file attachments
description: This example demonstrates how to send an image attachment to a requesting user as a binary stream.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Examples, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Scripted REST API example - streaming file attachments

This example demonstrates how to send an image attachment to a requesting user as a binary stream.

```
/**
 *  Sample Scripted REST Resource that returns a stream of binary representing an attachment
 *  This sample uses ServiceNow JavaScript API GlideSysAttachmentInputStream to get an attachment as a stream then
 *  users WriteStream to stream the response.
 */
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {
    var hdrs = {},
        attachment_sys_id = '1852fd52471321009db4b5b08b9a71a9';

    hdrs['Content-Type'] = 'image/jpeg';
    response.setStatus(200);
    response.setHeaders(hdrs);

    var writer = response.getStreamWriter();
    var attachmentStream = new GlideSysAttachmentInputStream(attachment_sys_id);
    writer.writeStream(attachmentStream);
})(request, response);
```

A request to this resource returns the following response.

```
//  sample response
/*
 HTTP/1.1 200 OK
 Set-Cookie: glide_session_store=SYSTEM; Expires=Fri, 30-Oct-2015 21:57:00 GMT; Path=/; HttpOnly
 Content-Type: image/jpeg
 Transfer-Encoding: chunked
 Date: Fri, 30 Oct 2015 21:26:59 GMT
 Connection: close
 Server: ServiceNow

 <binary response body excluded from this sample>
 */
```

**Parent Topic:**[Scripted REST API examples](../concept/c_ScriptedRESTAPIExamples.md)

