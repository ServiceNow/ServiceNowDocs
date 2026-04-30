---
title: Log viewer table fields
description: This section describes the information displayed in the Log viewer table.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-26"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Log viewer table fields

This section describes the information displayed in the **Log viewer** table.

<table id="table_iwb_y13_2qb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time

</td><td>

Timestamp of the log line in the format that the source uses. If no value appears, then check the source type structure of the raw data.

</td></tr><tr><td>

Service instance

</td><td>

Service instance in which the metric was found.

</td></tr><tr><td>

Component

</td><td>

Logical component of the service instance that generated the event. Multiple CIs can sometimes perform the same function.

</td></tr><tr><td>

Message

</td><td>

Inner message of the raw log line that contains the text of the system-generated log message regarding the nature of the occurrence.

</td></tr><tr><td>

Level

</td><td>

Type of event. The available values, in order of importance, are:-   **Emergency**
-   **Alert**
-   **Critical**
-   **Error**
-   **Warning**
-   **Notice**
-   **Informational**
-   **Debug**

</td></tr><tr><td>

Host

</td><td>

Host identifier from the log line that consists of the hostname or IP address of the endpoint.

</td></tr><tr><td>

Log message

</td><td>

The raw log message without the header.

</td></tr></tbody>
</table>**Note:** By default, the Raw message column does not appear in the Log viewer table. You can display this column by selecting it from the **Filters** pane. For more information, see [Customize the Log viewer table](../task/hla-op-log-viewer-table-sow.md).

**Parent Topic:**[Health Log Analytics reference](../../health-log-analytics-admin/concept/hla-reference.md)

