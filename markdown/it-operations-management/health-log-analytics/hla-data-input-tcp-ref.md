---
title: TCP data input configuration fields
description: Description of the fields on the TCP data input configuration form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# TCP data input configuration fields

Description of the fields on the TCP data input configuration form.

## Basic configuration

<table id="table_pvw_fvf_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. Select a unique port from the array. The placeholder shows the range of ports from which to choose. Make sure that your organization’s security team opens the selected port.

This field is required.

</td></tr><tr><td>

MID

</td><td>

The MID Server to which the logs are streamed. **Note:**

-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, Create an service instance and add CIs to it. Set the status of the new service instance to Operational.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_fgz_cwf_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the data input.

</td></tr><tr><td>

Transport

</td><td>

Protocol used to send the log data.Rsyslog and Splunk send data using the TCP protocol.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Last log time

</td><td>

The time when the last log streamed in the data input.

</td></tr><tr><td>

Error message

</td><td>

The streaming error.This field is populated automatically. It displays only when a streaming error has occurred.

</td></tr></tbody>
</table>## Advanced configuration

<table id="table_sfw_2xx_vmb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Use SSL/TLS

</td><td>

Option to use SSL/TLS.

</td><td>

 

</td></tr><tr><td>

Look up hostnames

</td><td>

Option to perform DNS lookup to resolve IPs to hostnames.

</td><td>

false

</td></tr><tr><td>

Boss thread count

</td><td>

The number of threads that manage connections.

</td><td>

1

</td></tr><tr><td>

Worker thread count

</td><td>

The number of threads that handle incoming data.

</td><td>

4

</td></tr><tr><td>

Read timeout seconds

</td><td>

The timeout in seconds since the last read. When the timeout expires, the system closes the channel.

</td><td>

30

</td></tr><tr><td>

Default timezone

</td><td>

The default time zone of events. The system uses this default when the log does not specify a time zone.

</td><td>

GMT

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of events to drop.

</td><td>

-1

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of events to receive.

</td><td>

-1

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages in bytes.

</td><td>

32766

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input.

</td><td>

UTF-8

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td><td>

 

</td></tr><tr><td>

Line breaker delimiters

</td><td>

The line break character separating the raw log lines.Splitting values must be separated by a comma followed by a space: ", ". For example: "\\r, \\n, , splitHere, \#".

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration fields](../concept/hla-data-input-config-fields.md)

