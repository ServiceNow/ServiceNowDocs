---
title: Create a schedule plan
description: Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Scheduling your teams' work, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Create a schedule plan

Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability. This way, you can make sure that you are using your resources in the best way possible for your organization.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

You can set the number of days to cache agent schedules using the **sn\_shift\_planning.number\_of\_days\_to\_cache** [system property](../reference/configurable-wfo-itsm-scheduling-reference.md).

If you do any of the following:

-   Import agent schedules using table import
-   Disable business rules and use a script to load the data

you must manually run the **Shift Planning - Delete All Agent Schedules Cache** [schedule job](../reference/configurable-wfo-itsm-scheduling-reference.md) to clear the cache.

**Note:** Your administrator can set user preferences for the pagination size to view schedule plans. For more information see, [Scheduling in Workforce Optimization for ITSM](../reference/configurable-wfo-itsm-scheduling-reference.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png)\).

3.  Create a schedule plan.

    1.  Click the **Team Calendar** tab.

        **Note:** You can analyze the staff alignment for a day or for the week.

    2.  In the contextual side panel, click the Show Schedules icon ![Show Schedules icon.](../image/show-schedules-icon.png) to display the schedules.
    3.  In the Schedules panel, click the + icon.

        **Tip:**

        -   **Search schedules:** Type keywords in the Schedules search field to access related schedule plans easily.
        -   **Filter schedules:** Select the filter icon \(![Filter schedule](../image/show-filter-icon.png)\) and then select the desired schedule states using the **Schedule plan state** filter and the desired start and end dates using the **Schedule plan dates** filter to narrow down the display of schedules in the team calendar.
        You can duplicate an existing schedule to create another one. The start date changes to the day after the current date and the end date changes to 30 days from the current date.

    4.  In the **Name** field, enter a name for the schedule plan.
    5.  From the **Start Date** field, select a date to start the schedule plan and click **OK**.
    6.  From the **End Date** field, select a date to end the schedule plan and click **OK**.
    7.  In the **Assignment groups** section, assign the schedule plan to your groups.

        -   To assign it to all groups you manage, select **Groups I manage**.
        -   To assign it to specific groups, select **Specific groups**.
        You can view the schedule of all agents in the assignment group that you directly or additionally manage.

    8.  Click **Save schedule**.
    .

4.  Add a work shift to the schedule plan.

    **Note:** To add more shifts to an existing schedule plan, select the schedule plan and then add the work shift.

    1.  Click **Add Shift**.
    2.  In the **Shift** field, select the work shift that you want to add to the schedule plan.
    3.  In the **Event type** field, select the work event that categorizes the work shift.
5.  Add agents to the work shift.

    1.  In the **Assign agents** field, search for agents and add one or more agents to add to the shift.
    2.  To publish the schedule plan, select **Publish**.
    It may take a few minutes for the screen to refresh. For more information on publishing a schedule plan, see [Publish a schedule plan for visibility into team coverage](publish-schedule-wfo-itsm.md).


**Parent Topic:**[Scheduling your teams' work in Workforce Optimization for ITSM](../concept/scheduling-configurable-workforce-optimization-itsm.md)

