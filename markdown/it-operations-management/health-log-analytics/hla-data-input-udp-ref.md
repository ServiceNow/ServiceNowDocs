---
title: UDP data input configuration fields
description: Description of the fields on the UDP data input configuration form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# UDP data input configuration fields

Description of the fields on the UDP data input configuration form.

## Basic configuration

<table id="table_rrg_rp5_r5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

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

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr></tbody>
</table>The fields in the following table show read-only information.

<table id="table_orh_fq5_r5b"><thead><tr><th>

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

Protocol used to send the log data: UDP.

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

|Field|Description|Default value|
|-----|-----------|-------------|
|Default timezone|The default time zone of events. The system uses this default when the log does not specify a time zone.|GMT|
|Sub sample drop ratio|The ratio of events to drop.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Rate limit|Limitation on the number of events per second that the data input processes.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32,766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for selecting to discard logs if many processes are waiting in the queue to access the MID Server.|false|

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

