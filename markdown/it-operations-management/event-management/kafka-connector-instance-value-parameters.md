---
title: Kafka connector instance value parameters
description: The following table displays the Kafka connector instance value parameters that you can fill in, as needed, when creating a Kafka connector instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-10-13"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Kafka connector instance value parameters

The following table displays the Kafka connector instance value parameters that you can fill in, as needed, when creating a Kafka connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bootstrap\_servers

</td><td>

Set to **true** to enable debug logs.Default: false

</td></tr><tr><td>

consumer\_group\_name

</td><td>

Limits metric history retrieval to prevent system overload.Default: 180 minutes

</td></tr><tr><td>

topic

</td><td>

Adds a small time buffer to ensure no metrics are missed.Default: 5 minutes

</td></tr><tr><td>

Field\_mappings

</td><td>

Maps field names from Kafka message payload to internal field identifiers. For example: - "node": "host" → maps host in message to internal node field. - "value": "value" → maps metric value. - "timestamp": "ts" → maps timestamp field.

Default: "\{ "metric\_type": "metric\_name", "resource": "mountpoint", "node": "host", "value": "value", "timestamp": "ts"\}

</td></tr><tr><td>

logPayloadForDebug

</td><td>

Determines whether to print the raw log payload. Set to true only for debugging purposes, as printing the raw payload quickly fills up the MID Server logs. Default value: false

</td></tr><tr><td>

debug

</td><td>

Displays debug messages. Default value: false. Specify true to see debug messages.

</td></tr><tr><td>

max\_poll\_attempts

</td><td>

Number of times to attempt polling Kafka for messages before stopping.Default value: 10

</td></tr><tr><td>

max\_poll\_records

</td><td>

Maximum number of records fetched in a single poll. Default value: 5000

</td></tr><tr><td>

max\_poll\_retry

</td><td>

Number of times to retry polling if no records are returned consecutively. Default value: 2

</td></tr><tr><td>

poll\_timeout\_ms

</td><td>

Maximum time \(in milliseconds\) to wait during a poll operation before timing out. Default value: 60000

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

