---
title: TCP integration configuration fields
description: Description of the fields on the TCP integration configuration forms for Health Log Analytics.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [TCP, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# TCP integration configuration fields

Description of the fields on the TCP integration configuration forms for Health Log Analytics.

For the TCP integration setup procedure, see [Set up a TCP integration for Health Log Analytics](../task/il-connector-hla-tcp.md).

<table id="table_sfp_25d_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My TCP integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID server name

</td><td>

The MID Server to which the logs are streamed. This field is required.-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. This field is required.Select a unique port from the array. The placeholder shows the range of ports from which to choose. Make sure that your organization’s security team opens the selected port.

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
</table><table id="table_kfx_jyd_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use SSL/TLS

</td><td>

Option to use SSL/TLS.

</td></tr><tr><td>

Lookup hostnames

</td><td>

Option to perform DNS lookup to resolve IPs to hostnames.

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

The time zone of events that the system will use if a log does not specify the time zone.By default, the system uses GMT in such cases, but you can specify a different time zone.

</td></tr><tr><td>

Default timezone

</td><td>

The default time zone of events. The system uses this default when the log does not specify a time zone.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of events to drop.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of events to receive.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages in bytes.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td></tr><tr><td>

Line breaker delimiters

</td><td>

The line break character separating the raw log lines.Splitting values must be separated by a comma followed by a space: ", ". For example: "\\r, \\n, , splitHere, \#".

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

