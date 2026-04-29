---
title: Edge Delta TCP integration configuration fields
description: Description of the fields on the Edge Delta TCP integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Edge Delta, TCP, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Edge Delta TCP integration configuration fields

Description of the fields on the Edge Delta TCP integration configuration forms for Health Log Analytics.

For the Edge Delta TCP integration setup procedure, see [Set up an Edge Delta TCP integration for Health Log Analytics](../task/il-connector-hla-edgedelta-tcp.md).

<table id="table_avj_dqh_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Edge Delta TCP integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID server name

</td><td>

MID Server to which the Edge Delta logs are streamed. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server used for listening on logs. This field is required.Choose a port within the suggested range from the array. The port must not be occupied by another process. Ensure that your organization's security team opens the selected port.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: TCP. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_i3k_rqh_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lookup hostnames

</td><td>

Option to perform DNS lookup to resolve IPs to hostnames. The default value is false.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of logs to drop. The default value is -1: no logs are dropped.For example: If you want one out of every five logs to be dropped, change the value to 5.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of logs to receive. The default value is -1: no logs are received.For example: If you want one out of every five logs to be received, change the value to 5.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages in bytes. The default value is 32766.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input. Default is UTF-8.

</td></tr><tr><td>

Line breaker delimiters

</td><td>

The line break character separating the raw log lines.Splitting values must be separated by a comma followed by a space: ", ". For example: "\\r, \\n, , splitHere, \#".

</td></tr><tr><td>

Boss thread count

</td><td>

The number of threads that manage connections.

</td></tr><tr><td>

Worker thread count

</td><td>

The number of threads that handle incoming data.

</td></tr><tr><td>

Read timeout seconds

</td><td>

The timeout in seconds since the last read. When the timeout expires, the system closes the channel.

</td></tr><tr><td>

Default timezone

</td><td>

The time zone of events that the system uses if a log does not specify the time zone.By default, the system uses GMT, but you can specify a different time zone.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

