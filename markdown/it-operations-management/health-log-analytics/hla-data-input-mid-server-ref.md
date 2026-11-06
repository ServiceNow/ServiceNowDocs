---
title: MID Server data input configuration fields
description: Description of the fields on the MID Server data input configuration form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/health-log-analytics/hla-data-input-mid-server-ref.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# MID Server data input configuration fields

Description of the fields on the MID Server data input configuration form.

|Field|Description|
|-----|-----------|
|Description|Optional description of the data input.|
|MID|The name of the MID Server from which the logs are streamed.|

<table id="table_cfn_3fb_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the data input. This field is read-only.

</td></tr><tr><td>

Transport

</td><td>

Protocol used to stream the log data. This field is read-only.This data input uses the MID Server to stream log data to your instance.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created. This field is read-only.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed. This field is read-only.

</td></tr><tr><td>

MID last receiving time

</td><td>

The time when the last log streamed in the data input.

</td></tr><tr><td>

Advanced

</td><td>

Option to display the **Advanced** tab for advanced configuration.

</td></tr></tbody>
</table>|Field|Description|Default value|
|-----|-----------|-------------|
|Default timezone|The default time zone used when a log doesn't include time zone information.|GMT|
|Sub sample drop ratio|The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.|-1|
|Sub sample receive ratio|The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32766|
|Character encoding|The character encoding for this data input. This field is read-only.|UTF-8|
|Drop if queue is full|Option to discard logs if many processes are waiting in the queue to access the MID Server.|Clear|

**Parent Topic:**[Data input configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/health-log-analytics/hla-data-input-config-fields.md)

