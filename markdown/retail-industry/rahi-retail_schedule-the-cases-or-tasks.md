---
title: Schedule the store plan
description: Schedule the store plan based on the requirement- immediate, one time, or recurring. Once the store plan gets scheduled, it automates the case and task generation which reduces manual work.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage store plans to generate cases and tasks, Manage store plans, Retail]
---

# Schedule the store plan

Schedule the store plan based on the requirement- immediate, one time, or recurring. Once the store plan gets scheduled, it automates the case and task generation which reduces manual work.

## Before you begin

Role required: sn\_rtl\_hq\_ops.agent, sn\_rtl\_hq\_ops.agent\_manager, sn\_rtl\_hq\_ops.location\_manager, and sn\_fsm\_planned\_wm.planned\_work\_admin

**Note:** Use sn\_fsm\_planned\_wm.planned\_work\_admin role to avail the one-time and recurring schedule options.

## Procedure

1.  On the Schedule form, select **Immediate** to generate a case immediately.

    1.  Select the date by selecting the calendar and enter the time in the **Due date and time**.

2.  Select **One time** to generate a case in future at the scheduled time.

    1.  Select the date by selecting the calendar and enter the time in the **Schedule details** &gt; **Effective Start**.

    2.  Enter the number of days for the case to be due from the effective start date in the **Schedule details** &gt; **Lead time**.

3.  Select **Recurring** to generate recurring cases in future.

    1.  Select the starting date by selecting the calendar and enter the time in the **Schedule details** &gt; **Effective Start**.

    2.  Select the ending date by selecting the calendar and enter the time in the **Schedule details** &gt; **Effective End**.

    3.  Select the trigger type from the **Recurrence details** &gt; **Trigger Type** drop-down list.

    4.  Enter the number of days, hours, minutes, and seconds in the **Recurrence details** &gt; **Repeat** section.

    5.  Enter the number of days for the case to be due from the effective start date in the **Recurrence details** &gt; **Lead time**.

4.  Select **Save** to stay on the window and select **Save &amp; continue** to go to the next step.


## Result

The summary gets generated based on the store plan schedule.

**Parent Topic:**[Manage store plans to generate cases and tasks](rahi-retail-manage-store-plan-authoring.md)

