---
title: Maintenance plan calendar view
description: After publishing a maintenance plan, the plan opens in a calendar view. The calendar view shows the plan details, maintenance items, schedules, plan records, and maintenance cases for a selected plan record.
locale: en-US
release: australia
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage Workplace Maintenance Management plans, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Maintenance plan calendar view

After publishing a maintenance plan, the plan opens in a calendar view. The calendar view shows the plan details, maintenance items, schedules, plan records, and maintenance cases for a selected plan record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the **Preventative Maintenance** tab and select **All Plans**.

3.  Click open an existing plan to view the published maintenance plan in a calendar view.

    The calendar view page is displayed by default when you publish a maintenance plan.

4.  The **Overview** tab shows a weekly calendar for a selected plan record.

    ![Maintenance plan calendar view showing the Overview tab and maintenance cases.](../images/wsd-maint-overview-tab.png)

    **Note:** The Overview tab currently supports the weekly view and the current system time zone.

5.  Click open the **Details** tab.

    The **Details** tab shows the state of the maintenance plan. Changes can be made to the maintenance plan state to reflect whether the maintenance plan is in Draft, In progress, or Active state. Work notes can be created but are only visible to a workplace manager or administrator creating the maintenance plan.

    ![Calendar view showing the Details tab.](../images/wsd-maint-cal-details-tab-comments.png)

    1.  Name: Name of the Workplace Maintenance Plan.

    2.  Active: Plan is active.

    3.  Start date: Start date of the scheduled maintenance plan.

    4.  End date: The end date is when the scheduled maintenance plan ends.

    5.  Compose:

        -   Comments: Option to add comments for Workplace Managers.
        -   Work notes Private: Private work notes.
    6.  Activity: Activity initiated on a Workplace maintenance plan.

    7.  Schedules: Search for schedules.

6.  Select open the **Maintenance items** tab to view maintenance items that you added in the plan type \(location or asset\) field while creating a maintenance plan.

    ![Calendar view showing maintenance items for a maintenance plan.](../images/wsd-cal-maint-items.png)

    1.  Select the record number for a maintenance item \(for example, SPCE0009004\) to view details for the Workplace Core Space form.

        Floors, spaces, and areas associated for a selected building are displayed as part of the maintenance items.

    2.  Case Details panel on the right shows the Workplace Case Management case ID number.

        -   State: Indicates status of a maintenance case.
        -   Assigned to: Indicates the user assigned to a workplace maintenance case.
        -   Assignment group: Indicates user group assigned to a workplace maintenance plan case.
        For more information, see [Workplace maintenance cases](create-maint-cases.md).

7.  If you selected **Skip Scheduling** while creating the plan, you can publish the plan here using the **Publish** option.

    **Note:** The **Publish** option is not available when you select **Skip Scheduling** while creation.

8.  To view the schedule plan for a maintenance record, click the **Schedules** tab.

    You also have the option to create or copy a schedule. For more information, see [Create or copy a maintenance schedule](create-maint-schedule.md).

9.  Select **Plan records**.

    ![Calendar view showing Plan records.](../images/wsd-maint-cal-plan-records.png)

    Plan records page shows the following pre-filled values:

    |Column|Description|
    |------|-----------|
    |Name|Schedule name for a maintenance item.|
    |Source ID|The items associated with the maintenance plan record.|
    |Schedule|Link to the schedule details.|
    |Requested due by|Maintenance plan schedule date.|
    |Next run value|The schedule job run time for a maintenance plan record.|
    |Last completion time|Scheduled job run time completion.|

10. Select **Maintenance cases** tab.

    The workplace Maintenance cases are created only if the corresponding plan record can pick a template by satisfying a condition in the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table. You can construct any condition on the Workplace Maintenance Service Configuration table, and the template is assigned to a maintenance case when a condition is satisfied. For more information, see [Create plan service configuration](create-maint-service-config.md).

    |Column|Description|
    |------|-----------|
    |Number|Case ID for a maintenance case. It is linked to the case details, schedules, and attachments.|
    |Short description|Description of a maintenance plan.|
    |State|Status of a maintenance item.|
    |Scheduled on|The date on which the maintenance case is scheduled to run.|
    |Scheduled value|The value is equal to the time \(days\) which the schedule is set to run.|
    |Assigned to|The name of the user in the case is assigned to \(set by the manager\).|
    |Assignment group|The user group assigned to a case and is set by a workplace manager or workplace administrator.|
    |Opened|The date on which the case was opened.|

    A contextual sidebar is available on the right page for Schedules, Case details, and Attachments. You can search for schedules, update case details, and add attachments to workplace maintenance plans.

11. Select **Save.**


**Parent Topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Previous topic:**[Create and publish maintenance plans](create-publish-maintenance-plans.md)

**Next topic:**[Create or copy a maintenance schedule](create-maint-schedule.md)

