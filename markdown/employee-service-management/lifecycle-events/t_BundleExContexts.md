---
title: Monitor the status of a lifecycle event case
description: Monitor the status of a lifecycle event case with activity set execution contexts. You can monitor the state of each activity set in a lifecycle event case. You can further monitor the state of the individual activities. You can also report on the activity set contexts table in conjunction with the HR case table.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an HR case for a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Monitor the status of a lifecycle event case

Monitor the status of a lifecycle event case with activity set execution contexts. You can monitor the state of each activity set in a lifecycle event case. You can further monitor the state of the individual activities. You can also report on the activity set contexts table in conjunction with the HR case table.

## Before you begin

Role required: sn\_hr\_le.activity\_reader

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Lifecycle Events Cases**.

    **Note:** Alternatively, you can navigate to **Lifecycle Events** &gt; **Administration** &gt; **Execution Contexts** to view all execution context records.

2.  Open a lifecycle event case.

3.  Under the **Related Links** section, click **Activity Set Execution**.

    ![Under the Related Links section on the HR case form, click Activity Set Execution.](../image/lifecycle-event-activity-set-execution.png)

4.  From the Activity Set Contexts list, you can monitor the state of each activity set in the lifecycle event case.

    ![Monitor the state of each activity set in the lifecycle event case.](../image/lifecycle-event-activity-set-execution-activity-sets.png)

<table id="table_alf_2jw_5fb"><thead><tr><th>

Column headers

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity set

</td><td>

Activity set that is associated with the lifecycle event case.

</td></tr><tr><td>

State

</td><td>

Status of the activity set:-   Awaiting Trigger
-   Running Activities
-   Finished
-   Error
 **Note:** You can monitor the status of individual activities by opening the activity set context record.

</td></tr><tr><td>

HR case

</td><td>

Lifecycle event case that is being monitored.

</td></tr></tbody>
</table>5.  To further monitor the state of each activity within an activity set:

    1.  Click the preview button for the applicable activity set.

        ![Click the Preview button next to each activity set to monitor the state of the individual activities.](../image/lifecycle-event-activity-set-execution-activities.png)

    2.  On the Activity Set Context form, under the Activity Status section, you can monitor the state of each activity within the activity set.

        ![For each activity set, you can monitor the state of the individual activities.](../image/lifecycle-event-activity-set-execution-activities-drilldown.png)


