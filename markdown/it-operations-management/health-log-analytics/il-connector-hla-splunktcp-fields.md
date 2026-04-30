---
title: Splunk TCP integration configuration fields
description: Description of the fields on the Splunk TCP integration configuration forms for Health Log Analytics.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Splunk TCP, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Splunk TCP integration configuration fields

Description of the fields on the Splunk TCP integration configuration forms for Health Log Analytics.

For the Splunk TCP integration setup procedure, see [Set up a Splunk TCP integration for Health Log Analytics](../task/il-connector-hla-splunktcp.md).

<table id="table_rp3_c3g_q2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Splunk TCP integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID server name

</td><td>

MID Server to which log data from Splunk is pulled. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. This field is required.Make sure that your organization’s security team opens the selected port on the MID Server.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: TCP. This field is read-only.

</td></tr><tr><td>

Use Cooked Data

</td><td>

Option to ingest log data from Splunk in the preprocessed \("cooked"\) format that Splunk uses on the forwarder.Ingesting data into HLA in this format ensures that each log line retains the relevant contextual information that Splunk embeds into it.

</td></tr></tbody>
</table><table id="table_x5c_f3g_q2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use SSL/TLS

</td><td>

Option to use SSL/TLS, for enhanced data security and protection.**Note:** SSL/TLS must be enabled if you want to send logs in a compressed format.

</td></tr><tr><td>

Lookup hostnames

</td><td>

Option to perform DNS lookup to resolve IPs to hostnames. The default value is false.

</td></tr><tr><td>

Use Forwarder TimeZone

</td><td>

Option to pass information about the time zone in which the forwarder is located.The MID Server uses this information to adjust for the time zone from which the logs arrive.

This option is displayed when **Use Cooked Data** is selected. It is relevant when using Splunk Universal Forwarders.

</td></tr><tr><td>

Enable Compression

</td><td>

Option to send logs in compressed format.Sending logs in a compressed format minimizes the size of the data being transferred, which is important when dealing with large volumes of log data.

This option is displayed when **Use Cooked Data** and **Use SSL/TLS** are selected. It is relevant when using Splunk Universal Forwarders.

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

The time zone of events that the system will use if a log does not specify the time zone.By default, the system uses GMT in such cases, but you can specify a different time zone.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

