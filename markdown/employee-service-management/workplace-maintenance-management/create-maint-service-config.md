---
title: Create plan service configuration
description: Configure a plan service to associate workplace services and set scheduling conditions for a plan record.
locale: en-US
release: australia
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage Workplace Maintenance Management plans, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Create plan service configuration

Configure a plan service to associate workplace services and set scheduling conditions for a plan record.

## Before you begin

The maintenance schedule must have an entry in the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table for a plan record. Set conditions for a scheduling job to create maintenance cases for active plan records.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Preventive Maintenance** &gt; **Plan Service Configurations**.

2.  Select **New**.

3.  On the Workplace Maintenance Configuration form, fill in the fields:

    1.  Workplace service: Name of the Workplace service.

        Select the lookup list icon \(![Lookup list icon.](../../contact-tracing/image/icon-lookup.png)\) and workplace service for a plan record. For example: Cleaning desk.

        For more information, see [Create workplace services](create-workplace-services.md).

    2.  Order: Integer-based value.

        The highest order value is prioritized. For example: 100.

    3.  Select the **Set conditions** filter and apply filter conditions for a selected item.

        For example, select **Schedule****is****Workplace cleaning**. The selected condition is applied to all plan records in a selected plan.

        ![Create plan service configuration.](../images/wsd-schedule-conditions-plan-service-config.png)

        For more information about Workplace services, see [Create workplace services](create-workplace-services.md).

        .

    4.  Select **Set**.

    5.  Expand **View matching results** to see services associated with a plan service configuration.

    1.  Select and open the **View matching results** to see the schedule job **Name****Next run time** or **Next run value** duration.

        ![View matching results showing the Next run value for a meter-based schedule.](../images/wsd-meter-based-next-run-value.png)

        The selected schedule is updated in the Workplace Maintenance Service Configuration table and the schedule template is associated to it. If there’s a template associated to a schedule, it creates a workplace maintenance case.

        ![Workplace template configuration form showing workplace service for a plan record.](../images/workplace-template-configuration-new.png)

        For more information, see [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md) and [Workplace maintenance cases](create-maint-cases.md).

4.  Select **Save**.

5.  The schedule job **Workplace Planned Maintenance Nightly Run** runs and creates maintenance cases for a workplace service in a plan record.

6.  Navigate to a published plan record.

7.  Select **Maintenance cases** in the calendar view.

8.  The Workplace Services column shows the plan service configuration associated with a plan record.

    ![Published maintenance plan showing mapped workplace services to a maintenance case.](../images/wsd-published-maint-case-wiht-service.png)

    This record is updated in the Workplace Maintenance Service Configuration table.

    For more information, see [Workplace maintenance cases](create-maint-cases.md).


**Parent Topic:**[Manage Workplace Maintenance Management plans](../concept/manage-maintenance-plans.md)

**Previous topic:**[Create workplace services](create-workplace-services.md)

**Next topic:**[Workplace maintenance cases](create-maint-cases.md)

