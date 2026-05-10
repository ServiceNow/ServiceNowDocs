---
title: Track and manage your team's schedule
description: Create, update, or monitor your team's schedule from one location. You can approve or reject requests for swapping shifts or time off for agents within your assignment group.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scheduling, Workforce Optimization, Managing workforce, Use, Field Service Management]
---

# Track and manage your team's schedule

Create, update, or monitor your team's schedule from one location. You can approve or reject requests for swapping shifts or time off for agents within your assignment group.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

Using the calendar, you can do the following:

-   View all of your agents by assignment group.
-   Get insights into team compliance with published schedules.
-   View agent's work schedule that is actual shift time vs clock-in and clock-out times.
-   Filter the team calendar based on the values in the **Assignment Group**, **Location**, **Skills**, **Shift Plan**, and **Events** fields for a customized view.
-   Modify agent's shift, clock-in, and clock-out times, if required

**Note:** The "sn\_shift\_planning.agent" role is required for an agent's schedule to be visible in the Team calendar in Manager Workspace.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).

3.  Modify an agent's shift times.

    The schedule that includes this shift must be in the Preview or Published state.

    1.  In the **Team Calendar** tab, navigate and point to the shift for the agent that you want to modify the schedule for.

        **Note:** Note: To avoid delays in loading events, as well as other processes that utilize a caching mechanism through an event queue, see [Custom queues to process events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/useful-server-side-scripts.md).

    2.  In the shift pop-up window, click the Edit icon \(![Edit icon.](../image/EditWidgetButton.png)\).
    3.  Modify the agent's shift time.

        **Note:** If the existing shift has a break, you can add more breaks to the shift.

    4.  Click **Save**.
    The following snapshot displays the time worked summary for a selected agent.![Manager Workspace Team Calendar showing several agent schedules organized by hours in the day.](../../workforce-optimization-for-customer-service-configurable/image/team_calendar_new.png)

4.  Approve or reject an agent's time off or shift-swap with another agent.

    **Note:**

    You must approve a request two days before the time-off or shift-swap start date. Outside that time period, the approval will be auto-rejected. For more information, see the descriptions of **Setting the due date for time-off and shift-swap request approvals** in [Components installed with Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/components-installed-configurable-wfo-cs.md).

    Overlapping time-off requests by an agent will be rejected.

    1.  Click **Approvals**.

    2.  Select the request.

    3.  Accept or reject the request.

        You can view all agent requests in your queue and the details for each request.

        -   To approve a request, click **Approve**.

            If you approve the request, the schedule gets updated in the team calendar based on the approvals.

        -   To reject a request, click **Reject**.

