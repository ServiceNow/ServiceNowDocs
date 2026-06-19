---
title: ACC Log Analytics \(ACC-L\) integration configuration fields
description: Description of the fields on the ACC Log Analytics \(ACC-L\) integration configuration forms for Health Log Analytics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/il-connector-hla-accl-fields.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ACC, Agent Client Collector, Log Analytics, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# ACC Log Analytics \(ACC-L\) integration configuration fields

Description of the fields on the ACC Log Analytics \(ACC-L\) integration configuration forms for Health Log Analytics.

For the ACC Log Analytics \(ACC-L\) integration setup procedure, see [Set up an ACC Log Analytics integration for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-accl.md).

<table id="table_l3c_pxl_whc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transport

</td><td>

The protocol used to send the log data. This field is read-only.The ACC-L integration uses a ServiceNow Agent to send data.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server to which the ACC-L agent connects. This field is required.**Important:** This port can't be the same as the MID Web Server port.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr><tr><td colspan="2">

ACC Listener

</td></tr><tr><td>

MID Server

</td><td>

The MID Server to which the logs stream. This field is required.**Note:**

-   Only one ACC-L integration can be defined per MID Server.

You can only select MID Servers with AgentClientCollector capability that support basic authentication. MID Servers that support mTLS are not listed.

-   The default maximum number of data inputs streaming logs to a single MID Server is 10.

You can modify this number in the MID Server properties. Exception: if 10 non-ACC-L integrations are already defined for a MID Server, you can still add one ACC-L integration, for a total of 11.

-   When you submit the form, this field is set to read-only.
-   **Important:** The configured MID Server can't be changed after the integration is activated.


</td></tr><tr><td>

MID Web Server port

</td><td>

Port used by the MID Server to receive data from ACC agents. This field is auto-populated and read-only when a MID Server has been configured. **Note:** The MID Web Server port must be reachable through your firewall.

</td></tr></tbody>
</table><table id="table_gxc_sxl_whc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lookup hostnames

</td><td>

Option to perform DNS lookup to resolve IPs to hostnames.

</td></tr><tr><td>

Use SSL

</td><td>

Option to use SSL.

</td></tr><tr><td>

Client inactivity timeout \(seconds\)

</td><td>

The timeout, in seconds, to close an inactive channel.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of logs to drop. The default value is -1: no logs are dropped.For example: If you want one out of every five logs to be dropped, change the value to 5.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages, in bytes.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this integration: UTF-8. This field is read-only.

</td></tr><tr><td>

Worker thread count

</td><td>

The number of threads that handle incoming data.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of logs to receive. The default value is -1: no logs are received.For example: If you want one out of every five logs to be received, change the value to 5.

</td></tr><tr><td>

Default timezone

</td><td>

The default time zone of events. The system uses this default when the log does not specify a time zone.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if many processes are waiting in the queue to access the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

