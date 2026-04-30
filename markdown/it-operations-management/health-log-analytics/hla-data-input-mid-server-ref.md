---
title: MID Server data input configuration fields
description: Description of the fields on the MID Server data input configuration form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# MID Server data input configuration fields

Description of the fields on the MID Server data input configuration form.

## Basic configuration

<table id="table_d14_4fb_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

MID

</td><td>

The MID Server from which the logs are streamed.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. **Note:** This field is only available for MID Server data inputs created in the May 2025 store release or later releases.

This field is required. By default, it is set to ServiceNow MID Server.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_cfn_3fb_pvb"><thead><tr><th>

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

Protocol used to stream the log data.This data input uses the MID Server to stream log data to your instance.

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

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Default timezone|The default time zone of events. The system uses this default when the log does not specify a timezone.|GMT|
|Sub sample drop ratio|The ratio of events to discard.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for discarding logs if there is a load on the MID Server.| |

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

