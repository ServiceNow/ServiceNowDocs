---
title: Workplace planned maintenance scheduled job
description: The scheduled Job Workplace Planned Maintenance Nightly Run runs at the configured time and creates maintenance cases. It also pre-creates maintenance cases when the scheduled duration is less than a day.
locale: en-US
release: xanadu
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage Workplace Maintenance Management plans, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace planned maintenance scheduled job

The scheduled Job **Workplace Planned Maintenance Nightly Run** runs at the configured time and creates maintenance cases. It also pre-creates maintenance cases when the scheduled duration is less than a day.

The scheduled job can pre-create cases for day and up to two days ahead of the scheduled time. This is based on the time difference between the system time zone where the job is running, and the workplace agent time zone working on the cases.

The scheduled job **Workplace Planned Maintenance Nightly Run** performs the following:

-   Creates duration-based cases.
-   Creates meter-based cases.

The scheduled job can also pre-create maintenance cases when the schedule configured is less than a day. The duration is based on your system time zone settings. For example, if you have a maintenance schedule of six hours, it creates the following number of maintenance cases:

-   For a six-hour schedule, four maintenance cases are created for each maintenance asset or location in a day.
-   For a six-hour schedule, eight maintenance cases are created for two maintenance assets or locations in a day \(four cases for each\).

    ![Published Workplace Maintenance Plan showing eight maintenance cases for two maintenance items.](../images/wsd-case-generation-with-schedule-less.png "Workplace Maintenance cases")

-   For a six-hour schedule, 12 maintenance cases are created for three maintenance assets or locations \(four cases for each\).

When the scheduled job runs, it creates maintenance cases only for those planned records that have a template associated to a maintenance schedule.

**Note:** When a maintenance schedule is created, it picks up a template from the Workplace maintenance service configuration table \(sn\_wsd\_maintenance\_service\_config\). Based on your requirements, associate a template to a plan record. Multiple templates can be created and associated to a maintenance plan. For more information, see [Create a workplace template configuration](../../workplace-case-mgmt/task/create-workplace-template-confguration.md).

## Duration-based cases

For duration-based cases, the **Workplace Planned Maintenance Nightly Run** scheduled job performs the following:

-   Fetches all active plan records having the **Next run time** duration.
-   Filters out plan records where the Next run time is 48 hours or less than a day.

    ![Published plan showing the Next run time duration.](../images/wsd-plan-record-showing-next-run-time.png "Schedule job Next run time")

-   Checks for an entry in the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table.
-   Gets all records from the Workplace Maintenance Service Configuration table.
-   For each record in the Workplace Maintenance Service Configuration table, the schedule for the current plan record must have a template associated to it.
    -   If there’s a template, the scheduled job creates a maintenance case and updates the **Next run time** in the Workplace Maintenance Service Configuration table for a plan record.
    -   If there’s no template associated to a plan record, the scheduled job fetches the next plan record in a queue.

**Note:** When defining a duration-based maintenance schedule, you can define the **Minimum lead time in days** \(takes integer-based values\). For example, If if the lead time is 0, it indicates that the cases for the current day are created today itself. But if the lead time is 1, the cases were created yesterday, that is, the cases are generated one day ahead of the schedule. The **Next run time** duration has the lead time value defined for a schedule. For more information, see [Create or copy a maintenance schedule](../task/create-maint-schedule.md).

## Meter-based cases

For meter-based cases, the **Workplace Planned Maintenance Nightly Run** scheduled job performs the following:

-   The scheduled job fetches all active plan records having a **Next run value**.
-   For each plan record, the **Next run value** depends on the **Field** name value. The **Field** value is available when you’re creating a meter-based schedule.

    For more information, see in [Create or copy a maintenance schedule](../task/create-maint-schedule.md).

-   The scheduled job retrieves the value of the **Field** name from the Asset \(sn\_ent\_asset\) table and compares it with the **Next run value** for a plan record.
-   The schedule job checks if the **Next run Value** is less than the actual value in the Asset table and proceeds further.
-   if the **Next run value** is more, it fetches the next plan record in a queue.
-   The maintenance schedule for a current plan record must have an entry in the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table.
-   Gets all the records from the Workplace Maintenance Service Configuration table for that schedule in a Plan record.
-   For each record in the Workplace Maintenance Service Configuration table, the schedule for the current plan record must have a template associated to it.
    -   If there’s a template associated to a maintenance schedule, the schedule job creates a workplace maintenance case and updates the **Next run value** for a plan record.
    -   If there’s no template associated to a maintenance schedule, the scheduled job picks up the next plan record in a queue.

**Parent Topic:**[Manage Workplace Maintenance Management plans](manage-maintenance-plans.md)

**Previous topic:**[Create or copy a maintenance schedule](../task/create-maint-schedule.md)

**Next topic:**[Workplace maintenance cases](../task/create-maint-cases.md)

