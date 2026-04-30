---
title: ACC data input configuration fields
description: Description of the fields on the ACC data input configuration form.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure ACC data inputs manually, Set up additional ACC data inputs, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# ACC data input configuration fields

Description of the fields on the ACC data input configuration form.

<table id="table_oc5_dqg_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MID

</td><td>

The MID Server to which the logs stream.**Note:**

-   Only one ACC data input can be defined per MID Server. You can select only MID Servers with AgentClientCollector capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties. However, when 10 data inputs that are not ACC data inputs have been defined for a MID Server, one ACC data input can still be defined for it, making a total of 11 data inputs defined for that MID Server.
-   When you submit the form, this field becomes read-only.

This field is required.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server.

 The port must be configured and active. It must not be occupied by another process. Make sure that your organization’s security team opens the port before you assign it.

 **Note:** When you update the port, the system updates the Agent Client Collector with the new port configuration. Log streaming continues seamlessly without log loss after 1-3 minutes.

This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr></tbody>
</table>The fields in the following table show read-only information.

<table id="table_vvd_xqg_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the data input: Agent Log Analytics.**Note:** All ACC data inputs have the same name. You can identify an ACC data input by the name of the MID Server that is defined for it.

</td></tr><tr><td>

Status

</td><td>

The status of the data input.

</td></tr><tr><td>

Transport

</td><td>

The protocol used to send the log data.The ACC data input sends data using a ServiceNow Agent.

</td></tr><tr><td>

Sources count

</td><td>

The total number of log sources originating from all ACC data inputs together.

 This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

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
</table>|Field|Description|Default value|
|-----|-----------|-------------|
|Look up hostnames|Option for selecting to perform DNS lookup to resolve IPs to hostnames.|false|
|Use SSL|Option for selecting to use SSL.|true|
|Client inactivity timeout \(sec\)|The timeout, in seconds, to close an inactive channel.|15|
|Worker thread count|The number of threads that handle incoming data.|4|
|Default time zone|The default time zone of events. The system uses this default when the log does not specify a time zone.|GMT|
|Sub sample drop ratio|The ratio of events to drop.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32,766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for selecting to discard logs if many processes are waiting in the queue to access the MID Server.|false|

