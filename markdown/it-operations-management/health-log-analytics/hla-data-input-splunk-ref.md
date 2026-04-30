---
title: Splunk data input configuration fields
description: Description of the fields on the Splunk data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Splunk data input configuration fields

Description of the fields on the Splunk data input configuration form.

## Basic configuration

<table id="table_a2d_jh4_nnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data input name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

MID Server

</td><td>

The MID Server to which the logs stream.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

This field is required.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. Make sure that your organization’s security team opens the selected port in the MID Server.

This field is required.

</td></tr><tr><td>

Transport Protocol

</td><td>

The protocol used for streaming log messages to your ServiceNow instance.-   TCP - When using the Transmission Control Protocol \(TCP\) protocol, all logs will reach the instance. However, the Splunk pipeline might be blocked if the MID Server is down or the connection to it is lost. TCP is the default transport protocol.
-   UDP - When using the User Datagram Protocol \(UDP\) protocol, the Splunk pipeline will never be blocked. However, some logs might be dropped before they reach the instance.

 For more information about streaming log data using the TCP or UCP transport protocol, see the [Streaming Splunk data using Heavy Forwarder: Selecting TCP or UDP \[KB0998928\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998928) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Use Cooked Data

</td><td>

Option to ingest log data from Splunk in the preprocessed \("cooked"\) format that Splunk uses on the forwarder.Ingesting data into HLA in this format ensures that each log line retains the relevant contextual information that Splunk embeds into it.

**Note:** If you select this option, there is no need to edit the `props.conf` and `transforms.conf` files during Splunk data input configuration.

</td></tr><tr><td>

Use Forwarder TimeZone

</td><td>

Option to pass information about the time zone in which the forwarder is located.The MID Server uses this information to adjust for the time zone from which the logs arrive. This option is relevant when using Splunk Universal Forwarders.

</td></tr><tr><td>

Enable Compression

</td><td>

Option to send logs in compressed format.Sending logs in a compressed format minimizes the size of the data being transferred, which is important when dealing with large volumes of log data. This option is relevant when using Splunk Universal Forwarders and can only be used when SSL/TLS is enabled.

</td></tr></tbody>
</table>## Advanced configuration

<table id="table_y31_w2p_pvb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default values

</th></tr></thead><tbody><tr><td>

Use SSL/TLS

</td><td>

Option for selecting to use SSL/TLS.**Note:** To send logs in a compressed format, SSL/TLS must be enabled.

</td><td>

 

</td></tr><tr><td>

Look up hostnames

</td><td>

Option for selecting to perform DNS lookup to resolve IPs to hostnames.

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

Option for selecting to discard logs if there is a load on the MID Server.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

