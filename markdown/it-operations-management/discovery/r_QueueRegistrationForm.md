---
title: Queue Registration form reference
description: The Queue Registration form displays the fields available when creating or modifying a queue.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Queue Registration form reference

The Queue Registration form displays the fields available when creating or modifying a queue.

<table id="table_ygy_4g4_gfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queue

</td><td>

Name of the queue.

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Automatic Job Scheduling

</td><td>

Option to enable automatic job scheduling. When selected, the queue switches to automatic job scheduling and the system handles all job configurations.

</td></tr><tr><td>

Event Processing Order

</td><td>

Method used to process events. Options include:-   Parallel: Process multiple events simultaneously.
-   Sequential: Process only one event at a time. The events are interdependent and can only process after the previous event completes.

**Note:** After you configure the processing order and submit the queue, it can't be edited. Instead, you must delete the queue and create another queue.

</td></tr><tr><td>

Job configuration type

</td><td>

Type of job configuration. Options include:-   Constant number: Creates the required number of jobs.
-   Scale with node: Creates multiple jobs based on the number of nodes. Select this option if you don't know the number of available nodes.

**Note:** This field is automatically set to Constant number when the Event Processing Order field is set to Sequential.

</td></tr><tr><td>

Scale factor

</td><td>

Total number of jobs, which is calculated based on the value of the **Job configuration type** field.

</td></tr><tr><td>

Poll interval

</td><td>

How frequently jobs should poll and process events in this queue.

</td></tr><tr><td>

Description

</td><td>

Description of the queue.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery reference](discovery-references.md)

