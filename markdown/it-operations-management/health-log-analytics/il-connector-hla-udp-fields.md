---
title: UDP integration configuration fields
description: Description of the fields on the UDP integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [UDP, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# UDP integration configuration fields

Description of the fields on the UDP integration configuration forms for Health Log Analytics.

For the UDP integration setup procedure, see [Set up a UDP integration for Health Log Analytics](../task/il-connector-hla-udp.md).

<table id="table_ogz_c1d_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My UDP integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

MID server name

</td><td>

The MID Server to which the logs are streamed. This field is required.**Note:**

-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

</td></tr><tr><td>

Service instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. This field is required. The port must be within the range 6000-6200. Make sure that your organization’s security team opens the selected port on the MID Server.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance: UDP. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_q5k_5bd_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default timezone

</td><td>

The time zone of events that the system will use if a log does not specify the time zone.By default, the system uses GMT in such cases, but you can specify a different time zone.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of events to drop. The default value is -1.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of events to receive. The default value is -1.

</td></tr><tr><td>

Rate limit

</td><td>

Limitation on the number of events per second that the data input processes. The default value is -1.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages, in bytes. The default value is 32,766.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input. The default value is UTF-8. This field is read-only.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if many processes are waiting in the queue to access the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

