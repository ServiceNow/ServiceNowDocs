---
title: Implement automated job scheduling
description: Implement the message processing framework \(automated jobs scheduling\) by using the Queue Registration link on the Event Registration form.
locale: en-US
release: australia
product: System Events
classification: system-events
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring system events, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# Implement automated job scheduling

Implement the message processing framework \(automated jobs scheduling\) by using the Queue Registration link on the Event Registration form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **System** &gt; **Event Registry**.

2.  Select **New** to register a new event.

    **Note:** You can also select an existing event to update the configurations.

3.  Click the Queue Registration link in the banner message on the Event Registration form.

    **Note:** You can also disable automated job scheduling by selecting **Disable Automatic Job Scheduling** button on the Queue Registry list page.

    If you have started a new event, the Queue Registry list shows up. If you have selected an existing event, the Queue Registration new record shows up.

4.  Select **New** to create a new queue.

    The Queue Registration form shows up.

5.  On the form, fill in the fields.

<table id="table_c34_gpb_4bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queue

</td><td>

Name of the queue

</td></tr><tr><td>

Application

</td><td>

Scope of the application

</td></tr><tr><td>

Automatic Job Scheduling

</td><td>

Option to implement automated job scheduling

</td></tr><tr><td>

Event Processing Order

</td><td>

Option to select the way of processing events-   Parallel: Process multiple events simultaneously
-   Sequential: Process only one event at a time. The events are inter-dependent and can process only after the previous event is completed
**Note:** Once you have configured the processing order and submitted the queue, it can’t be edited. You can delete the queue and create a new queue.

</td></tr><tr><td>

Job configuration type

</td><td>

Type of job configuration**Note:** This field is disabled when you select Sequential as the Event Processing Order. If you select Parallel as the Event Processing Order, you have 2 options.

-   Constant: Creates the required number of jobs
-   Scale with node: Multiplies jobs by the number of nodes. You can use this option if you are unaware of the number of available nodes


</td></tr><tr><td>

Scale factor

</td><td>

Total number of jobs based on the Job configuration type selected

</td></tr><tr><td>

Poll interval

</td><td>

Determines how frequently jobs should poll and process events of this queue

</td></tr><tr><td>

Description

</td><td>

Optional field to describe about this queue related information

</td></tr></tbody>
</table>6.  Click **Submit**.

    The Queue Registry list shows up. It also shows the update made to the recent queue.

7.  Select the recently added queue.

    The Queue Registration form shows up.

8.  Scroll down to the Related lists section.

9.  Select the **Status** entry in the Queue Details related list.

    **Note:** Since the new queue has been submitted, the Status entry is Active.

    The Queue Details form shows up.

10. Update the number of jobs for this queue as per the requirement.

    You can now manually scale up or down as per the requirements without having to configure everything and can eventually avoid misconfiguration.

11. Click Rollback related link on the Queue Registration form if you want to roll back a queue to its previous configurations without automated job scheduling.

    **Note:** The Rollback related link shows up only if you are in an automated jobs scheduling configuration.

12. Select **Retrieve Configurations** if you want to retrieve any existing job configurations for this queue.

    **Note:** This process is possible only if you are in an automated jobs scheduling configuration.

    If any queue with your suggested queue name already exists in the manual jobs scheduling configuration, the configurations of the existing queue are retrieved. You can then validate and update them as required.


**Parent Topic:**[Configuring System events](../concept/configuring-system-events.md)

