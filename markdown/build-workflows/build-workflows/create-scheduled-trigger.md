---
title: Create a saved scheduled trigger
description: Create a scheduled trigger that starts your flow when you need. Schedule the trigger to start your flow on a specific date and time or repeatedly at scheduled intervals. Reuse the trigger in flows that need to run on the same schedule.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Create a saved scheduled trigger

Create a scheduled trigger that starts your flow when you need. Schedule the trigger to start your flow on a specific date and time or repeatedly at scheduled intervals. Reuse the trigger in flows that need to run on the same schedule.

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin.

## About this task

Choose from a variety of scheduling options to create a scheduled trigger that starts your flow at the required time and interval. You can schedule a trigger in any time zone, with or without an end date for the schedule.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Trigger**.

    The New Trigger page appears.![Screen to enter the details of your trigger.](../images/scheduled-trigger-properties.png)

3.  Fill in the details for your trigger.

<table id="table_vgt_tld_5fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger name

</td><td>

Unique name to identify the trigger.

</td></tr><tr><td>

Trigger type

</td><td>

Type of trigger to start your flow. Select **Scheduled** &gt; **Recurrence**

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Application

</td><td>

Application to create the trigger. The default is Global.The application scope determines which data your trigger can access and what data it can share.

</td></tr><tr><td>

Domain

</td><td>

Domain scope of the flow. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Show additional properties** and fill any additional properties.

    |Field|Description|
    |-----|-----------|
    |Accessible from|Choice between whether the trigger data should be accessible only from the specified application or all application scopes.|
    |Category|Category where your trigger is displayed.|
    |Trigger annotation|Annotation for your trigger that the user can see before they select it.|

5.  Select **Build trigger**.

6.  On the Trigger definition form, specify the **Scheduling Details**.

    ![Form to specify the scheduling details for your trigger](../images/scheduled-trigger-definition.png)

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

Runs every week or at your chosen interval of weeks. For example, every 2, 3, or 10 weeks.![Option to select the days of the week for scheduling a weekly trigger.](../images/scheduled-trigger-weekly.png)

Select on which days of the week you want the trigger to run. For example, every Monday, Wednesday, and Friday.

</td></tr><tr><td>

Monthly

</td><td>

Runs every month or at your chosen interval of months, for example, every 2, 3, or 24 months.![Option to select the day of the month for scheduling a monthly trigger.](../images/scheduled-trigger-monthly.png)

Select on which day of the month you want the trigger to run:

-   **Fixed day**, for example, on the first day of the month.
-   **Relative weekday**, for example, every first Monday of the month.


</td></tr><tr><td>

Yearly

</td><td>

Runs every year in the selected month.![Option to select the month and the day of the month for scheduling a yearly trigger.](../images/scheduled-trigger-yearly.png)

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

    **Tip:** Your changes are saved automatically in Workflow Studio. Use the undo and redo buttons as you need.

7.  To make the trigger available, select **Publish**.


## Result

The scheduled trigger is created and published. You can use the trigger in any of your flows. For information about creating a flow, see [Create a flow in Workflow Studio](create-flow.md).

**Parent Topic:**[Building triggers](../concept/building-triggers.md)

