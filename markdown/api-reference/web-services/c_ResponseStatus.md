---
title: JSON response status
description: JSONv2 requests may return one of several response statuses.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JSONv2 web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# JSON response status

JSONv2 requests may return one of several response statuses.

## JSON Success Response

Each JSON success response includes a record array containing the records retrieved by the given action. Each JSON object contains one or more metadata elements, prefixed with \_\_, regarding the status for the action on each record, as illustrated in the previous examples. The JSON success responses use the following syntax:

\_\_status

```
"__status": "<value>"
```

where &lt;value&gt; is success or failure.

## JSON Failure Response

When the `_status` element returns failure, the `_error` element is added to identify the error and reason.

```
"__error": { "message": "<error value>", "reason": "<reason value> "}

```

where `<error value>` is the error message text and `<reason value>` is the reason the error was triggered.

The JSON error response contains only the error and reason elements. Generally, this indicates that the whole JSON operation failed and no records can be processed.

For example:

```
{"_error":"Cannot update with empty sysparm_query","reason":null}
```

**Parent Topic:**[JSONv2 web service](c_JSONv2WebService.md)

