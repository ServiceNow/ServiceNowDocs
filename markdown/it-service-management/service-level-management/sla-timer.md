---
title: SLA timer
description: Use the SLA timer component to track the amount of time that is required to complete the task as defined by the matching SLA definition.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Service Level Management, Service Level Management, IT Service Management]
---

# SLA timer

Use the SLA timer component to track the amount of time that is required to complete the task as defined by the matching SLA definition.

The SLA timer component is designed to visually display the current status of the Task SLA. You can also view more information about the task in the tooltip, such as the SLA definition name, the remaining time to breach, and the percentage completed details. When your task is in-schedule, then the tooltip provides extra information, such as the out-of-schedule details.

The timer component can show any of the following stages depending on the current status of the task.

<table id="table_h41_ksg_zkb"><thead><tr><th>

Stage

</th><th>

Color code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

In-progress

</td><td>

![SLA timer stage: In-progress](../image/sla-timer-inprogress.png)

</td><td>

The stage of the timer when the task SLA is in progress. You can find more information about the schedule and time on tooltip. The color code changes for in-progress state:-   ![SLA timer: 50% time lapsed](../image/sla-timer-inprogressyellow.png)green to yellow: When the time to complete reaches 50%
-   ![SLA timer: 75% time lapsed](../image/sla-timer-inprogressorange.png)yellow to orange: When the time to complete reaches 25%

</td></tr><tr><td>

Breached

</td><td>

![SLA timer state: Breached](../image/sla-timer-breached.png)

</td><td>

The stage of the timer when the time allocated to complete the task SLA is over. The tooltip provides more information on the time that the task was breached.

</td></tr><tr><td>

Cancelled

</td><td>

![SLA timer state: Cancelled](../image/sla-timer-cancelled.png)

</td><td>

The stage of the timer when the task SLA is cancelled. On the tooltip, you can see the time when it was cancelled.

</td></tr><tr><td>

Paused

</td><td>

![SLA timer state: Paused](../image/sla-timer-pause.png)

</td><td>

The stage of the timer when the task SLA is paused or put on-hold. The color displayed in this stage will correspond to the percentage elapsed when the task SLA was paused. When the stage changes from **Paused**to in-progress the timer starts from time when it was paused. You can find more information about the schedule and time on tooltip.

</td></tr><tr><td>

Achieved \(2010 SLA engine\)

</td><td>

![SLA timer state: Achieved](../image/sla-timer-achieved.png)

</td><td>

The stage of the timer when the task SLA is achieved. The information on when it was achieved is seen on the tooltip.

</td></tr><tr><td>

Completed

</td><td>

![SLA timer state: Completed](../image/sla-timer-completed.png)

</td><td>

The stage of the timer when the task SLA is completed. You can see when the it was completed on the tooltip.

</td></tr><tr><td>

Out of Schedule

</td><td>

![SLA timer state: Out-of-schedule](../image/sla-timer-out-of-schedule.png)

</td><td>

The stage of the timer when the task SLA goes out-of-schedule. You can find more information about the schedule and time on tooltip.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Service Level Management](exploring-slm.md)

