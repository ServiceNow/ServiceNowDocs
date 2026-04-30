---
title: Create a scheduled trigger for playbook
description: Create a scheduled trigger that starts your playbook at the required time and interval. You can schedule a trigger in any time zone, with or without an end date for the schedule.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Triggers, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Create a scheduled trigger for playbook

Create a scheduled trigger that starts your playbook at the required time and interval. You can schedule a trigger in any time zone, with or without an end date for the schedule.

## Before you begin

Role required: playbook.admin or pd\_author

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Open the playbook that you want to configure or create a playbook.

3.  On the sidebar, select **Triggers** \(![Icon to open the triggers.)](../images/triggers-icon.png)\).

    **Note:** You can't open triggers until the parent table is specified for the playbook. To specify a parent table, edit **Start** in the diagram view, or open the **More actions menu** \(![More actions menu](../images/icon-horizontal-menu.png)\) and select **Properties**.

    ![Triggers in playbooks with options to edit, delete, or create triggers.](../images/triggers-playbook.png)

    If triggers are already added to the playbook, the **Triggers** screen displays a list of the associated triggers. You can edit, delete, or add a trigger.

4.  Select **Add trigger** &gt; **Scheduled**.

5.  Specify the scheduling details.

    1.  Select the **Time zone** in which you want to schedule the trigger.

    2.  Specify the **Start date and time** for the trigger.

        The date and time is as per the selected time zone.

    3.  Use the **Repeat** and **Every** fields to define the schedule for the trigger.

<table id="table_bs2_msd_5fc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Daily

</td><td>

Runs every day or at your chosen interval of days. For example, everyday, every 2 days, every 3 days and so on.

</td></tr><tr><td>

Weekly

</td><td>

Runs every week or at your chosen interval of weeks. For example, every 2, 3, or 10 weeks.![Option to select the days of the week for scheduling a weekly trigger.](../../flow-designer/images/scheduled-trigger-weekly.png)

Select on which days of the week you want the trigger to run. For example, every Monday, Wednesday, and Friday.

</td></tr><tr><td>

Monthly

</td><td>

Runs every month or at your chosen interval of months, for example, every 2, 3, or 24 months.![Option to select the day of the month for scheduling a monthly trigger.](../../flow-designer/images/scheduled-trigger-monthly.png)

Select on which day of the month you want the trigger to run:

-   **Fixed day**, for example, on the first day of the month.
-   **Relative weekday**, for example, every first Monday of the month.


</td></tr><tr><td>

Yearly

</td><td>

Runs every year in the selected month.![Option to select the month and the day of the month for scheduling a yearly trigger.](../../flow-designer/images/scheduled-trigger-yearly.png)

Select on which day of the month you want the trigger to run:

-   **Fixed day**, for example, on the first day of the month.
-   **Relative weekday**, for example, every fourth Friday of the month.


</td></tr><tr><td>

Time interval

</td><td>

Runs at a specific time interval. Specify the interval in `hh:mm:ss` format. For example, you can create a trigger that runs every 47 hours and 30 minutes \(47:30:00\).

</td></tr><tr><td>

Does not repeat

</td><td>

Runs only once at the specified date and time.

</td></tr></tbody>
</table>    4.  If you want to end the schedule and stop the trigger from running after a certain date, from **End**, select **On this day**.

    5.  To end the schedule, specify an end **Date and time**.

6.  Specify the conditions for the trigger to run.

    Use the **Conditions** tab to add a condition when the playbook should run. You can also limit the number of records to be processed, up to 1000, and sort the records by a field.

7.  Select **Save and close**.


## Result

Your scheduled trigger is created.

**Parent Topic:**[Triggers](../concept/process-automation-designer-triggers.md)

**Related topics**  


[Create a trigger definition](create-trigger-definition.md)

[Add and configure a trigger in a playbook](add-configure-trigger.md)

[Triggers](../concept/process-automation-designer-triggers.md)

