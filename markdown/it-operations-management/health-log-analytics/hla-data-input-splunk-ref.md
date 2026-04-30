---
title: Splunk data input configuration fields
description: Description of the fields on the Splunk data input configuration form.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure data inputs \(Splunk\), Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
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

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default values|
|-----|-----------|--------------|
|Use SSL/TLS|Option for selecting to use SSL/TLS.| |
|Look up hostnames|Option for selecting to perform DNS lookup to resolve IPs to hostnames.|false|
|Boss thread count|The number of threads that manage connections.|1|
|Worker thread count|The number of threads that handle incoming data.|4|
|Read timeout seconds|The timeout in seconds since the last read. When the timeout expires, the system closes the channel.|30|
|Default timezone|The default time zone of events. The system uses this default when the log does not specify a time zone.|GMT|
|Sub sample drop ratio|The ratio of events to drop.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Max length in bytes|The maximum length of log messages in bytes.|32766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for selecting to discard logs if there is a load on the MID Server.| |

**Parent Topic:**[Configure data inputs \(Splunk\)](../task/hla-data-input-splunk.md)

