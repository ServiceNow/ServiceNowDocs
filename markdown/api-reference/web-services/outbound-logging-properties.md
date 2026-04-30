---
title: Outbound web service logging properties
description: These properties allow you to control the behavior of outbound web service request logging.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound web services: Logging, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Outbound web service logging properties

These properties allow you to control the behavior of outbound web service request logging.

<table id="table_kpp_tzr_lw"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.outbound\_http.db.log

</td><td>

By default, log information is written to a log file and to the instance database. Set this property to false to disable database logging.-   Type: true \| false
-   Default value: true
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.outbound\_http.text.content\_types

</td><td>

A comma-separated list of content types. The body of requests or responses with one of these content types is logged. By default, the content types text/\*, application/json, and application/xml are always logged. Use this property to add additional content types.-   Type: String
-   Default value: none
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.outbound\_http.content.max\_limit

</td><td>

The maximum number of characters logged from a request or response body. The first characters of the body, up to this limit, are logged. This property has a maximum possible value of 1000.-   Type: integer
-   Default value: 100
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.outbound\_http\_log.override

</td><td>

When this property is set to true, the property **glide.outbound\_http\_log.override.level** determines the log level for all requests and responses. This log level overrides any other log level settings. Only use this property for a limited time when troubleshooting.-   Type: true \| false
-   Default value: false
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.outbound\_http\_log.override.level

</td><td>

The log level to use for all requests and responses when **glide.outbound\_http\_log.override** is true. Valid values are `basic`, `elevated`, and `all`.-   Type: String
-   Default value: basic
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Outbound web services: Logging](../concept/outbound-request-logging.md)

