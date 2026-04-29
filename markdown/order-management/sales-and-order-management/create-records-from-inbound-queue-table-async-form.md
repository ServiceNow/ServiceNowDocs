---
title: Create records from inbound queue table async form
description: The Create records from inbound queue table async scheduled job form enables you to configure a scheduled job for asynchronous order processing.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Order Management reference, Reference, Sales and Order Management]
---

# Create records from inbound queue table async form

The Create records from inbound queue table async scheduled job form enables you to configure a scheduled job for asynchronous order processing.

<table id="table_cr2_nzr_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scheduled job.

</td></tr><tr><td>

Next action

</td><td>

Timestamp of the next job action.

</td></tr><tr><td>

Calendar

</td><td>

Time window during which the scheduled job can run. The calendar restricts job execution to a defined schedule, such as business hours. If an order is submitted outside the active window, the job will not process it until the next scheduled period.

</td></tr><tr><td>

Job ID

</td><td>

This value must be set to RunScriptJob.

</td></tr><tr><td>

State

</td><td>

State of the scheduler job. The available options are:-   Error
-   Paused
-   Permanent error
-   Queued
-   Ready
-   Running

</td></tr><tr><td>

System ID

</td><td>

Active nodes of the ServiceNow instance.

</td></tr><tr><td>

Job context

</td><td>

Context of the scheduled job.

</td></tr><tr><td>

Trigger type

</td><td>

Determines when and how often the scheduled job runs. The selected trigger type controls the additional scheduling fields that appear on the form. The available options are:-   None
-   Daily
-   Day and Month in Year
-   Day in Month
-   Day in Week in Month in Year
-   Days in Week
-   Disabled
-   Interval
-   Repeat
-   Run at System Startup
-   Run Once
-   Week in Month
-   Business Calendar: Entry Start
-   Business Calendar: Entry End

</td></tr><tr><td>

Repeat

</td><td>

Details of the time interval.

</td></tr><tr><td>

Time zone

</td><td>

Time zone in which you're operating your business.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)

**Related topics**  


[Configure a scheduled job for asynchronous order creation](../task/running-scheduled-job.md)

