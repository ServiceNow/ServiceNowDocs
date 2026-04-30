---
title: REST API HTTP response codes
description: REST messages sent to an instance return a specific HTTP response code.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# REST API HTTP response codes

REST messages sent to an instance return a specific HTTP response code.

|Status Code|Message|Details|
|-----------|-------|-------|
|200|Success|Success with response body.|
|201|Created|Success with response body.|
|204|Success|Success with no response body.|
|400|Bad Request|The request URI does not match the APIs in the system, or the operation failed for unknown reasons. Invalid headers can also cause this error.|
|401|Unauthorized|The user is not authorized to use the API.|
|403|Forbidden|The requested operation is not permitted for the user. This error can also be caused by ACL failures, or business rule or data policy constraints.|
|404|Not found|The requested resource was not found. This can be caused by an ACL constraint or if the resource does not exist.|
|405|Method not allowed|The HTTP action is not allowed for the requested REST API, or it is not supported by any API.|
|406|Not acceptable|The endpoint does not support the response format specified in the request Accept header.|
|415|Unsupported media type|The endpoint does not support the format of the request body.|
|500|Internal server error|An unexpected error occurred while processing the request. The response contains additional information about the error.|
|502|Bad gateway|The server, while acting as a gateway or proxy, received an invalid response from the upstream server.|
|503|Service unavailable|The server is currently unable to handle the request.|

**Parent Topic:**[REST APIs](../concept/c_RESTAPI.md)

