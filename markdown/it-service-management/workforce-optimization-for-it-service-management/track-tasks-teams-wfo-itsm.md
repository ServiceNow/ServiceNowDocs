---
title: Assign work based on your teams' skills and capacity
description: Plan your teams' work and assign work items such as incidents, problems, change requests, or interactions to them based on their skills, availability, and capacity. View your teams' shifts, events, and work assignments and assign or reassign the work items from a central location.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Assigning work, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Assign work based on your teams' skills and capacity

Plan your teams' work and assign work items such as incidents, problems, change requests, or interactions to them based on their skills, availability, and capacity. View your teams' shifts, events, and work assignments and assign or reassign the work items from a central location.

## Before you begin

**Note:** Your administrator must add sys ids for event categories that you want to display in the calendar to the **sn\_wfo\_work\_sched.shift\_data\_categories** system property. For more information, see [Work Scheduler components in Workforce Optimization for ITSM reference](../reference/work-scheduler-wfo-itsm-reference.md).

Role required: sn\_wfo\_work\_sched.manager

## About this task

Analyze the tasks that your agents are assigned to and their actual shift plans. If the agent doesn’t work during the duration the task has to be completed, you can reassign the task based on agent availability.

**Note:**

-   Each type of task is displayed in the color defined in the queue configuration.
-   You can enter keywords in the **Search** field in the sidebar to search a card.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select the **Work Scheduler** icon.

    -   You can view the work shifts of all of your agents for all teams you manage. When you select the shift, the pop-up displays the shift details such as the shift time span and agent break times.
    -   In the contextual side panel, select the Filter icon \( ![Filter icon](../../service-operations-workspace/image/filter-icon.png)\) and then select any filter, add the desired criteria, and select **Apply** to narrow down the display of the team members in the calendar. You can filter based on your team's assignment group, skills, location, schedule plan, or shift plan.
3.  If you don’t have any queue configurations in the Work scheduler, select the queue settings icon \(![Queue filter icon](../image/queuefilter.png)\) and then enable up to five work item types.

    The application creates a queue configuration and corresponding filters for each enabled work item type.

4.  Create a queue configuration.

    1.  Select **Queue configurations**.

    2.  In the **My queue configurations** list, select **New**.

    3.  On the form, fill in the fields.

        |Name|Description|
        |----|-----------|
        |Name|Name for the queue configuration.|
        |Work configuration|The type of work configuration you want to use for the queue configuration.|
        |Color|The work item color that displays in the calendar.|
        |Order|The order number in which you want the queue configuration displayed in Work scheduler.|
        |Matching rule|The matching rule for the work item type.|

    4.  Select **Save**.

5.  Analyze your teams' work and schedule.

    1.  From the **Queue** menu, select a work item to view related tasks.

        For example, if you select **Unassigned Incidents**, you can see all tasks related to the Unassigned Incident queue.

        You can select a time zone to view the agent schedule in that time zone.

    2.  Analyze the tasks and work shifts for each agent in the calendar.

        You can use the pagination to scroll through the work shifts.

6.  Assign a work item to an agent.

    1.  Select a task that you want to assign to an agent.

        When you enable the **Show suggested only** option, by default, you can choose to display team members based on their availability, skills, or time zone. The ranking of the team members are based on matching assignment rules set for each criteria. Work scheduler uses [Assignment workbench](https://www.servicenow.com/docs/access?context=case-assignment-matching-criteria&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) to evaluate agents to work on tasks.

        You can select one or more of these criteria and the ranking of the team members will be based on the selected criteria:

        -   **WFO - Availability**—The number of hours the team member is available.
        -   **WFO - Mandatory skills**— If the task has mandatory and optional skills associated with it, the work scheduler displays agents who have all of the mandatory skills first and then the agents who have the optional skills.
        -   **WFO - Optional skills**— If the task only has optional skills associated with it, then the list displays the agents with the optional skills.
        -   **WFO- Timezone overlap**—The delta between the task time zone and the user's time zone. For example, if the user is located in the Pacific time zone and if the task location is in the Eastern time zone, then it will display as **+3**; if the task location is Hawaii, then it will display as **-3**.
        To add your own matching rule, see [Create a criteria for a matching rule in Work scheduler](assignment-rules-work-scheduler-wfo-itsm.md).

        All of these criteria are based on the **More is better** ranking method where a higher value is better. For example, when the WFO-Mandatory skills criteria is enabled, team members that have more skills that are mandatory to work on the work item will be ranked higher.

        For each criteria, if there is 100% match, then the values are displayed in green color; if not, the values are displayed in yellow color. If all criteria match a 100% then the matching details are displayed in green color; if not, they're displayed in yellow color.

    2.  Select an agent from the work scheduler calendar to whom you want to assign the task.

    3.  Click and drag your mouse device for the time span on the calendar for which you want the agent to work on the task.

        The task is assigned to that agent. You can also edit the duration of the time span or drag the time span and reassign the task to another agent.

        **Note:** From the work queue, when you select a task that has been assigned to an agent, the application auto-scrolls to the page that has the timespan for the task and displays the schedule for the agent.

7.  Update a work item from the calendar.

    1.  Select a desired task on the calendar that you want to update.

    2.  Select the Edit icon to access a work item record.

    3.  On the form, make the necessary updates.

    4.  Select **Update**.

    The image below is a representation of the Work scheduler screen.

    ![Work Scheduler screen](../image/work-scheduler-ui.png)


**Parent Topic:**[Assigning work using Work Scheduler in Workforce Optimization for ITSM](../concept/work-scheduler-wfo-itsm.md)

