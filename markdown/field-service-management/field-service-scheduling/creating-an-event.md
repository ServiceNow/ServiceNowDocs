---
title: Create a personal event
description: Enable agents and managers to efficiently schedule events, including time off and appointments, through Workforce. Additionally, managers have the capability to organize meetings and schedule time off and training.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the team calendar, Managing agents and tasks from Workforce, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Create a personal event

Enable agents and managers to efficiently schedule events, including time off and appointments, through Workforce. Additionally, managers have the capability to organize meetings and schedule time off and training.

## Before you begin

Role required: wm\_agent, wm\_manager

## About this task

Agents can only create personal events for themselves, while managers can create events for anyone they manage.

## Procedure

1.  Navigate to **Workforce**.

    -   Managers, navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Workforce**.
    -   Agents, navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Workforce**.
    -   If Workforce Optimization is installed and activated, navigate to **Workspaces** &gt; **Manager Workspace** &gt; **Workforce**.
2.  Click the **Event Management** icon in the right side panel.

3.  On the form, fill in the fields.

4.  Click **Save.**

    **Note:**

    When an event is created in Workforce, its data is stored in the **`cmn_schedule`** table, and the associated time spans are stored in the **`cmn_schedule_span`** table.

    -   **`cmn_schedule`** contains the overall schedule record for the event.
    -   **`cmn_schedule_span`** stores the individual time segments that define the event’s duration.
    To verify that an event has been successfully created, check for its record in the **`cmn_schedule`** table and confirm that the corresponding spans exist in **`cmn_schedule_span`**.


**Parent Topic:**[Using the team calendar](using-team-calendar.md)

**Related topics**  


[View personal events on the Team calendar in Workforce](view-personal-events-on-the-team-calendar.md)

