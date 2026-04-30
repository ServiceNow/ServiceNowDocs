---
title: Create Event workflow activity
description: The Create Event activity adds an event to the event queue, but does not immediately fire the event.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow notification activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create Event workflow activity

The **Create Event** activity adds an event to the event queue, but does not immediately fire the event.

The event processor typically processes the event within one minute. This activity triggers any business rules or email notifications that would normally be triggered by the event.

For more information about creating and using system events, see [System Events](https://www.servicenow.com/docs/access?context=events&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Results

**Finished:** the activity added the event to the event queue.

## Input variables

<table id="table_p1n_n4l_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event name

</td><td>

The name of the event to create. From the Event Name lookup list, select the event to add to the queue. If the event requires parameters, specify them in the Parameter script field.

</td></tr><tr><td>

Parameter 1

</td><td>

The first parameter of the event.

 **Note:** If this parameter is a string value, it must be within quotes \(" "\).

</td></tr><tr><td>

Parameter 2

</td><td>

The second event parameter.

 **Note:** If this parameter is a string value, it must be within quotes \(" "\).

</td></tr></tbody>
</table>