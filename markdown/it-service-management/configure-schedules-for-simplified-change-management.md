---
title: Configure schedules for Simplified Change Management
description: Create and manage blackout and maintenance schedules for Change Management to control when changes are permitted or blocked across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-schedules-for-simplified-change-management.html
release: australia
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 3
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure schedules for Simplified Change Management

Create and manage blackout and maintenance schedules for Change Management to control when changes are permitted or blocked across your organization.

## Before you begin

Role required: sn\_itsm\_chg\_admin.change\_schedules\_config

## About this task

Use the Blackout and Maintenance windows to schedule a change. Blackout schedules block changes during critical periods such as financial year-end or major platform releases. Maintenance windows designate periods when changes are actively expected, such as recurring patching cycles. Both schedule types serve as the authoritative source for downstream enforcement logic including conflict detection and approval routing.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Change schedules**. \[Omitted image "simplified-change-schedules.png"\] Alt text: Change schedules configuration page

    The **Schedules** list displays the pre-configured schedules, organized under the **Blackouts** and **Maintenance** tabs.

5.  To create a new schedule, select **Add New**.

    **Note:** To edit an existing schedule, select it from the **Schedules** list and make the necessary updates.

6.  In the Name your schedule section, enter a descriptive name in the **Schedule name** field.

    For example, you can include the type, scope, or timeframe, like APAC Holiday Blackout or Monthly Patching Window US East. The name appears in the change calendar, conflict notifications, and audit reports.

7.  In the What type of schedule are you creating? section, select a schedule type.

    |Option|Description|
    |------|-----------|
    |**Blackout schedule**|Changes are blocked during this time.|
    |**Maintenance window**|Changes are allowed only during this time.|

8.  In the Which items does this schedule apply to? section, select a source to define the scope of the schedule.

    |Option|Description|
    |------|-----------|
    |**All CIs**|The schedule applies to all configuration items in the database across the organization.|
    |**CI class**|The schedule applies to a specific class of configuration items, such as all Windows servers.|
    |**Change request**|The schedule applies based on change request attributes such as assignment group, change model, or change type.|

9.  In the When does this schedule run? section, configure the schedule timing.

    1.  Enter the **Start date/time** and **End date/time**, or select **All day** to apply the schedule for the full calendar day.

    2.  In the **Select the correct timezone for your schedule** field, select the applicable timezone.

    3.  Under **Schedule repeat**, select a recurrence pattern.

        |Pattern|Behavior|
        |-------|--------|
        |**One time**|The schedule runs once between the specified dates.|
        |**Weekly**|The schedule repeats every week.|
        |**Monthly**|The schedule repeats every month.|
        |**Yearly**|The schedule repeats every year.|
        |**Specific**|Define a custom recurrence rule.|

    4.  Enter the interval in the **Repeat every** field.

        Runs once from 12:00:00 to 12:00:00 \(US/Pacific\) starting 10 May 2026 and ending 13 May 2026.

10. Select **Save**.

11. When you have finished configuring, select **Mark as configured** to save your settings and mark this step as complete.

    To revert changes made in the current session before saving, select **Undo**.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with Now Assist** conversational flow, accessible from the banner at the top of the page.


## Result

The new schedule is created and appears in the **Schedules** list under the **Blackouts** or **Maintenance** tab, depending on the type you selected. The schedule is active immediately and is used by Change Management for conflict detection and change enforcement.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

**Related topics**  


[Create blackout and maintenance schedules in Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateBlkoutMaintSched.md)

