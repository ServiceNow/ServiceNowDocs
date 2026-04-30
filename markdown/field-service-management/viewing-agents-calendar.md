---
title: Viewing an agent's calendar
description: You can view an agent's schedule, availability, personal events, and tasks that are either assigned or work in progress.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Viewing an agent's calendar

You can view an agent's schedule, availability, personal events, and tasks that are either assigned or work in progress.

The calendar displays agent information for a selected day, work day, or week. Agents are displayed based on membership availability within the calendar window. If the date falls within the specified range, the agent is shown. The tasks that are assigned to an agent appear in the agent's calendar slots. A horizontal line that appears on the left side of a task can indicate either of the following information:

-   Estimated travel start time that includes Estimated onsite arrival buffer duration
-   Actual travel start time
-   Scheduled work start time
-   Actual work start time

**Note:** No visual indicator appears for the tasks that don't have a specified travel start time. Additionally, **Estimated onsite arrival buffer duration** is considered only when `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled and have been added to the task card. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).

![Calendar showing tasks assigned to agents, available agents, and agent schedules for a selected day or week.](../image/agent-calendar-schedule.png)

As a dispatcher, you can do the following:

-   Set defaults for the resource filters by checking the **Save as default view** and selecting **Apply**. This over-writes the existing selections and retains your new resource selections even after a session ends.

    **Note:** Selections are retained only if you save them as the default view. Unsaved selections are erased after the session ends.

-   View the last saved defaults by selecting the **Reset to default view** check box. This option is visible only if your new selections are different from the default selections.
-   Use the territory filter icon to assign tasks to agents based on their skills, availability, and geographic locations.
-   Use the task number to view the task SLA in the task panel or calendar. The task appears in the agent's calendar slot.
-   Use the more actions icon and select **Remove all time gaps** to rearrange a schedule so tasks happen back to back. Any required timing between tasks is honored.
-   View the task SLA details in the task SLA record, such as the stage of the task SLA and whether the SLA has been breached. SLA details show on the task card in the task panel and the calendar. The number on the card in the task panel is the amount of time remaining before the SLA is breached. The horizontal line that appears under the task in the calendar view is a task bar. The bar and the number in the task panel, indicate the stage of task SLA with different colors based on the following SLA durations:

    |SLA duration|Bar color|
    |------------|---------|
    |Below 50%|Green|
    |In-between 50% and 75%|Yellow|
    |In-between 75% and 100%|Orange|
    |Above 100% \(breached\)|Red|
    |Paused|Gray|


