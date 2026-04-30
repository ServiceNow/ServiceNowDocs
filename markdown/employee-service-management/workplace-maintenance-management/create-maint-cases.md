---
title: Workplace maintenance cases
description: The schedule job creates maintenance cases for plan records.
locale: en-US
release: yokohama
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2025-09-07"
reading_time_minutes: 2
breadcrumb: [Manage, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace maintenance cases

The schedule job creates maintenance cases for plan records.

## Before you begin

The scheduled job Workplace Planned Maintenance Nightly runs every 48 hours \(end of day tomorrow\) and creates duration-based and meter-based cases.

Role required: admin

## Procedure

1.  Select a published plan record.

2.  On the calendar view, select the **Maintenance case** tab to view cases created by the scheduled job.

    The **Workplace Maintenance Nightly run** scheduled job generates maintenance cases for maintenance plan records.

    ![The Overview tab for a Maintenance plan calendar view showing maintenance cases.](../images/wsd-maint-overview-tab.png)

3.  Select a maintenance case to view the **Workplace Service** associated with a maintenance case and the scheduled job value for a case.

    For more information, see [Create plan service configuration](create-maint-service-config.md).

    ![Published plan showing maintenance cases with an associated workplace service and a schedule.](../images/wsd-published-maint-case-wiht-service.png)

4.  Select a maintenance case to open the Case details panel and perform the following to update the record:

    1.  State: Update the maintenance case details by changing the maintenance plan state \(Draft, Work in progress, Complete, and so on\).

    2.  Assigned to: Select a user to assign this case.

    3.  Assigned to group: Select a user group to assign this case.

    4.  Select **Update**.

5.  Navigate to **All** &gt; **System Definitions** &gt; **Scheduled jobs**.

    1.  Search for Workplace Maintenance Management in the Application Column.

    2.  **Workplace Maintenance Nightly run**: This scheduled job runs every 48 hours \(end of day tomorrow\) and generates maintenance cases for maintenance plan records.

    3.  To execute the schedule job before the scheduled time, select **Execute Now**.

        The scheduled job checks for active plan records with a **Next Run time** \(duration-based schedule\) or **Next run value** \(meter-based schedule\) and checks for a schedule template in a plan record. When it finds a schedule template, it creates maintenance cases.

        For more information about how to create a scheduled job and how the scheduled job picks up plan records based on conditions and workplace services, see [Create or copy a maintenance schedule](create-maint-schedule.md) and [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

6.  To optimize cleaning activities for a selected location using Agentic AI workflow, the Optimize cleaning activity scheduled job is executed.

    For more information, see [Components installed with Workplace Maintenance Management](../reference/components-installed-with-maintenance-mgmt.md) and [Optimize cleaning activities agent overview](../../now-assist-wsd/concept/optimise-cleaning-agent-overview.md).


**Parent Topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Previous topic:**[Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md)

**Next topic:**[Create workplace services](create-workplace-services.md)

