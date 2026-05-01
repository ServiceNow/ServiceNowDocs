---
title: Confirm Assignment pop-up window
description: When using the dynamic scheduling feature, the Confirm Assignment pop-up window displays the task assignment recommendations.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Choose tasks to run, Assigning WOTs using Dynamic Scheduling, Scheduling and dispatching, Use, Field Service Management]
---

# Confirm Assignment pop-up window

When using the dynamic scheduling feature, the Confirm Assignment pop-up window displays the task assignment recommendations.

When a dispatcher selects multiple tasks for assignment and clicks **Auto Assign**, the results of the task assignment process are displayed in the Confirm Assignment pop-up window. Information about the selected tasks, including the **Short Description**, **Scheduled Start**, and **Estimated End**, is displayed in the following categories.

<table id="table_a14_5ww_vy"><thead><tr><th>

Category

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Assigned

</td><td>

Dynamic scheduling is able to find a suitable agent and recommends the task for assignment.

</td></tr><tr><td>

Unassigned

</td><td>

Dynamic scheduling is not able to find a suitable agent and the task remains unassigned.

</td></tr><tr><td>

Reassigned

</td><td>

Tasks that were previously assigned and have been reassigned to a different agent or time slot to allow for the assignment of the selected tasks.

</td></tr><tr><td>

Not Assigned

</td><td>

Tasks that were previously assigned, have been unassigned to allow for the assignment of the selected tasks, and have not yet been reassigned. Selected tasks that do not match the task filter also appear in the Not Assigned category.

</td></tr></tbody>
</table>The information icon next to each task displays additional information about the task in a tool tip, such as required skills and parts. For unassigned and reassigned tasks, this information also includes the previous agent and schedule start time.

If more tasks are selected than dynamic scheduling can handle, the pop-up window displays a message to reduce the number of tasks.

If there has been an update to any of the selected tasks, an informational message notifies the dispatcher to run the recommendations again.

Clicking **Save** confirms the task assignment recommendations listed in the Confirm Assignment pop-up window.

## Task assignment debug log

System administrators can also view task assignment debug logs in the Confirm Assignment pop-up window by enabling the **com.snc.dynamic.scheduling.showlogs** system property. This information is displayed below each task in the pop-up window. Collapse or expand the debug log by clicking on the task.

