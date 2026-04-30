---
title: Control request and response content type
description: Controls which content types are allowed in scripted REST API requests and responses.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Control request and response content type

Controls which content types are allowed in scripted REST API requests and responses.

By default, scripted REST APIs support `application/json`, `application/xml`, and `text/xml`. User-defined custom content types \(with `json` or `xml` subtypes\) are also supported. For example, `application/vnd.collection+json` and `application/vnd.adobe.xdp+xml` are treated as JSON and XML, respectively.

**Important:** If the request body format is not of a `json` or `xml` subtype, use only the request body `dataStream` field to access the request body. Using request body `data`, `dataString`, `nextEntry()`, or `hasNext()` with a non-json or non-xml format results in a `500` error response.

## Setting defaults

You can set default values for the API using the **Default supported request formats** and **Default supported response formats** fields. These fields define acceptable values users can pass in the Content-Type and Accept request headers, respectively. If a requesting user specifies an Accept or Content-Type header not supported by the API or resource, the instance responds with an HTTP error code of `406` or `415`.

You can override these values for each resource using the **Supported request formats** and **Supported response formats** on the Scripted REST Service form.

**Note:** The **Supported request formats** field appears only for PUT, POST, and PATCH resources.

## Using wildcard values

You can use wildcard values when specifying valid content types.

-   To perform a single-character wildcard search, use the percent sign \(%\) character. This wildcard finds words that contain any one character in place the percent-sign-character. For example, to find words such as text or test, search for: `te%t`.
-   To perform a multiple-character wildcard search, use the asterisk \(\*\) character. This wildcard finds words that contain zero or more characters in place of the asterisk-character. For example, to find words such as planned or placed, search for: `pl*d`.

## Using the x-www-form-urlencoded content type

If a REST API or resource accepts the `application/x-www-form-urlencoded` content-type, you can retrieve the urlencoded values provided in the request as a JSON map. You can then supply these urlencoded key-value pairs as query parameters, in the request body, or both. They are combined and stored in the request parameters. Access these parameters through the `request.queryParams` object.

For example, if your API is defined to accept the `application/x-www-form-urlencoded` content-type and your API is implemented as follows,

```
(function process(/*RESTAPIRequest*/ request, /*RESTAPIResponse*/ response) {

 response.setBody(request.queryParams);

})(request, response);
```

… then the following request yields the respective response:

```
POST to localhost:8080/api/now/some_api/some_resource?name3=value3&name4=value4
```

Body:

```
name1=value1&name2=value2
```

Response:

```
{ "result":
    { "name4": [ "value4" ], "name3": [ "value3" ], "name2": [ "value2" ],
      "name1": [ "value1" ]
    }
}
```

## Sending binary type in a response

When sending a binary type in a response, you must set the response content type and write the binary stream directly using a `RESTAPIResponseStream` object. You can access this object by calling `getStreamWriter()` on the response object. For more information, see.

**Parent Topic:**[Create a scripted REST API](../task/t_CreateAScriptedRESTService.md)

