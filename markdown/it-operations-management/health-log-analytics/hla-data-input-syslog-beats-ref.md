---
title: Rsyslog, Filebeat, or Winlogbeat data input configuration fields
description: Description of the fields on the Rsyslog, Filebeat, and Winlogbeat data input configuration forms.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Rsyslog, Filebeat, or Winlogbeat data input configuration fields

Description of the fields on the Rsyslog, Filebeat, and Winlogbeat data input configuration forms.

## Basic configuration

<table id="table_iky_4jq_j4b"><thead><tr><th>

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

-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

This field is required.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server.

 Choose a port within the suggested range from the array. The port must not be occupied by another process. Make sure that your organization’s security team opens the selected port.

This field is required.

</td></tr><tr><td>

Content pack

</td><td>

\(Linux using Filebeat only\) The content pack to use.Content packs contain default source types and mapping script templates. Health Log Analytics activates the selected pack automatically and uses its mapping script for mapping the data input sources. For more information, see [Health Log Analytics content packs for quicker time to value](../concept/hla-content-packs.md).

</td></tr></tbody>
</table><table id="table_eqc_zjq_j4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Path

</td><td>

The full path from which to stream logs. You can use a wildcard. This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr><tr><td>

Component

</td><td>

The device type or stack layer as context for the logs that is used for anomaly detection and correlation. For example: Tomcat.Components typically represent CIs in the CMDB. Several components are often clustered together in a single service instance.

</td></tr><tr><td>

Source Type

</td><td>

The source type, which defines how Health Log Analytics handles a specific application and parses the log data. For example: Tomcat Catalina.Each data input can have multiple source types, based on the diversity of its log formats. Service instances and components can have any number of source types.

</td></tr></tbody>
</table>## Advanced configuration

For Rsyslog data inputs:

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

For data inputs that use Beats agents:

|Field|Description|Default value|
|-----|-----------|-------------|
|Client inactivity timeout \(sec\)|The timeout, in seconds, to close an inactive channel.|15|
|Worker thread count|The number of threads that handle incoming data.|4|
|Default time zone|The default time zone of events. The system uses this default when the log does not specify a time zone.|GMT|
|Sub sample drop ratio|The ratio of events to drop.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for selecting to discard logs if there is a load on the MID Server.|false|

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

