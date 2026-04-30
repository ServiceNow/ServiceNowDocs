---
title: Configure outbound logging
description: You can configure outbound request logging to log basic, elevated, or all HTTP request and response information for specific domains.Certain elements are logged based on the configured log level.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Logging, Outbound, Web services, API implementation, API implementation and reference]
---

# Configure outbound logging

You can configure outbound request logging to log basic, elevated, or all HTTP request and response information for specific domains.

To configure the log level for a REST method or SOAP message function, navigate to the record you want to configure and click the **Set log level** related link, then select a log level for the current record.

To modify the log level for multiple outbound requests, navigate to **System Web Services** &gt; **HTTP Log Levels** and change the log levels using the list. All outbound requests that have been configured with a specific log level are listed.

You can override the log level for all outbound requests using the properties **glide.outbound\_http\_log.override** and **glide.outbound\_http\_log.override.level**. Use these properties only for a limited time when troubleshooting.

You can set the log level in a script using the setLogLevel\(\) function from the SOAPMessageV2 and RESTMessageV2 APIs. For more information about using these APIs, refer to the API documentation.

**Parent Topic:**[Outbound web services: Logging](outbound-request-logging.md)

**Related topics**  


[RESTMessageV2 - setLogLevel\(\)](../../../app-store/dev_portal/API_reference/RESTMessageV2/concept/c_RESTMessageV2API.md#)

[SOAPMessageV2 - setLogLevel\(\)](../../../app-store/dev_portal/API_reference/SOAPMessageV2/concept/c_SOAPMessageV2API.md#)

## Outbound request log levels

Certain elements are logged based on the configured log level.

### Logged elements

The following elements from the request and response are logged depending on the configured log level.

<table id="table_s23_xx5_hw"><thead><tr><th>

Field

</th><th>

Basic

</th><th>

Elevated

</th><th>

All

</th></tr></thead><tbody><tr><td>

Sequence

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

HTTP Method

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Protocol

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Scheme

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Hostname

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Path

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

HTTP response status

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Request length

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Response length

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Total call time

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

System ID

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Source table

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Source record ID**Note:** You must have read access for records in the specified **Source table** to view this field.

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Scope

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Session

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Transaction

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

User

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

MID server

</td><td>

x

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Request headers

</td><td>

 

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Request query

</td><td>

 

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Response headers

</td><td>

 

</td><td>

x

</td><td>

x

</td></tr><tr><td>

Request body

</td><td>

 

</td><td>

 

</td><td>

x

</td></tr><tr><td>

Response body

</td><td>

 

</td><td>

 

</td><td>

x

</td></tr></tbody>
</table>