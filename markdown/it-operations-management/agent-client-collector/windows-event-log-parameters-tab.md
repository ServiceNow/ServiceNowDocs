---
title: Windows event log filter parameters
description: The configurable values on the Check Parameters tab of the os.windows.check-event-log check.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Windows event log filter parameters

The configurable values on the Check Parameters tab of the os.windows.check-event-log check.

<table id="table_ylr_rzv_mxb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider\_name

</td><td>

String

</td><td>

Name of the provider that generated the event.**Note:** If you do not specify a **log\_file** value together with the **provider\_name**, the system searches all available log files, which increases the time it takes to receive results.

</td></tr><tr><td>

log\_file

</td><td>

String

</td><td>

The name of the Windows event log file from which you retrieve events. Possible values are:-   Application
-   System

**Note:** If you do not specify a **provider\_name** value together with the **log\_file**, the system searches all events from the log file, which increases the number of retrieved events.

</td></tr><tr><td>

id

</td><td>

Integer

</td><td>

The numerical id of the event. Possible values are 0-65535.

</td></tr><tr><td>

warning

</td><td>

Integer

</td><td>

Any value above the specified parameter generates a Warning event.

</td></tr><tr><td>

event\_level

</td><td>

String

</td><td>

The severity level of the event. Possible values:-   Critical
-   Error
-   Warning
-   Information
-   Verbose

</td></tr><tr><td>

regex\_pattern

</td><td>

String

</td><td>

The regex pattern to be used in searching the event logs.The value must be enclosed in double quotation marks. For example, "error".

</td></tr><tr><td>

duration\_hour

</td><td>

Integer

</td><td>

The time period for which you want to retrieve events from the Windows event log. Value is specified in hours; fractions of hours are specified with decimals.

</td></tr><tr><td>

critical

</td><td>

Integer

</td><td>

Any value equal to or above the specified parameter generates a Critical event.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](acc-monitoring-reference.md)

