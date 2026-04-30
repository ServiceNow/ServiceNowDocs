---
title: Create or copy a maintenance schedule
description: After creating a maintenance plan, define a maintenance schedule for a maintenance plan. Define duration or meter-based schedules for your assets or locations on a daily, weekly, monthly, or yearly basis.
locale: en-US
release: yokohama
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2025-09-08"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Create or copy a maintenance schedule

After creating a maintenance plan, define a maintenance schedule for a maintenance plan. Define duration or meter-based schedules for your assets or locations on a daily, weekly, monthly, or yearly basis.

## Before you begin

Role required: admin

## About this task

Maintenance schedules are duration or meter based. For example, on the Maintenance Schedule form, select Duration or Meter as the trigger for replacing a printer ink cartridge. Define the maintenance schedule duration as three months and the paper sheets as 10,000. The schedule is triggered when the paper sheets need refill and the printer ink cartridges are replaced based on this trigger. The maintenance schedule populates the **Next run time** \(duration-based schedules\) and **Next run value** \(meter-based schedules\) in the Plan Service configuration. Maintenance schedule job checks for a maintenance schedule template in a plan record and creates maintenance cases.

For more information, see [Create plan service configuration](create-maint-service-config.md) and [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Central.**

2.  Select the **Preventive Maintenance** tab.

3.  Select open a published maintenance plan from **My Plans** or **All plans**.

4.  On the maintenance calendar view, select the **Schedules** tab.

    ![Maintenance plan calendar view showing the Schedules tab.](../images/wsd-maint-mgmt-schedules-tab.png)

5.  Select **Copy schedule** to copy a maintenance schedule for an existing maintenance plan.

6.  Search for a maintenance plan name from the list.

7.  Select **Copy**.

    An existing schedule is copied over to a maintenance plan item.

    **Note:** You can also create a maintenance schedule if copying a schedule isn’t the best option for a maintenance plan.

8.  To create a schedule, select **Create schedule**.

    The New Schedule form opens. Fill in the form fields.

<table id="table_cgj_d21_dzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the schedule. For example: Weekly schedule for meeting rooms.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the schedule or schedule type.

</td></tr><tr><td>

Interval

</td><td>

The time or duration during which the schedule job should run. For example, select any of the following from the drop-down list:

-   Weekly
-   Monthly
-   Annually
-   Week in a month


</td></tr><tr><td>

Active

</td><td>

Select the check box to activate the schedule for a maintenance plan.

</td></tr><tr><td>

Trigger

</td><td>

Option to create a duration or meter-based scheduled maintenance.-   **Duration**: Maintenance to be performed based on time \(Next Run time\). Depending on your selection, additional fields are displayed to define a duration. For example: Quarterly, weekly, hourly, and so on.
-   **Meter**: Maintenance to be performed based on count. Based on your selection, **Every** and **Field** options appear. For example: Change the printer cartridge after every 1000 printed sheets.


</td></tr><tr><td>

Trigger type \(Duration\)

</td><td>

Trigger type determines the schedule run time interval duration \(weekly, monthly, annual, and so on\).![Duration-based schedule for a maintenance plan.](../images/wsd-create-durationbased-schedule.png)

For a duration-based schedule, complete the following field information:

**Interval**: For example, select a duration from the drop-down options. For example: **Weekly**

Repeat: Repeat interval hours. For example: 1 hour.

</td></tr><tr><td>

Trigger type \(Meter\)

</td><td>

For meter-based schedule, complete the following field information: ![Meter-based schedule for a maintenance plan.](../images/wsd-create-schedule-meter-based.png)

-   **Table**: Workplace Location or Model. Selected by default. The selection depends on your selection of Model \(asset\) or Location while creating a maintenance plan. For more information, see [Create and publish maintenance plans](create-publish-maintenance-plans.md).
-   **Field**: Field value for the trigger type. Select a value from the drop-down options. For example, **Start Date and time**.
-   **Every**: The repeat interval duration. The number of occurrences that must be recorded before the maintenance plan is executed. Takes an integer-based value and the value must be greater than zero \(0\). For example: 2 days.


</td></tr><tr><td>

Minimum lead time in days

</td><td>

Applicable only for a duration-based schedule and takes integer-based values \(For example: 2\). Number of days prior to the scheduled due date to determine the date on which the work should begin. That date is pre-filled in the Scheduled start field for the task. This field appears when Duration is selected for Trigger. The scheduled job ensures that the **Next run time** duration has the lead time value considered \(Next run time value = Next schedule target date - Lead time\).

For example, if your **Due day of week** is next week Monday and your lead time is 2, then your lead time is Friday \(the current week\). By Friday, the maintenance plan schedule is assigned to a Workplace Manager or administrator for executing or triggering the schedule next week Monday.

</td></tr></tbody>
</table>9.  Select **Save**.

10. Publish the plan.

11. Select the published plan record and on the calendar view, navigate to the **Schedules** tab.

12. Select and open the schedule to view details.

    ![Published plan record showing the maintenance schedule for a plan record.](../images/wsd-meter-based-schedule-detail-form.png)


**Parent Topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Previous topic:**[Maintenance plan calendar view](cal-view-overview.md)

**Next topic:**[Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md)

**Related topics**  


[Workplace maintenance cases](create-maint-cases.md)

