---
title: Vector Agent data input configuration fields
description: Description of the fields on the Vector Agent data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Vector Agent data input configuration fields

Description of the fields on the Vector Agent data input configuration form.

<table id="table_rnn_bmp_12c"><thead><tr><th>

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

The MID Server to which the Vector Agent logs are streamed. This field is required.**Note:** If the MID Server is down or the connection is lost, the Vector pipeline may get blocked.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server used for listening to logs. This field is required.Choose a port within the range of 6000-6200.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance.Currently, only TCP is available.

</td></tr><tr><td>

Status

</td><td>

Status of the data input.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

