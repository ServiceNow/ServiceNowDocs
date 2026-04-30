---
title: ServiceNow System Logs Retriever data input configuration fields
description: Description of the fields on the ServiceNow System Logs Retriever data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# ServiceNow System Logs Retriever data input configuration fields

Description of the fields on the ServiceNow System Logs Retriever data input configuration form.

<table id="table_fjt_vky_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. The default value is ServiceNow Glide Sys Log. This field is required.**Note:** Health Log Analytics comes with the source type glide\_sys\_log for log traffic from the ServiceNow Glide Sys Log service instance.

</td></tr><tr><td>

From

</td><td>

From date and time for reading the data. The data input doesn’t read data older than this date and time. This field is required.

</td></tr><tr><td>

Status

</td><td>

Status of the data input.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Syslog table filter

</td><td>

The criteria used to filter log data from the System Log table before streaming it to the AI engine.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

